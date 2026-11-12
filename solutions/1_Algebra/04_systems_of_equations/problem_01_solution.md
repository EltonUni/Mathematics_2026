# Exercise 1. From a System to a Matrix

## The system

$$
\begin{cases}
2x - y + z = 4,\\
x + 3y - 2z = 1,\\
3x + y + z = 7.
\end{cases}
$$

We want to write it in the form $Ax = b$.

---

## Step 1: Identify the unknowns

The variables appearing in the equations are $x$, $y$, $z$. We always keep them in the same order in every equation, so we collect them in the **vector of unknowns**:

$$
\mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}
$$

---

## Step 2: Read off the coefficients (coefficient matrix $A$)

Each equation gives one row of $A$. The entries of the row are the coefficients of $x$, $y$, $z$ **in that order**. If a variable is missing, its coefficient is $0$. If it appears without a number, its coefficient is $1$ (and $-y$ means $-1$).

| Equation | Coefficient of $x$ | Coefficient of $y$ | Coefficient of $z$ |
|---|---|---|---|
| $2x - y + z = 4$ | $2$ | $-1$ | $1$ |
| $x + 3y - 2z = 1$ | $1$ | $3$ | $-2$ |
| $3x + y + z = 7$ | $3$ | $1$ | $1$ |

Therefore:

$$
A = \begin{pmatrix}
2 & -1 & 1\\
1 & 3 & -2\\
3 & 1 & 1
\end{pmatrix}
$$

---

## Step 3: Right-hand side vector $b$

The numbers to the right of the equal signs, in the same order as the equations:

$$
b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$

---

## Step 4: Write the system as $Ax = b$

$$
\begin{pmatrix}
2 & -1 & 1\\
1 & 3 & -2\\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
=
\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$

---

## Step 5: Verify that each row corresponds to one equation

Matrix–vector multiplication works **row by row**: the $i$-th entry of $Ax$ is the dot product of the $i$-th row of $A$ with the vector $\mathbf{x}$.

**Row 1:**
$$
(2,\,-1,\,1)\cdot(x,\,y,\,z) = 2x - y + z = 4
$$
This is exactly the first equation.

**Row 2:**
$$
(1,\,3,\,-2)\cdot(x,\,y,\,z) = x + 3y - 2z = 1
$$
This is exactly the second equation.

**Row 3:**
$$
(3,\,1,\,1)\cdot(x,\,y,\,z) = 3x + y + z = 7
$$
This is exactly the third equation.

So multiplying out gives

$$
Ax = \begin{pmatrix} 2x - y + z \\ x + 3y - 2z \\ 3x + y + z \end{pmatrix}
$$

and the equality $Ax = b$ means that these three entries are equal, entry by entry, to $4$, $1$, $7$, which is precisely the original system.

---

## Explanation: how rows correspond to equations

- **Row $i$ of $A$** stores the coefficients of the **$i$-th equation**.
- **Entry $b_i$** is the right-hand side of the **$i$-th equation**.
- **Column $j$ of $A$** stores the coefficients of the **$j$-th unknown** (column 1 → $x$, column 2 → $y$, column 3 → $z$).
- The single matrix equation $Ax = b$ is a compact way of writing all three scalar equations at once.

---

## Final answer

$$
A = \begin{pmatrix}
2 & -1 & 1\\
1 & 3 & -2\\
3 & 1 & 1
\end{pmatrix},
\qquad
\mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix},
\qquad
b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$