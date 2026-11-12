# Exercise 12. Homogeneous System

## The system

$$
\begin{cases}
x + 2y - z = 0,\\
2x + 4y - 2z = 0,\\
x - y + 2z = 0.
\end{cases}
$$

All right-hand sides are $0$, so this is a **homogeneous system** $Ax = \mathbf{0}$.

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

- $R_2 \leftarrow R_2 - 2R_1$: $(0,\,0,\,0,\,0)$
- $R_3 \leftarrow R_3 - R_1$: $(0,\,-3,\,3,\,0)$

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

Swap $R_2 \leftrightarrow R_3$, then $R_2 \leftarrow -\tfrac{1}{3}R_2$:

$$
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 0\\
0 & 1 & -1 & 0\\
0 & 0 & 0 & 0
\end{array}\right)
$$

This is row echelon form with **2 pivots** (columns 1 and 2).

---

## Step 4: Reduced row echelon form

$R_1 \leftarrow R_1 - 2R_2$:

$$
\left(\begin{array}{ccc|c}
1 & 0 & 1 & 0\\
0 & 1 & -1 & 0\\
0 & 0 & 0 & 0
\end{array}\right)
$$

---

## Step 5: Basic and free variables

- Pivot columns: $x$ and $y$ → **basic variables**.
- No pivot in column 3 → $z$ is a **free variable**.

$$
\operatorname{rank}(A) = 2, \qquad n = 3, \qquad \text{free variables} = 3 - 2 = 1.
$$

---

## Step 6: Read the solution

The RREF gives

$$
\begin{cases}
x + z = 0,\\
y - z = 0.
\end{cases}
\quad\Longrightarrow\quad
x = -z,\quad y = z.
$$

Set $z = t$, $t \in \mathbb{R}$:

$$
x = -t, \qquad y = t, \qquad z = t.
$$

**Parametric (vector) form:**

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
= t \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

Interpretation: the solution set is a **line through the origin** in $\mathbb{R}^3$ with direction vector $(-1,1,1)$.

---

## Step 7: Verification (for any $t$)

With $(x,y,z) = (-t,\,t,\,t)$:

- $x + 2y - z = -t + 2t - t = 0$ ✓
- $2x + 4y - 2z = -2t + 4t - 2t = 0$ ✓
- $x - y + 2z = -t - t + 2t = 0$ ✓

Example with $t = 1$: $(-1,1,1)$ gives $-1+2-1 = 0$, $-2+4-2 = 0$, $-1-1+2 = 0$ ✓.

---

## Step 8: Why $(0,0,0)$ always solves a homogeneous system

For any homogeneous system $Ax = \mathbf{0}$, put $x = \mathbf{0}$. Every equation has the form

$$
a_{i1}\cdot 0 + a_{i2}\cdot 0 + \dots + a_{in}\cdot 0 = 0,
$$

which is true. In matrix language, $A\mathbf{0} = \mathbf{0}$ for every matrix $A$.

Consequences:

- A homogeneous system is **never inconsistent**: $\operatorname{rank}(A) = \operatorname{rank}([A \mid \mathbf{0}])$ always, since a zero column cannot create a contradictory row $(0\ \cdots\ 0 \mid c)$ with $c \neq 0$.
- Only two cases are possible: **only the trivial solution** (when $\operatorname{rank}(A) = n$), or **infinitely many solutions** (when $\operatorname{rank}(A) < n$).
- Here $\operatorname{rank}(A) = 2 < 3$, so there are non-trivial solutions. The trivial solution $(0,0,0)$ corresponds to $t = 0$.

---

## Final answer

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
= t\begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

The system has infinitely many solutions (one free variable, $z$), and $(0,0,0)$ is always among them because $A\mathbf{0} = \mathbf{0}$.