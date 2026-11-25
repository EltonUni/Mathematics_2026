# Exercise 8. Two Systems with the Same Coefficient Matrix

## The two systems

Consider the following two systems of linear equations:

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

## Problem statement

Solve both systems (S1) and (S2) and analyze the shared structure of their elimination steps:

1. Solve each system separately using Gaussian elimination and back substitution, and verify both solutions.
2. Compare the elimination steps for (S1) and (S2) to identify which steps and results can be reused across both systems and which parts must be recomputed.
3. Explain why the operations on $A$ are independent of the right-hand side, and demonstrate how to solve both systems simultaneously using a single combined augmented matrix $[A \mid b_1\ b_2]$.

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

**Elimination.** Swap rows ($R_1 \leftrightarrow R_2$) to place the unit pivot $1$ in the top-left position without introducing fractions:

$$
\left(\begin{array}{cc|c}
2 & 1 & 5\\
1 & -1 & 1
\end{array}\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(\begin{array}{cc|c}
1 & -1 & 1\\
2 & 1 & 5
\end{array}\right)
$$

Now eliminate $x$ from row 2 using the elementary row operation $R_2 \leftarrow R_2 - 2R_1$:

- Coefficient of $x$: $2 - 2\cdot 1 = 0$
- Coefficient of $y$: $1 - 2\cdot(-1) = 3$
- Right-hand side: $5 - 2\cdot 1 = 3$

$$
\left(\begin{array}{cc|c}
1 & -1 & 1\\
2 & 1 & 5
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & -1 & 1\\
0 & 3 & 3
\end{array}\right)
$$

**Back substitution**

$$
3y = 3 \;\Longrightarrow\; y = 1,
\qquad
x - y = 1 \;\Longrightarrow\; x - 1 = 1 \;\Longrightarrow\; x = 2.
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

**Elimination.** Apply the exact same elementary row operations—first $R_1 \leftrightarrow R_2$:

$$
\left(\begin{array}{cc|c}
2 & 1 & 1\\
1 & -1 & 4
\end{array}\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(\begin{array}{cc|c}
1 & -1 & 4\\
2 & 1 & 1
\end{array}\right)
$$

Then eliminate $x$ from row 2 using $R_2 \leftarrow R_2 - 2R_1$:

- Coefficient of $x$: $2 - 2\cdot 1 = 0$
- Coefficient of $y$: $1 - 2\cdot(-1) = 3$
- Right-hand side: $1 - 2\cdot 4 = -7$

$$
\left(\begin{array}{cc|c}
1 & -1 & 4\\
2 & 1 & 1
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & -1 & 4\\
0 & 3 & -7
\end{array}\right)
$$

**Back substitution**

$$
3y = -7 \;\Longrightarrow\; y = -\frac{7}{3},
\qquad
x - y = 4 \;\Longrightarrow\; x - \left(-\frac{7}{3}\right) = 4 \;\Longrightarrow\; x = 4 - \frac{7}{3} = \frac{5}{3}.
$$

**Check:** $2\cdot\frac{5}{3} - \frac{7}{3} = \frac{3}{3} = 1$ ✓ and $\frac{5}{3} - \left(-\frac{7}{3}\right) = \frac{12}{3} = 4$ ✓.

$$
(x,y) = \left(\frac{5}{3},\ -\frac{7}{3}\right)
$$

---

## Part B: Compare the elimination steps

| | System 1 | System 2 |
|---|---|---|
| Elementary row operations | $R_1 \leftrightarrow R_2$, then $R_2 \leftarrow R_2 - 2R_1$ | $R_1 \leftrightarrow R_2$, then $R_2 \leftarrow R_2 - 2R_1$ |
| Left part after elimination | Rows $(1,\ -1)$ and $(0,\ 3)$ | Rows $(1,\ -1)$ and $(0,\ 3)$ |
| Right-hand side after elimination | $(1,\ 3)^T$ | $(4,\ -7)^T$ |

**What is the same:** the choice of pivots, the sequence of elementary row operations ($R_1 \leftrightarrow R_2$ followed by $R_2 \leftarrow R_2 - 2R_1$), and the resulting upper triangular matrix

$$
U = \begin{pmatrix} 1 & -1\\ 0 & 3 \end{pmatrix}.
$$

**What is different:** only the transformed right-hand side column ($(1,\ 3)^T$ versus $(4,\ -7)^T$).

---

## Part C: Why is this part the same?

1. The elementary row operations that are chosen depend **only on the entries of $A$**. Selecting the unit pivot via $R_1 \leftrightarrow R_2$ and determining the multiplier $2$ in $R_2 \leftarrow R_2 - 2R_1$ rely strictly on the first column of $A$; the right-hand side is never consulted.
2. The right-hand side is only **carried along** by the same operations. Each row swap or row replacement acts on the $b$-column as a passive follower.
3. Therefore, for every system $Ax = b$ with this coefficient matrix $A$, the left block always reduces to the exact same upper triangular matrix $U$.

In other words, Gaussian elimination encodes a fixed sequence of elementary transformations applied to whatever vector $b$ is attached, making all work on $A$ completely independent of $b$.

---

## Part D: Doing both systems at once

Because the left part and elementary row operations are identical, we can eliminate **once** on a combined augmented matrix containing both right-hand-side columns:

$$
\left(\begin{array}{cc|cc}
2 & 1 & 5 & 1\\
1 & -1 & 1 & 4
\end{array}\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(\begin{array}{cc|cc}
1 & -1 & 1 & 4\\
2 & 1 & 5 & 1
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|cc}
1 & -1 & 1 & 4\\
0 & 3 & 3 & -7
\end{array}\right)
$$

Then only back substitution is performed separately for each right-hand-side column:

- **Column 1 (System 1):** $3y = 3 \implies y = 1$, and $x - 1 = 1 \implies x = 2$.
- **Column 2 (System 2):** $3y = -7 \implies y = -\frac{7}{3}$, and $x - \left(-\frac{7}{3}\right) = 4 \implies x = \frac{5}{3}$.

This matches Part A and avoids repeating the elimination steps on the coefficient matrix. Both right-hand sides are transformed simultaneously, reducing duplicated work. For many right-hand sides, the saving grows substantially: the initial factorization of $A$ requires approximately $O(n^3)$ arithmetic operations, while each additional right-hand side requires only $O(n^2)$ operations for forward and back substitution. Recording the row swap and elimination multiplier is the basic idea behind an LU factorization with row permutation, written as $PA=LU$. In this example, the row swap is chosen to obtain a convenient unit pivot rather than to follow the standard largest-absolute-value partial-pivoting rule.

---

## Final answer

- **System 1:** $(x,y) = (2,\ 1)$
- **System 2:** $(x,y) = \left(\frac{5}{3},\ -\frac{7}{3}\right)$
- **The same in both cases:** the pivots, the elementary row operations ($R_1 \leftrightarrow R_2$ and $R_2 \leftarrow R_2 - 2R_1$), and the upper triangular matrix $U = \begin{pmatrix} 1 & -1\\ 0 & 3\end{pmatrix}$, because they depend solely on the coefficient matrix $A$.
- **Different:** only the transformed right-hand side column ($(1,\ 3)^T$ versus $(4,\ -7)^T$), which is why back substitution must be repeated for each system.