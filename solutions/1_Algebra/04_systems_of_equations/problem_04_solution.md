# Exercise 4. Infinitely Many Solutions

## The system

Consider the following system of three linear equations:

$$
\begin{cases}
x+y+z=2,\\
2x+2y+2z=4,\\
x-y+z=0.
\end{cases}
$$

## Problem statement

Solve the given system using Gaussian elimination and determine whether it has a unique solution, no solution, or infinitely many solutions.

Show all the essential steps:

1. Write the augmented matrix $[A\mid b]$ and apply elementary row operations to obtain row echelon form.
2. Identify the pivot variables and the free variable.
3. Write the general solution in parametric (vector) form, using a parameter for the free variable.
4. Explain why the system has infinitely many solutions.
5. Verify the parametric solution by substituting it into all three original equations. Also provide a numerical example using a chosen parameter value.

---

## Step 1: Write the augmented matrix

$$
[A \mid b] =
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2\\
2 & 2 & 2 & 4\\
1 & -1 & 1 & 0
\end{array}\right)
$$

---

## Step 2: Eliminate $x$ from rows 2 and 3

- $R_2 \leftarrow R_2 - 2R_1$: $(2-2,\ 2-2,\ 2-2,\ 4-4)=(0,0,0,0)$
- $R_3 \leftarrow R_3 - R_1$: $(1-1,\ -1-1,\ 1-1,\ 0-2)=(0,-2,0,-2)$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2\\
0 & 0 & 0 & 0\\
0 & -2 & 0 & -2
\end{array}\right)
$$

The zero row $0=0$ is always true. It carries no information, which means the second equation was redundant (it is $2\times$ the first equation).

---

## Step 3: Reorder rows

Swap $R_2 \leftrightarrow R_3$ so the zero row goes to the bottom:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2\\
0 & -2 & 0 & -2\\
0 & 0 & 0 & 0
\end{array}\right)
$$

---

## Step 4: Normalize the second pivot

Apply:

$$
R_2 \leftarrow -\frac12 R_2
$$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2\\
0 & 1 & 0 & 1\\
0 & 0 & 0 & 0
\end{array}\right)
$$

This is row echelon form with only 2 pivots (in columns 1 and 2) for 3 unknowns.

---

## Step 5: Reduce above the pivot (reduced row echelon form)

Apply:

$$
R_1 \leftarrow R_1-R_2
$$

$$
\left(\begin{array}{ccc|c}
1 & 0 & 1 & 1\\
0 & 1 & 0 & 1\\
0 & 0 & 0 & 0
\end{array}\right)
$$

---

## Step 6: Identify pivot and free variables

- Pivot columns: column 1 ($x$) and column 2 ($y$) $\rightarrow$ basic variables $x,y$.
- Column 3 has no pivot $\rightarrow$ $z$ is a free variable.

Since

$$
\operatorname{rank}(A) = \operatorname{rank}([A\mid b]) = 2 < 3,
$$

the system is consistent and has infinitely many solutions, with one free parameter.

---

## Step 7: Write the parametric solution

From the reduced row echelon form:

$$
\begin{cases}
x+z=1,\\
y=1,\\
z\text{ is free.}
\end{cases}
$$

Set $z=t$, where $t\in\mathbb{R}$. Then:

$$
x=1-t,\qquad y=1,\qquad z=t.
$$

Parametric (vector) form:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1\\
1\\
0
\end{pmatrix}
+t
\begin{pmatrix}
-1\\
0\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
}
$$

Interpretation: the solution set is a line in $\mathbb{R}^3$ passing through $(1,1,0)$ with direction vector $(-1,0,1)$.

---

## Step 8: Check with a chosen parameter value

Choose $t=2$:

$$
(x,y,z)=(1-2,\ 1,\ 2)=(-1,\ 1,\ 2).
$$

| Equation | Substitution | Result |
|---|---|---|
| $x+y+z=2$ | $-1+1+2$ | $2=2$ ✓ |
| $2x+2y+2z=4$ | $-2+2+4$ | $4=4$ ✓ |
| $x-y+z=0$ | $-1-1+2$ | $0=0$ ✓ |

All three equations hold.

**General check (for any $t$):**

- $x+y+z=(1-t)+1+t=2$ ✓
- $2x+2y+2z=2(1-t)+2+2t=4$ ✓
- $x-y+z=(1-t)-1+t=0$ ✓

Therefore, every real value of $t$ gives a valid solution.

---

## Final answer

The system has infinitely many solutions, with free variable $z=t$:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1-t\\
1\\
t
\end{pmatrix},
\qquad t\in\mathbb{R}.
}
$$