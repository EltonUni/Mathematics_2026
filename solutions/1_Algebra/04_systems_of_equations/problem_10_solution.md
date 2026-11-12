# Exercise 10. A Polynomial Through Three Points

## The problem

Find $p(x) = ax^2 + bx + c$ whose graph passes through $(0,1)$, $(1,3)$ and $(2,9)$.

The unknowns are the **coefficients** $a, b, c$. Each point gives one linear equation in them.

---

## Step 1: Translate each point into an equation

A point $(x_0, y_0)$ lies on the graph exactly when $p(x_0) = y_0$.

- $(0,1)$: $a\cdot 0^2 + b\cdot 0 + c = 1 \;\Longrightarrow\; c = 1$
- $(1,3)$: $a\cdot 1^2 + b\cdot 1 + c = 3 \;\Longrightarrow\; a + b + c = 3$
- $(2,9)$: $a\cdot 2^2 + b\cdot 2 + c = 9 \;\Longrightarrow\; 4a + 2b + c = 9$

---

## Step 2: The linear system

$$
\begin{cases}
c = 1,\\
a + b + c = 3,\\
4a + 2b + c = 9.
\end{cases}
$$

In matrix form $M\mathbf{u} = \mathbf{y}$ with unknown vector $\mathbf{u} = (a,b,c)^T$:

$$
\begin{pmatrix}
0 & 0 & 1\\
1 & 1 & 1\\
4 & 2 & 1
\end{pmatrix}
\begin{pmatrix} a \\ b \\ c \end{pmatrix}
=
\begin{pmatrix} 1 \\ 3 \\ 9 \end{pmatrix}
$$

---

## Step 3: Augmented matrix

$$
\left(\begin{array}{ccc|c}
0 & 0 & 1 & 1\\
1 & 1 & 1 & 3\\
4 & 2 & 1 & 9
\end{array}\right)
$$

The entry in position $(1,1)$ is $0$, so we need a row swap.

---

## Step 4: Gaussian elimination

**Swap** $R_1 \leftrightarrow R_2$:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 3\\
0 & 0 & 1 & 1\\
4 & 2 & 1 & 9
\end{array}\right)
$$

**Eliminate $a$ from row 3:** $R_3 \leftarrow R_3 - 4R_1$:

- $(4-4,\ 2-4,\ 1-4,\ 9-12) = (0,\,-2,\,-3,\,-3)$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 3\\
0 & 0 & 1 & 1\\
0 & -2 & -3 & -3
\end{array}\right)
$$

**Swap** $R_2 \leftrightarrow R_3$ so the second pivot is in column 2:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 3\\
0 & -2 & -3 & -3\\
0 & 0 & 1 & 1
\end{array}\right)
$$

This is row echelon form with **3 pivots**, so the solution is unique.

---

## Step 5: Back substitution

**Row 3:** $c = 1$.

**Row 2:**
$$
-2b - 3c = -3 \;\Longrightarrow\; -2b = -3 + 3 = 0 \;\Longrightarrow\; b = 0.
$$

**Row 1:**
$$
a + b + c = 3 \;\Longrightarrow\; a = 3 - 0 - 1 = 2.
$$

So $a = 2,\ b = 0,\ c = 1$ and

$$
p(x) = 2x^2 + 1.
$$

---

## Step 6: Check by substituting all three points

| Point | $p(x) = 2x^2 + 1$ | Result |
|---|---|---|
| $(0,1)$ | $p(0) = 0 + 1 = 1$ | ✓ |
| $(1,3)$ | $p(1) = 2 + 1 = 3$ | ✓ |
| $(2,9)$ | $p(2) = 8 + 1 = 9$ | ✓ |

All three points lie on the graph.

---

## Step 7: Why the solution is unique

Expanding the determinant of the coefficient matrix along the first row:

$$
\det M =
\begin{vmatrix}
0 & 0 & 1\\
1 & 1 & 1\\
4 & 2 & 1
\end{vmatrix}
= 1\cdot(1\cdot 2 - 1\cdot 4) = -2 \neq 0.
$$

So $M$ is invertible and exactly one quadratic passes through these three points. This is a general fact: three points with distinct $x$-coordinates determine a unique polynomial of degree at most $2$.

---

## Final answer

$$
p(x) = 2x^2 + 0\cdot x + 1 = 2x^2 + 1,
\qquad (a,b,c) = (2,\ 0,\ 1).
$$