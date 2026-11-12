# Exercise 14. A Small Change in the Right-Hand Side

## The two systems

$$
\text{(S1)}\ \begin{cases} x + y = 2,\\ 2x - y = 1,\\ 3x = 3, \end{cases}
\qquad\qquad
\text{(S2)}\ \begin{cases} x + y = 2,\\ 2x - y = 1,\\ 3x = 3.1. \end{cases}
$$

Both have 3 equations in 2 unknowns and the **same** coefficient matrix

$$
A = \begin{pmatrix} 1 & 1\\ 2 & -1\\ 3 & 0 \end{pmatrix}.
$$

They differ only in the last right-hand-side entry: $3$ versus $3.1$.

---

## Part A: System S1

### Step 1: Augmented matrix

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
2 & -1 & 1\\
3 & 0 & 3
\end{array}\right)
$$

### Step 2: Eliminate $x$ from rows 2 and 3

- $R_2 \leftarrow R_2 - 2R_1$: $(0,\,-3,\,-3)$
- $R_3 \leftarrow R_3 - 3R_1$: $(0,\,-3,\,-3)$

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & -3 & -3\\
0 & -3 & -3
\end{array}\right)
$$

### Step 3: Eliminate $y$ from row 3

$R_3 \leftarrow R_3 - R_2$: $(0,\,0,\,0)$

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & -3 & -3\\
0 & 0 & 0
\end{array}\right)
$$

The last row is $0 = 0$: no contradiction. Two pivots, two unknowns:

$$
\operatorname{rank}(A) = \operatorname{rank}([A \mid b]) = 2 = n,
$$

so S1 is **consistent with a unique solution**.

### Step 4: Back substitution

$$
-3y = -3 \Rightarrow y = 1, \qquad x + y = 2 \Rightarrow x = 1.
$$

### Step 5: Check in all three equations

| Equation | Substitution $(1,1)$ | Result |
|---|---|---|
| $x + y = 2$ | $1 + 1$ | $2$ ✓ |
| $2x - y = 1$ | $2 - 1$ | $1$ ✓ |
| $3x = 3$ | $3\cdot 1$ | $3$ ✓ |

$$
(x,y) = (1,\ 1)
$$

---

## Part B: System S2

### Step 1: Augmented matrix

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
2 & -1 & 1\\
3 & 0 & 3.1
\end{array}\right)
$$

### Step 2: Eliminate $x$ from rows 2 and 3

- $R_2 \leftarrow R_2 - 2R_1$: $(0,\,-3,\,-3)$
- $R_3 \leftarrow R_3 - 3R_1$: $(0,\,-3,\,3.1 - 6) = (0,\,-3,\,-2.9)$

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & -3 & -3\\
0 & -3 & -2.9
\end{array}\right)
$$

### Step 3: Eliminate $y$ from row 3

$R_3 \leftarrow R_3 - R_2$: $(0,\ 0,\ -2.9 + 3) = (0,\,0,\,0.1)$

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & -3 & -3\\
0 & 0 & 0.1
\end{array}\right)
$$

### Step 4: Interpret

The last row reads

$$
0\cdot x + 0\cdot y = 0.1,
$$

which is **impossible**. Now there are three pivots in the augmented matrix:

$$
\operatorname{rank}(A) = 2 \neq 3 = \operatorname{rank}([A \mid b]),
$$

so S2 is **inconsistent: no solution**.

### Step 5: Direct confirmation

The first two equations alone force $(x,y) = (1,1)$ (adding them gives $3x = 3$, so $x = 1$ and $y = 1$). Then the third equation would need

$$
3x = 3\cdot 1 = 3 \neq 3.1.
$$

---

## Part C: Why a small change can change the type

1. **Three equations, two unknowns (overdetermined).** The first two equations already determine a single point, $(1,1)$. The third equation is not a new condition on $(x,y)$ in general. It must **happen to agree** with that point.

2. **Compatibility is an exact condition, not an approximate one.** Row 3 of $A$ is a combination of rows 1 and 2:

$$
(3,\,0) = (1,\,1) + (2,\,-1).
$$

For consistency the right-hand sides must obey the same relation:

$$
b_3 = b_1 + b_2 = 2 + 1 = 3.
$$

   S1 satisfies this ($b_3 = 3$). S2 breaks it ($3.1 \neq 3$) by $0.1$.

3. **Geometrically**, each equation is a line in the plane. In S1 the three lines pass through the single point $(1,1)$. In S2 the third line $x = \tfrac{3.1}{3} \approx 1.0333$ is a vertical line slightly shifted, so it misses the point where the first two lines cross. Three lines meeting in exactly one common point is a *special* situation, and any perturbation destroys it.

4. **In terms of rank**, $\operatorname{rank}([A\mid b])$ jumps from $2$ to $3$ because $b$ moves out of the column space of $A$. The column space of $A$ is only a 2-dimensional plane inside $\mathbb{R}^3$, and a generic $b$ is not in it. The vector $b = (2,1,3)^T$ lies exactly on that plane, while $(2,1,3.1)^T$ does not.

5. **Practical remark.** Systems whose consistency depends on exact equalities are sensitive to small errors (measurement noise, rounding). In such overdetermined cases one often uses **least squares** to find the best approximate solution instead of demanding an exact one.

---

## Summary table

| | S1 ($b_3 = 3$) | S2 ($b_3 = 3.1$) |
|---|---|---|
| $\operatorname{rank}(A)$ | $2$ | $2$ |
| $\operatorname{rank}([A\mid b])$ | $2$ | $3$ |
| Last row after elimination | $0 = 0$ | $0 = 0.1$ |
| Type | Consistent, unique solution | Inconsistent, no solution |
| Solution | $(1,1)$ | none |

---

## Final answer

- **S1** is consistent with the unique solution $(x,y) = (1,1)$.
- **S2** is inconsistent (no solution), since elimination yields $0 = 0.1$.
- A tiny change in $b_3$ changes the type because consistency requires the exact relation $b_3 = b_1 + b_2$, which mirrors the dependence of row 3 on rows 1 and 2. Changing $b_3$ even slightly violates it.