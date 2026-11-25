# Exercise 10. A Polynomial Through Three Points

## The problem

Find the quadratic polynomial $p(x)=ax^2+bx+c$ whose graph passes through the three points $(0,1)$, $(1,3)$, and $(2,9)$.

## Problem statement

Determine the unknown coefficients $a,b,c$ of the quadratic polynomial $p(x)=ax^2+bx+c$.

Show all the essential steps:

1. Substitute the three given points into the polynomial to form a system of linear equations for $a,b,c$.
2. Write the coefficient system in matrix form and construct its augmented matrix.
3. Solve the coefficient system using Gaussian elimination and back substitution.
4. Construct the resulting polynomial and verify it by substituting each of the three original points into $p(x)$.
5. Explain why the resulting polynomial is unique.

---

## Step 1: Translate each point into an equation

A point $(x_0,y_0)$ lies on the graph exactly when $p(x_0)=y_0$.

- $(0,1)$:
$$
a\cdot0^2+b\cdot0+c=1
\quad\Longrightarrow\quad c=1
$$
- $(1,3)$:
$$
a\cdot1^2+b\cdot1+c=3
\quad\Longrightarrow\quad a+b+c=3
$$
- $(2,9)$:
$$
a\cdot2^2+b\cdot2+c=9
\quad\Longrightarrow\quad 4a+2b+c=9
$$

---

## Step 2: Form the linear system

$$
\begin{cases}
c=1,\\
a+b+c=3,\\
4a+2b+c=9.
\end{cases}
$$

In matrix form $M\mathbf{u}=\mathbf{y}$, with unknown vector $\mathbf{u}=(a,b,c)^T$:

$$
\begin{pmatrix}
0 & 0 & 1\\
1 & 1 & 1\\
4 & 2 & 1
\end{pmatrix}
\begin{pmatrix}
a\\
b\\
c
\end{pmatrix}
=
\begin{pmatrix}
1\\
3\\
9
\end{pmatrix}
$$

---

## Step 3: Write the augmented matrix

$$
\left(\begin{array}{ccc|c}
0&0&1&1\\
1&1&1&3\\
4&2&1&9
\end{array}\right)
$$

The entry in position $(1,1)$ is $0$, so we need a row swap.

---

## Step 4: Gaussian elimination

**Swap $R_1\leftrightarrow R_2$:**

$$
\left(\begin{array}{ccc|c}
1&1&1&3\\
0&0&1&1\\
4&2&1&9
\end{array}\right)
$$

**Eliminate $a$ from row 3:**

Apply $R_3\leftarrow R_3-4R_1$:

$$
(4-4,\ 2-4,\ 1-4,\ 9-12)=(0,-2,-3,-3)
$$

$$
\left(\begin{array}{ccc|c}
1&1&1&3\\
0&0&1&1\\
0&-2&-3&-3
\end{array}\right)
$$

**Swap $R_2\leftrightarrow R_3$** so the second pivot is in column 2:

$$
\left(\begin{array}{ccc|c}
1&1&1&3\\
0&-2&-3&-3\\
0&0&1&1
\end{array}\right)
$$

This is row echelon form with 3 pivots, so the coefficient system has a unique solution.

---

## Step 5: Back substitution

From row 3:

$$
c=1
$$

From row 2:

$$
-2b-3c=-3
$$

Substitute $c=1$:

$$
-2b-3=-3
\quad\Longrightarrow\quad b=0
$$

From row 1:

$$
a+b+c=3
$$

Substitute $b=0$ and $c=1$:

$$
a=3-0-1=2
$$

Therefore:

$$
a=2,\qquad b=0,\qquad c=1
$$

The resulting polynomial is:

$$
\boxed{p(x)=2x^2+1}
$$

---

## Step 6: Verify by substituting all three points

Substitute each given $x$-coordinate into $p(x)=2x^2+1$ and check that the result equals the corresponding $y$-coordinate.

| Given point | Substitution | Result |
|---|---|---|
| $(0,1)$ | $p(0)=2(0)^2+1$ | $1=1$ ✓ |
| $(1,3)$ | $p(1)=2(1)^2+1$ | $3=3$ ✓ |
| $(2,9)$ | $p(2)=2(2)^2+1$ | $9=9$ ✓ |

All three points lie on the graph of the resulting polynomial.

---

## Step 7: Why the solution is unique

The determinant of the coefficient matrix is:

$$
\det M=
\begin{vmatrix}
0&0&1\\
1&1&1\\
4&2&1
\end{vmatrix}
$$

Expanding along the first row:

$$
\det M=1\cdot(1\cdot2-1\cdot4)=-2\neq0
$$

Therefore, $M$ is invertible, and the coefficient system has exactly one solution.

This is also a general fact: three points with distinct $x$-coordinates determine a unique polynomial of degree at most $2$.

In this case, $a=2\neq0$, so the resulting polynomial is indeed quadratic.

---

## Final answer

The required quadratic polynomial is:

$$
\boxed{p(x)=2x^2+0x+1=2x^2+1}
$$

The coefficients are:

$$
\boxed{(a,b,c)=(2,0,1)}
$$

The polynomial passes through all three given points and is unique.