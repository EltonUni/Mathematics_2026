# Exercise 5. Row Echelon Form and Number of Solutions

## The augmented matrix

$$
[A \mid b] =
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 3\\
0 & 1 & 2 & 1\\
0 & 0 & 0 & 0
\end{array}\right)
$$

The unknowns are $x, y, z$ (columns 1, 2, 3). The matrix is already in **row echelon form**, so no elimination is needed to read off the structure.

---

## Step 1: Check consistency

Look for a contradictory row of the form $(0\ \ 0\ \ 0 \mid c)$ with $c \neq 0$.

The third row is $(0\ \ 0\ \ 0 \mid 0)$, i.e. $0 = 0$. This is **always true** and carries no information. There is no contradiction, so the system is **consistent**.

---

## Step 2: Find the pivots

- Row 1: leading entry $1$ in column 1 (variable $x$)
- Row 2: leading entry $1$ in column 2 (variable $y$)
- Row 3: zero row, no pivot

So there are **2 pivots**, in columns 1 and 2:

$$
\operatorname{rank}(A) = \operatorname{rank}([A \mid b]) = 2.
$$

---

## Step 3: Count the solutions and free variables

The number of unknowns is $n = 3$. The number of free variables is

$$
n - \operatorname{rank}(A) = 3 - 2 = 1.
$$

**How we know how many variables can be chosen freely:**

- Variables in **pivot columns** (here $x$ and $y$) are **basic**: their values are determined by the equations once the others are fixed.
- Variables in **non-pivot columns** (here $z$) are **free**: they can take any value.
- Since the system is consistent and there is at least one free variable, there are **infinitely many solutions**, with exactly **one parameter**.

---

## Step 4: Write the system from the matrix

$$
\begin{cases}
x + 2y - z = 3,\\
y + 2z = 1,\\
0 = 0.
\end{cases}
$$

---

## Step 5: Solve by back substitution

Let the free variable be $z = t$, with $t \in \mathbb{R}$.

**From row 2:**
$$
y = 1 - 2z = 1 - 2t.
$$

**From row 1:**
$$
x = 3 - 2y + z = 3 - 2(1 - 2t) + t = 3 - 2 + 4t + t = 1 + 5t.
$$

---

## Step 6: Cross-check using the reduced row echelon form

$R_1 \leftarrow R_1 - 2R_2$:

$$
\left(\begin{array}{ccc|c}
1 & 0 & -5 & 1\\
0 & 1 & 2 & 1\\
0 & 0 & 0 & 0
\end{array}\right)
$$

This reads $x - 5z = 1$ and $y + 2z = 1$, so $x = 1 + 5z$ and $y = 1 - 2z$. The result agrees with Step 5.

---

## Step 7: Parametric (vector) form

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
=
\begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} 5 \\ -2 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

Interpretation: the solution set is a **line in $\mathbb{R}^3$** through $(1,1,0)$ with direction vector $(5,-2,1)$.

---

## Step 8: Verification

**General check (for any $t$):**

- Equation 1: $x + 2y - z = (1+5t) + 2(1-2t) - t = 1 + 5t + 2 - 4t - t = 3$ ✓
- Equation 2: $y + 2z = (1-2t) + 2t = 1$ ✓

**Specific check with $t = 1$:** $(x,y,z) = (6,\,-1,\,1)$

- $6 + 2(-1) - 1 = 3$ ✓
- $-1 + 2(1) = 1$ ✓

---

## Final answer

The system is consistent with $\operatorname{rank}(A) = 2 < 3$, so it has **infinitely many solutions** and exactly **one free variable** ($z$):

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
=
\begin{pmatrix} 1 + 5t \\ 1 - 2t \\ t \end{pmatrix},
\qquad t \in \mathbb{R}.
$$