# Exercise 2. Gaussian Elimination: One Solution

## The system

$$
\begin{cases}
x + y + z = 6,\\
2x - y + z = 3,\\
x + 2y - z = 2.
\end{cases}
$$

---

## Step 1: Write the augmented matrix

$$
[A \mid b] =
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
2 & -1 & 1 & 3\\
1 & 2 & -1 & 2
\end{array}\right)
$$

The first pivot is already $1$, so no row swap is needed yet.

---

## Step 2: Eliminate $x$ from rows 2 and 3

- $R_2 \leftarrow R_2 - 2R_1$: $(2-2,\ -1-2,\ 1-2,\ 3-12) = (0,\,-3,\,-1,\,-9)$
- $R_3 \leftarrow R_3 - R_1$: $(1-1,\ 2-1,\ -1-1,\ 2-6) = (0,\,1,\,-2,\,-4)$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & -3 & -1 & -9\\
0 & 1 & -2 & -4
\end{array}\right)
$$

---

## Step 3: Choose a convenient second pivot

Swap $R_2 \leftrightarrow R_3$ so the pivot is $1$ (this avoids fractions):

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & 1 & -2 & -4\\
0 & -3 & -1 & -9
\end{array}\right)
$$

---

## Step 4: Eliminate $y$ from row 3

$R_3 \leftarrow R_3 + 3R_2$:

- Coefficient of $y$: $-3 + 3 = 0$
- Coefficient of $z$: $-1 + 3\cdot(-2) = -7$
- Right-hand side: $-9 + 3\cdot(-4) = -21$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6\\
0 & 1 & -2 & -4\\
0 & 0 & -7 & -21
\end{array}\right)
$$

This is **row echelon form** with three pivots ($1$, $1$, $-7$), so the system has a **unique solution**.

---

## Step 5: Back substitution

**From row 3:**
$$
-7z = -21 \;\Longrightarrow\; z = 3
$$

**From row 2:**
$$
y - 2z = -4 \;\Longrightarrow\; y = -4 + 2\cdot 3 = 2
$$

**From row 1:**
$$
x + y + z = 6 \;\Longrightarrow\; x = 6 - 2 - 3 = 1
$$

---

## Step 6: Check consistency in all original equations

| Equation | Substitution $(x,y,z) = (1,2,3)$ | Result |
|---|---|---|
| $x + y + z = 6$ | $1 + 2 + 3$ | $6$ ✓ |
| $2x - y + z = 3$ | $2 - 2 + 3$ | $3$ ✓ |
| $x + 2y - z = 2$ | $1 + 4 - 3$ | $2$ ✓ |

All three equations are satisfied, so the solution is consistent.

---

## Extra check: the determinant

$$
\det A =
\begin{vmatrix}
1 & 1 & 1\\
2 & -1 & 1\\
1 & 2 & -1
\end{vmatrix}
= 1\big((-1)(-1) - 1\cdot 2\big) - 1\big(2\cdot(-1) - 1\cdot 1\big) + 1\big(2\cdot 2 - (-1)\cdot 1\big)
= -1 + 3 + 5 = 7 \neq 0
$$

Since $\det A \neq 0$, the matrix is invertible and the solution is unique.
(This also matches the pivots: $1\cdot 1\cdot(-7) = -7$, and the one row swap flips the sign, giving $+7$.)

---

## Final answer

$$
\mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}
= \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}
$$