# Exercise 15. Classifying Three Systems

The goal is to eliminate **only as far as needed** to see the type. The decisive question is always: after elimination, is there a contradictory row $(0\ \ 0 \mid c)$ with $c \neq 0$, and how many pivots are there compared with the number of unknowns?

---

## System 1

$$
\begin{cases}
x + y = 2,\\
x - y = 0.
\end{cases}
$$

### Elimination

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
1 & -1 & 0
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & -2 & -2
\end{array}\right)
$$

### Classification

- Two pivots (in columns 1 and 2), no zero row, no contradiction.
- $\operatorname{rank}(A) = \operatorname{rank}([A\mid b]) = 2 = n$.

**Type: exactly one solution.**

For completeness: $-2y = -2 \Rightarrow y = 1$, then $x = 2 - 1 = 1$, so $(x,y) = (1,1)$.
Check: $1 + 1 = 2$ ✓, $1 - 1 = 0$ ✓.

**Geometric view:** the slopes are $-1$ and $+1$, so the lines are not parallel and meet in one point.

---

## System 2

$$
\begin{cases}
x + y = 2,\\
2x + 2y = 4.
\end{cases}
$$

### Elimination

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
2 & 2 & 4
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & 0 & 0
\end{array}\right)
$$

### Classification

- The second row is $0 = 0$: always true, no contradiction.
- Only one pivot, so $\operatorname{rank}(A) = \operatorname{rank}([A\mid b]) = 1 < 2 = n$.
- One free variable.

**Type: infinitely many solutions.**

Let $y = t$. Then $x = 2 - t$:

$$
\begin{pmatrix} x \\ y \end{pmatrix}
= \begin{pmatrix} 2 \\ 0 \end{pmatrix} + t\begin{pmatrix} -1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

Check with $t = 1$: $(1,1)$ gives $2$ ✓ and $4$ ✓.

**Geometric view:** the second equation is $2\times$ the first, so both describe the **same line**.

---

## System 3

$$
\begin{cases}
x + y = 2,\\
2x + 2y = 5.
\end{cases}
$$

### Elimination

$$
\left(\begin{array}{cc|c}
1 & 1 & 2\\
2 & 2 & 5
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2\\
0 & 0 & 1
\end{array}\right)
$$

### Classification

- The second row reads $0\cdot x + 0\cdot y = 1$, i.e. $0 = 1$, which is **impossible**.
- $\operatorname{rank}(A) = 1 \neq 2 = \operatorname{rank}([A\mid b])$.

**Type: no solution (inconsistent).**

**Geometric view:** the lines $x + y = 2$ and $x + y = \tfrac52$ have the same slope but different intercepts, so they are **parallel and distinct**.

---

## Comparison: Systems 2 and 3

Both have the same coefficient matrix with proportional rows, $(2,2) = 2\cdot(1,1)$. The only difference is the right-hand side:

- System 2: $4 = 2\cdot 2$ → compatible → infinitely many solutions.
- System 3: $5 \neq 2\cdot 2$ → incompatible → no solution.

So the **left-hand side** shows that a free variable is possible, and the **right-hand side** decides whether the system is actually consistent.

---

## Summary table

| System | Row after elimination | $\operatorname{rank}(A)$ | $\operatorname{rank}([A\mid b])$ | $n$ | Type |
|---|---|---|---|---|---|
| 1 | $(0\ \ -2 \mid -2)$ | $2$ | $2$ | $2$ | **One solution** $(1,1)$ |
| 2 | $(0\ \ 0 \mid 0)$ | $1$ | $1$ | $2$ | **Infinitely many** |
| 3 | $(0\ \ 0 \mid 1)$ | $1$ | $2$ | $2$ | **No solution** |

## Decision rule used

1. A row $(0\ \cdots\ 0 \mid c)$ with $c \neq 0$ → **no solution**.
2. Otherwise, if the number of pivots equals the number of unknowns → **exactly one solution**.
3. Otherwise (fewer pivots than unknowns) → **infinitely many solutions**.