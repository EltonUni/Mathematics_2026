# Exercise 13. Does Every Equation Add New Information?

## The system

Consider the following system of three linear equations in the unknowns $x_1,x_2,x_3$:

$$
\begin{cases}
x_1+x_2=10,\\
x_2+x_3=8,\\
x_1-x_3=2.
\end{cases}
$$

## Problem statement

Solve the given system and determine whether all three equations provide independent information.

Show all the essential steps:

1. Solve the system using Gaussian elimination and back substitution. Write the general solution in parametric (vector) form.
2. Verify the general solution by substituting it into all three original equations.
3. Determine whether the three equations are linearly independent or whether one equation follows from the others.
4. Show the explicit algebraic calculation proving which equation can be obtained from the other two.
5. Explain how many independent equations are actually necessary to describe the solution set.

---

## Step 1: Augmented matrix

$$
\left(\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
1&0&-1&2
\end{array}\right)
$$

---

## Step 2: Eliminate $x_1$ from row 3

Apply:

$$
R_3\leftarrow R_3-R_1
$$

This gives:

$$
(1-1,\ 0-1,\ -1-0,\ 2-10)
=(0,-1,-1,-8)
$$

The resulting matrix is:

$$
\left(\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&-1&-1&-8
\end{array}\right)
$$

---

## Step 3: Eliminate $x_2$ from row 3

Apply:

$$
R_3\leftarrow R_3+R_2
$$

This gives:

$$
(0,\ -1+1,\ -1+1,\ -8+8)=(0,0,0,0)
$$

The resulting matrix is:

$$
\left(\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&0&0&0
\end{array}\right)
$$

Row 3 becomes $0=0$. It is always true and adds no new information.

The system is consistent, with:

$$
\operatorname{rank}(A) = \operatorname{rank}([A\mid b]) = 2 < 3 = n.
$$

Therefore, there is one free variable and infinitely many solutions.

---

## Step 4: Solve by back substitution

The pivots are in columns 1 and 2, so $x_3$ is free.

Let:

$$
x_3=t,\qquad t\in\mathbb{R}.
$$

From row 2:

$$
x_2+x_3=8
\quad\Longrightarrow\quad
x_2=8-t.
$$

From row 1:

$$
x_1+x_2=10
\quad\Longrightarrow\quad
x_1=10-(8-t)=2+t.
$$

**Parametric (vector) form:**

$$
\boxed{
\begin{pmatrix}
x_1\\
x_2\\
x_3
\end{pmatrix}
=
\begin{pmatrix}
2\\
8\\
0
\end{pmatrix}
+t
\begin{pmatrix}
1\\
-1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
}
$$

Interpretation: the solution set is a line in $\mathbb{R}^3$ through $(2,8,0)$ with direction vector $(1,-1,1)$.

---

## Step 5: Verification for any $t$

Substitute $(x_1,x_2,x_3)=(2+t,8-t,t)$ into all three original equations:

- Equation 1:
$$
x_1+x_2=(2+t)+(8-t)=10
$$
- Equation 2:
$$
x_2+x_3=(8-t)+t=8
$$
- Equation 3:
$$
x_1-x_3=(2+t)-t=2
$$

All three equations are satisfied for every real value of $t$.

**Numerical example with $t=1$:**

$$
(x_1,x_2,x_3)=(3,7,1).
$$

Checking:

$$
3+7=10,\qquad 7+1=8,\qquad 3-1=2.
$$

The example satisfies all three equations.

---

## Step 6: Which equation follows from the others? Proof by calculation

Subtract equation 2 from equation 1, on both sides:

$$
(x_1+x_2)-(x_2+x_3)=10-8
$$

Simplifying:

$$
x_1-x_3=2.
$$

This is exactly equation 3.

Hence:

$$
\boxed{\text{Eq.}_3=\text{Eq.}_1-\text{Eq.}_2}
$$

In terms of the rows of the augmented matrix:

$$
\boxed{
(1,0,-1\mid 2) = (1,1,0\mid 10) - (0,1,1\mid 8)
}
$$

Therefore, equation 3 is a consequence of equations 1 and 2. Any solution satisfying the first two equations automatically satisfies the third.

---

## Step 7: Are all three equations independently necessary?

- Not all three: Equation 3 can be deleted without changing the solution set.
- The relationship is symmetric:
$$
\begin{aligned}
\text{Eq.}_3&=\text{Eq.}_1-\text{Eq.}_2,\\
\text{Eq.}_1&=\text{Eq.}_2+\text{Eq.}_3,\\
\text{Eq.}_2&=\text{Eq.}_1-\text{Eq.}_3.
\end{aligned}
$$
Therefore, any one of the three equations can be removed, while the other two still describe the same solution set.
- But not two: Any two equations are linearly independent because neither is a scalar multiple of the other. Together, any pair gives rank 2. Removing a second equation would leave only one independent equation and introduce an additional free variable.

Therefore, exactly two independent equations are necessary to describe the solution set, matching:

$$
\operatorname{rank}(A)=2.
$$

---

## Step 8: Geometric interpretation

Each equation represents a plane in $\mathbb{R}^3$.

The three planes are not independent: they all contain the same line, so their intersection is a line, not a single point.

The third plane adds no new restriction because it is already implied by the first two equations.

---

## Final answer

The system has infinitely many solutions, with one free variable $x_3=t$:

$$
\boxed{
\begin{pmatrix}
x_1\\
x_2\\
x_3
\end{pmatrix}
=
\begin{pmatrix}
2+t\\
8-t\\
t
\end{pmatrix},
\qquad t\in\mathbb{R}.
}
$$

The three equations are not all independent. Equation 3 equals Equation 1 minus Equation 2, so only two independent equations are needed to describe the solution set.