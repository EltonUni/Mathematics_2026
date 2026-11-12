# Exercise 9. A System from a Sum Condition

## The system

$$
\begin{cases}
x + y = 10,\\
2x + 5y = 32.
\end{cases}
$$

---

## Step 1: Write the augmented matrix

$$
[A \mid b] =
\left(\begin{array}{cc|c}
1 & 1 & 10\\
2 & 5 & 32
\end{array}\right)
$$

The first pivot is already $1$.

---

## Step 2: Eliminate $x$ from row 2

$R_2 \leftarrow R_2 - 2R_1$:

- Coefficient of $x$: $2 - 2\cdot 1 = 0$
- Coefficient of $y$: $5 - 2\cdot 1 = 3$
- Right-hand side: $32 - 2\cdot 10 = 12$

$$
\left(\begin{array}{cc|c}
1 & 1 & 10\\
0 & 3 & 12
\end{array}\right)
$$

This is **row echelon form** with two pivots ($1$ and $3$), so $\operatorname{rank}(A) = \operatorname{rank}([A \mid b]) = 2 = $ number of unknowns. The system is consistent with a **unique solution**.

---

## Step 3: Back substitution

**From row 2:**
$$
3y = 12 \;\Longrightarrow\; y = 4.
$$

**From row 1:**
$$
x + y = 10 \;\Longrightarrow\; x = 10 - 4 = 6.
$$

---

## Step 4: Check in the original equations

| Equation | Substitution $(x,y) = (6,4)$ | Result |
|---|---|---|
| $x + y = 10$ | $6 + 4$ | $10$ ✓ |
| $2x + 5y = 32$ | $12 + 20$ | $32$ ✓ |

---

## Step 5: Determinant check

$$
\det A = \begin{vmatrix} 1 & 1\\ 2 & 5 \end{vmatrix} = 1\cdot 5 - 1\cdot 2 = 3 \neq 0,
$$

so $A$ is invertible and the solution is unique.

---

## Step 6: Geometric explanation of uniqueness

Each equation describes a line in the plane:

- Line $L_1$: $x + y = 10$, i.e. $y = 10 - x$, with slope $-1$.
- Line $L_2$: $2x + 5y = 32$, i.e. $y = \tfrac{32}{5} - \tfrac{2}{5}x$, with slope $-\tfrac{2}{5}$.

The slopes are **different** ($-1 \neq -\tfrac{2}{5}$), so the lines are **not parallel** and not identical. Two non-parallel lines in the plane meet in **exactly one point**. That point is the solution:

$$
L_1 \cap L_2 = \{(6,\,4)\}.
$$

Equivalently, the normal vectors $(1,1)$ and $(2,5)$ are **linearly independent** (neither is a multiple of the other), which is the same as $\det A \neq 0$. If the lines were parallel, the system would have either no solution or infinitely many.

---

## Final answer

$$
(x,y) = (6,\ 4)
$$

The solution is unique because the two lines have different slopes and therefore intersect in exactly one point.