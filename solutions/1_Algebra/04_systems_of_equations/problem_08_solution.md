# Exercise 8. Two Systems with the Same Coefficient Matrix

## The two systems

$$
\text{(S1)}\ \begin{cases} 2x + y = 5,\\ x - y = 1, \end{cases}
\qquad\qquad
\text{(S2)}\ \begin{cases} 2x + y = 1,\\ x - y = 4. \end{cases}
$$

Both have the same coefficient matrix

$$
A = \begin{pmatrix} 2 & 1\\ 1 & -1 \end{pmatrix},
$$

and differ only in the right-hand side:

$$
b_1 = \begin{pmatrix} 5 \\ 1 \end{pmatrix},
\qquad
b_2 = \begin{pmatrix} 1 \\ 4 \end{pmatrix}.
$$

---

## Part A: Solve each system separately

### System 1

**Augmented matrix**

$$
\left(\begin{array}{cc|c}
2 & 1 & 5\\
1 & -1 & 1
\end{array}\right)
$$

**Elimination.** To avoid fractions, use $R_2 \leftarrow 2R_2 - R_1$:

- Coefficient of $x$: $2\cdot 1 - 2 = 0$
- Coefficient of $y$: $2\cdot(-1) - 1 = -3$
- Right-hand side: $2\cdot 1 - 5 = -3$

$$
\left(\begin{array}{cc|c}
2 & 1 & 5\\
0 & -3 & -3
\end{array}\right)
$$

**Back substitution**

$$
-3y = -3 \;\Longrightarrow\; y = 1,
\qquad
2x + 1 = 5 \;\Longrightarrow\; x = 2.
$$

**Check:** $2\cdot 2 + 1 = 5$ ✓ and $2 - 1 = 1$ ✓.

$$
(x,y) = (2,\ 1)
$$

### System 2

**Augmented matrix**

$$
\left(\begin{array}{cc|c}
2 & 1 & 1\\
1 & -1 & 4
\end{array}\right)
$$

**Elimination.** The same operation $R_2 \leftarrow 2R_2 - R_1$:

- Coefficient of $x$: $2\cdot 1 - 2 = 0$
- Coefficient of $y$: $2\cdot(-1) - 1 = -3$
- Right-hand side: $2\cdot 4 - 1 = 7$

$$
\left(\begin{array}{cc|c}
2 & 1 & 1\\
0 & -3 & 7
\end{array}\right)
$$

**Back substitution**

$$
-3y = 7 \;\Longrightarrow\; y = -\tfrac{7}{3},
\qquad
2x - \tfrac{7}{3} = 1 \;\Longrightarrow\; 2x = \tfrac{10}{3} \;\Longrightarrow\; x = \tfrac{5}{3}.
$$

**Check:** $2\cdot\tfrac{5}{3} - \tfrac{7}{3} = \tfrac{3}{3} = 1$ ✓ and $\tfrac{5}{3} + \tfrac{7}{3} = 4$ ✓.

$$
(x,y) = \left(\tfrac{5}{3},\ -\tfrac{7}{3}\right)
$$

---

## Part B: Compare the elimination steps

| | System 1 | System 2 |
|---|---|---|
| Row operation | $R_2 \leftarrow 2R_2 - R_1$ | $R_2 \leftarrow 2R_2 - R_1$ |
| Left part after elimination | $\begin{pmatrix} 2 & 1\\ 0 & -3\end{pmatrix}$ | $\begin{pmatrix} 2 & 1\\ 0 & -3\end{pmatrix}$ |
| Right-hand side after elimination | $\begin{pmatrix} 5\\ -3\end{pmatrix}$ | $\begin{pmatrix} 1\\ 7\end{pmatrix}$ |

**What is the same:** the choice of pivot, the row operation, and the resulting triangular matrix

$$
U = \begin{pmatrix} 2 & 1\\ 0 & -3 \end{pmatrix}.
$$

**What is different:** only the right-hand side column.

---

## Part C: Why is this part the same?

1. The row operations that are chosen depend **only on the entries of $A$**. The multiplier for $R_2$ is determined by the first column ($2$ and $1$), and the right-hand side is never consulted when choosing it.
2. The right-hand side is only **carried along** by the same operations. Each operation acts on the $b$-column as a passive follower.
3. Therefore, for every system $Ax = b$ with this $A$, the left block always ends up as the same $U$.

In other words, the elimination encodes a fixed transformation: the operation $R_2 \leftarrow 2R_2 - R_1$ is applied to whatever vector $b$ is attached, so the work on $A$ is independent of $b$.

---

## Part D: Doing both systems at once

Because the left part is identical, we can eliminate **once** on a combined augmented matrix with two right-hand-side columns:

$$
\left(\begin{array}{cc|cc}
2 & 1 & 5 & 1\\
1 & -1 & 1 & 4
\end{array}\right)
\xrightarrow{R_2 \leftarrow 2R_2 - R_1}
\left(\begin{array}{cc|cc}
2 & 1 & 5 & 1\\
0 & -3 & -3 & 7
\end{array}\right)
$$

Then only the back substitution is done separately for each column:

- Column 1: $y = 1$, $x = 2$
- Column 2: $y = -\tfrac{7}{3}$, $x = \tfrac{5}{3}$

This matches Part A and halves the elimination work. For many right-hand sides, the saving grows: the expensive elimination on $A$ ($\approx n^3/3$ operations) is done once, and each extra $b$ costs only the cheap steps ($\approx n^2$). This is the idea behind storing an **LU factorization**.

---

## Final answer

- System 1: $(x,y) = (2,\ 1)$
- System 2: $(x,y) = \left(\tfrac{5}{3},\ -\tfrac{7}{3}\right)$
- **The same in both cases:** the pivots, the row operations, and the triangular matrix $U = \begin{pmatrix} 2 & 1\\ 0 & -3\end{pmatrix}$, because they depend only on the coefficient matrix $A$.
- **Different:** only the transformed right-hand side column, which is why back substitution must be repeated for each system.