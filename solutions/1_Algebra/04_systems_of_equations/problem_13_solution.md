# Exercise 13. Does Every Equation Add New Information?

## The system

$$
\begin{cases}
x_1 + x_2 = 10,\\
x_2 + x_3 = 8,\\
x_1 - x_3 = 2.
\end{cases}
$$

---

## Step 1: Augmented matrix

$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10\\
0 & 1 & 1 & 8\\
1 & 0 & -1 & 2
\end{array}\right)
$$

---

## Step 2: Eliminate $x_1$ from row 3

$R_3 \leftarrow R_3 - R_1$: $(1-1,\ 0-1,\ -1-0,\ 2-10) = (0,\,-1,\,-1,\,-8)$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10\\
0 & 1 & 1 & 8\\
0 & -1 & -1 & -8
\end{array}\right)
$$

---

## Step 3: Eliminate $x_2$ from row 3

$R_3 \leftarrow R_3 + R_2$: $(0,\ -1+1,\ -1+1,\ -8+8) = (0,\,0,\,0,\,0)$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10\\
0 & 1 & 1 & 8\\
0 & 0 & 0 & 0
\end{array}\right)
$$

Row 3 became $0 = 0$: it is always true and adds **no information**. The system is consistent, with

$$
\operatorname{rank}(A) = \operatorname{rank}([A \mid b]) = 2 < 3 = n,
$$

so there is $3 - 2 = 1$ free variable and **infinitely many solutions**.

---

## Step 4: Solve

The pivots are in columns 1 and 2, so $x_3$ is free. Let $x_3 = t$, $t \in \mathbb{R}$.

**From row 2:**
$$
x_2 + x_3 = 8 \;\Longrightarrow\; x_2 = 8 - t.
$$

**From row 1:**
$$
x_1 + x_2 = 10 \;\Longrightarrow\; x_1 = 10 - (8 - t) = 2 + t.
$$

**Parametric (vector) form:**

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}
=
\begin{pmatrix} 2 \\ 8 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

The solution set is a **line in $\mathbb{R}^3$** through $(2,8,0)$ with direction $(1,-1,1)$.

---

## Step 5: Verification (for any $t$)

With $(x_1,x_2,x_3) = (2+t,\ 8-t,\ t)$:

- $x_1 + x_2 = (2+t) + (8-t) = 10$ ✓
- $x_2 + x_3 = (8-t) + t = 8$ ✓
- $x_1 - x_3 = (2+t) - t = 2$ ✓

Example with $t = 1$: $(3,7,1)$ gives $3+7=10$, $7+1=8$, $3-1=2$ ✓.

---

## Step 6: Which equation follows from the others? Proof by calculation

Subtract equation 2 from equation 1, both sides:

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8
\;\Longrightarrow\;
x_1 - x_3 = 2.
$$

This is exactly equation 3. Hence

$$
\text{Eq.}_3 = \text{Eq.}_1 - \text{Eq.}_2.
$$

In terms of the rows of the augmented matrix:

$$
(1,\,0,\,-1 \mid 2) = (1,\,1,\,0 \mid 10) - (0,\,1,\,1 \mid 8).
$$

So **equation 3 is a consequence of equations 1 and 2**. Any $(x_1,x_2,x_3)$ satisfying the first two automatically satisfies the third.

---

## Step 7: Are the equations "independently necessary"?

- Not all three: equation 3 can be **deleted** without changing the solution set.
- The relation $\text{Eq}_3 = \text{Eq}_1 - \text{Eq}_2$ is symmetric. It can be rewritten as $\text{Eq}_1 = \text{Eq}_2 + \text{Eq}_3$ or $\text{Eq}_2 = \text{Eq}_1 - \text{Eq}_3$, so **any one** of the three equations could be dropped.
- But **not two**: any two equations are not proportional, so they are independent, and together they still give rank $2$. Removing a second equation would leave a single equation with a 2-parameter family of solutions, which is too many.

So only **two independent equations** are needed, matching $\operatorname{rank}(A) = 2$.

---

## Step 8: Geometric interpretation

Each equation is a plane in $\mathbb{R}^3$. The three planes are not in general position: they all contain the same line, so they intersect in a **line** and not in a single point. The third plane adds no new restriction.

---

## Final answer

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}
=
\begin{pmatrix} 2 + t \\ 8 - t \\ t \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

The system has infinitely many solutions (one free variable, $x_3$). The three equations are **not** all independent: $x_1 - x_3 = 2$ equals the first equation minus the second, so it carries no new information.