# Exercise 12. Homogeneous System

## The system

Consider the following homogeneous system of three linear equations in the unknowns $x,y,z$:

$$
\begin{cases}
x+2y-z=0,\\
2x+4y-2z=0,\\
x-y+2z=0.
\end{cases}
$$

All right-hand sides are zero, so this is a **homogeneous system** $Ax=\mathbf{0}$.

## Problem statement

Solve the given homogeneous system and analyze its complete solution set.

Show all the essential steps:

1. Write the augmented matrix $[A\mid\mathbf{0}]$ and reduce it to reduced row echelon form (RREF).
2. Identify the basic variables and free variables using the pivot positions.
3. Find all solutions of the system and express the general solution in parametric (vector) form.
4. Verify the general solution by substituting it into all three original equations.
5. Explain why the zero (trivial) solution $(x,y,z)=(0,0,0)$ is always a solution of any homogeneous system $Ax=\mathbf{0}$, and show how it appears in the general solution.
6. Determine whether this particular system has only the trivial solution or also has non-trivial solutions.

---

## Step 1: Augmented matrix

$$
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 0\\
2 & 4 & -2 & 0\\
1 & -1 & 2 & 0
\end{array}\right)
$$

Since the last column is all zeros, it stays zero under every row operation. We could even omit it and work only with $A$.

---

## Step 2: Eliminate $x$ from rows 2 and 3

- $R_2\leftarrow R_2-2R_1$: $(0,0,0,0)$
- $R_3\leftarrow R_3-R_1$: $(0,-3,3,0)$

$$
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 0\\
0 & 0 & 0 & 0\\
0 & -3 & 3 & 0
\end{array}\right)
$$

The zero row means the second equation was redundant (it is $2\times$ the first).

---

## Step 3: Reorder and normalize

Swap $R_2\leftrightarrow R_3$, then apply:

$$
R_2\leftarrow-\frac13R_2
$$

The result is:

$$
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 0\\
0 & 1 & -1 & 0\\
0 & 0 & 0 & 0
\end{array}\right)
$$

This is row echelon form with 2 pivots (columns 1 and 2).

---

## Step 4: Reduced row echelon form

Apply:

$$
R_1\leftarrow R_1-2R_2
$$

We obtain:

$$
\left(\begin{array}{ccc|c}
1 & 0 & 1 & 0\\
0 & 1 & -1 & 0\\
0 & 0 & 0 & 0
\end{array}\right)
$$

---

## Step 5: Identify basic and free variables

- Pivot columns: $x$ and $y$ $\rightarrow$ **basic variables**.
- No pivot in column 3 $\rightarrow$ $z$ is a **free variable**.

The rank and number of free variables are:

$$
\operatorname{rank}(A)=2,\qquad n=3
$$

$$
\text{Number of free variables}=3-2=1.
$$

---

## Step 6: Find all solutions

The RREF gives:

$$
\begin{cases}
x+z=0,\\
y-z=0.
\end{cases}
$$

Therefore:

$$
x=-z,\qquad y=z.
$$

Set $z=t$, where $t\in\mathbb{R}$:

$$
x=-t,\qquad y=t,\qquad z=t.
$$

**Parametric (vector) form:**

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
t\begin{pmatrix}
-1\\
1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
}
$$

Interpretation: the solution set is a line through the origin in $\mathbb{R}^3$ with direction vector $(-1,1,1)$.

---

## Step 7: Verification for any $t$

Substitute $(x,y,z)=(-t,t,t)$ into all three original equations:

- Equation 1:
$$
x+2y-z=-t+2t-t=0
$$
- Equation 2:
$$
2x+4y-2z=-2t+4t-2t=0
$$
- Equation 3:
$$
x-y+2z=-t-t+2t=0
$$

All three equations are satisfied for every real value of $t$.

**Numerical example with $t=1$:**

$$
(x,y,z)=(-1,1,1)
$$

Substitution:

$$
-1+2-1=0
$$

$$
-2+4-2=0
$$

$$
-1-1+2=0
$$

The example also satisfies all three equations.

---

## Step 8: Why $(0,0,0)$ always solves a homogeneous system

For any homogeneous system $Ax=\mathbf{0}$, substitute:

$$
x=\mathbf{0}.
$$

Every equation then has the form:

$$
a_{i1}\cdot0+a_{i2}\cdot0+\dots+a_{in}\cdot0=0.
$$

This is always true.

In matrix notation:

$$
A\mathbf{0}=\mathbf{0}
$$

for every matrix $A$.

**Consequences:**

- A homogeneous system is never inconsistent because the zero vector is always a solution.
- Only two cases are possible: only the trivial solution (when $\operatorname{rank}(A)=n$), or infinitely many solutions (when $\operatorname{rank}(A)<n$).
- In this exercise, $\operatorname{rank}(A)=2<3$, so there are non-trivial solutions in addition to the trivial solution.
- In the parametric solution, the trivial solution $(0,0,0)$ appears when $t=0$.

---

## Final answer

The system has infinitely many solutions, with one free variable $z=t$:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
t\begin{pmatrix}
-1\\
1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
}
$$

The zero solution $(0,0,0)$ is always included because $A\mathbf{0}=\mathbf{0}$. Since the system has one free variable, it also has infinitely many non-trivial solutions.