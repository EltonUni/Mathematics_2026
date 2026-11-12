# Exercise 6. A System with a Parameter: Which Cases Actually Occur?

## The system

$$
\begin{cases}
x + y = 2,\\
ax + ay = 4.
\end{cases}
$$

The unknowns are $x, y$. The parameter $a \in \mathbb{R}$ appears only in the second equation.

---

## Step 1: Write the augmented matrix

$$
[A \mid b] =
\left(\begin{array}{cc|c}
1 & 1 & 2\\
a & a & 4
\end{array}\right)
$$

The first pivot is $1$, so we can eliminate directly with no case distinction on $a$.

---

## Step 2: Eliminate $x$ from row 2

$R_2 \leftarrow R_2 - aR_1$:

- Coefficient of $x$: $a - a\cdot 1 = 0$
- Coefficient of $y$: $a - a\cdot 1 = 0$
- Right-hand side: $4 - 2a$

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & 0 & 4 - 2a
\end{array}\right)
$$

Both coefficients of row 2 vanish **for every value of $a$**. This is the key observation of the exercise. The second row reads

$$
0\cdot x + 0\cdot y = 4 - 2a.
$$

---

## Step 3: Case analysis on $4 - 2a$

### Case 1: $a = 2$

Then $4 - 2a = 0$, and the matrix becomes

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & 0 & 0
\end{array}\right).
$$

The second row is $0 = 0$, which is always true, so there is no contradiction. We have

$$
\operatorname{rank}(A) = \operatorname{rank}([A \mid b]) = 1 < 2 = \text{number of unknowns},
$$

so there is **one free variable** and **infinitely many solutions**.

Let $y = t$, $t \in \mathbb{R}$. Then $x = 2 - t$:

$$
\begin{pmatrix} x \\ y \end{pmatrix}
=
\begin{pmatrix} 2 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} -1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

Check with $t = 1$: $(x,y) = (1,1)$. Then $1 + 1 = 2$ ✓ and $2\cdot 1 + 2\cdot 1 = 4$ ✓.

### Case 2: $a \neq 2$

Then $4 - 2a \neq 0$, and the second row is

$$
(0\ \ 0 \mid c), \qquad c = 4 - 2a \neq 0,
$$

i.e. $0 = c$, which is **impossible**. Hence

$$
\operatorname{rank}(A) = 1 \neq 2 = \operatorname{rank}([A \mid b]),
$$

and the system is **inconsistent**: **no solution**.

This includes $a = 0$, where the second equation is $0 = 4$ (obviously false).

---

## Step 4: Why "exactly one solution" can never occur

A unique solution would require $\operatorname{rank}(A) = 2$, i.e. two pivots. But the two rows of $A$ are

$$
(1,\ 1) \qquad\text{and}\qquad (a,\ a) = a\cdot(1,\ 1),
$$

so row 2 is always a multiple of row 1, and $\operatorname{rank}(A) \le 1$ for every $a$.

Equivalently, the determinant of the coefficient matrix is

$$
\det A = \begin{vmatrix} 1 & 1\\ a & a \end{vmatrix} = 1\cdot a - 1\cdot a = 0
\quad\text{for all } a.
$$

So $A$ is never invertible, and a unique solution is impossible.

Another way to say it: there are $2$ unknowns but at most $1$ pivot, so there is always at least one free variable *if the system is consistent*. A consistent system with a free variable has infinitely many solutions, never exactly one.

---

## Step 5: Geometric interpretation

Each equation is a line in the plane.

- Line 1: $x + y = 2$.
- Line 2: for $a \neq 0$, divide by $a$ to get $x + y = \tfrac{4}{a}$.

Both lines have the same direction (slope $-1$), so they are **parallel**. They either coincide or never meet, and they cannot intersect in exactly one point.

- They **coincide** when $\tfrac{4}{a} = 2$, i.e. $a = 2$ → infinitely many solutions.
- They are **distinct parallel lines** when $a \neq 2$, $a \neq 0$ → no solution.
- For $a = 0$ the second equation becomes $0 = 4$, which no point satisfies → no solution.

---

## Summary table

| Value of $a$ | $\operatorname{rank}(A)$ | $\operatorname{rank}([A\mid b])$ | Number of solutions |
|---|---|---|---|
| $a = 2$ | $1$ | $1$ | **Infinitely many** (one free parameter) |
| $a \neq 2$ | $1$ | $2$ | **None** |
| any $a$ | never $2$ | n/a | **Exactly one: never occurs** |

---

## Final answer

- **Infinitely many solutions** occur **only for $a = 2$**:
  $(x,y) = (2 - t,\ t)$, $t \in \mathbb{R}$.
- **No solution** occurs for **all $a \neq 2$**.
- **Exactly one solution never occurs**, because the second row of $A$ is always $a$ times the first, so $\operatorname{rank}(A) \le 1 < 2$ and $\det A = 0$ for every $a$.