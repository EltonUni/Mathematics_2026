# Exercise 3. Inconsistent System

## The system

$$
\begin{cases}
x + 2y = 3,\\
2x + 4y = 7.
\end{cases}
$$

We want to solve it or show that it has no solution.

---

## Step 1: Write the augmented matrix

$$
[A \mid b] =
\left(\begin{array}{cc|c}
1 & 2 & 3\\
2 & 4 & 7
\end{array}\right)
$$

The first pivot is already $1$.

---

## Step 2: Eliminate $x$ from row 2

$R_2 \leftarrow R_2 - 2R_1$:

- Coefficient of $x$: $2 - 2\cdot 1 = 0$
- Coefficient of $y$: $4 - 2\cdot 2 = 0$
- Right-hand side: $7 - 2\cdot 3 = 1$

$$
\left(\begin{array}{cc|c}
1 & 2 & 3\\
0 & 0 & 1
\end{array}\right)
$$

---

## Step 3: Interpret the contradiction

The second row of the matrix says

$$
0\cdot x + 0\cdot y = 1 \quad\Longleftrightarrow\quad 0 = 1,
$$

which is **impossible** for any values of $x$ and $y$.

A row of the form $(0\ \ 0 \mid c)$ with $c \neq 0$ is the typical signature of an **inconsistent system**.

---

## Step 4: Interpretation in terms of the original equations

Multiply the first equation by $2$:

$$
2x + 4y = 6.
$$

The second equation of the system claims

$$
2x + 4y = 7.
$$

So the same expression $2x + 4y$ would have to equal both $6$ and $7$ at once, which is a contradiction. The left-hand sides of the two equations are proportional (row 2 is $2\times$ row 1 on the left), but the right-hand sides are not ($7 \neq 2\cdot 3$).

---

## Step 5: Rank interpretation

$$
\operatorname{rank}(A) = 1,
\qquad
\operatorname{rank}([A \mid b]) = 2.
$$

Since $\operatorname{rank}(A) \neq \operatorname{rank}([A \mid b])$, the system is inconsistent (Rouché–Capelli theorem).

---

## Step 6: Geometric interpretation

Each equation is a line in the plane:

- $x + 2y = 3$ has slope $-\tfrac{1}{2}$,
- $2x + 4y = 7$, i.e. $x + 2y = \tfrac{7}{2}$, also has slope $-\tfrac{1}{2}$.

The lines are **parallel and distinct**, so they never intersect, and there is no common solution.

---

## Final answer

The system is **inconsistent**: it has **no solution**.

$$
\text{Solution set} = \varnothing
$$