# Exercise 11. A Parameter in a System of Three Equations

## The system

$$
\begin{cases}
x + y + z = 1,\\
x + ty + z = 2,\\
x + y + tz = 3.
\end{cases}
$$

---

## Step 1: Augmented matrix

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1\\
1 & t & 1 & 2\\
1 & 1 & t & 3
\end{array}\right)
$$

The first pivot is $1$, so it never depends on $t$ and no case distinction is needed yet.

---

## Step 2: Eliminate $x$ from rows 2 and 3

- $R_2 \leftarrow R_2 - R_1$: $(0,\ t-1,\ 0,\ 1)$
- $R_3 \leftarrow R_3 - R_1$: $(0,\ 0,\ t-1,\ 2)$

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1\\
0 & t-1 & 0 & 1\\
0 & 0 & t-1 & 2
\end{array}\right)
$$

The matrix is already in row echelon form. The second and third pivots are both $t-1$.

---

## Step 3: Where does a standard step stop being valid?

To continue (back substitution) we must **divide by the pivots** $t-1$:

$$
y = \frac{1}{t-1}, \qquad z = \frac{2}{t-1}.
$$

This division is valid **only if $t \neq 1$**. So $t = 1$ must be analyzed separately.

---

## Step 4: Case $t \neq 1$

Both pivots are nonzero, so there are 3 pivots and $\operatorname{rank}(A) = \operatorname{rank}([A\mid b]) = 3$.

**From row 3:** $z = \dfrac{2}{t-1}$.

**From row 2:** $y = \dfrac{1}{t-1}$.

**From row 1:**
$$
x = 1 - y - z = 1 - \frac{3}{t-1} = \frac{t-1-3}{t-1} = \frac{t-4}{t-1}.
$$

**Unique solution:**

$$
(x,y,z) = \left(\frac{t-4}{t-1},\ \frac{1}{t-1},\ \frac{2}{t-1}\right).
$$

**Check in the original equations (general $t \neq 1$):**

- Eq. 1: $\dfrac{t-4}{t-1} + \dfrac{1}{t-1} + \dfrac{2}{t-1} = \dfrac{t-1}{t-1} = 1$ ✓
- Eq. 2: $\dfrac{t-4}{t-1} + \dfrac{t}{t-1} + \dfrac{2}{t-1} = \dfrac{2t-2}{t-1} = 2$ ✓
- Eq. 3: $\dfrac{t-4}{t-1} + \dfrac{1}{t-1} + \dfrac{2t}{t-1} = \dfrac{3t-3}{t-1} = 3$ ✓

**Numerical example, $t = 2$:** $(x,y,z) = (-2,\ 1,\ 2)$.
$-2+1+2 = 1$ ✓, $-2+2+2 = 2$ ✓, $-2+1+4 = 3$ ✓.

---

## Step 5: Case $t = 1$

Substituting $t = 1$ in the echelon form:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1\\
0 & 0 & 0 & 1\\
0 & 0 & 0 & 2
\end{array}\right)
$$

Row 2 says $0 = 1$ and row 3 says $0 = 2$. Both are **impossible**, so the system is **inconsistent**:

$$
\operatorname{rank}(A) = 1 \neq 2 = \operatorname{rank}([A \mid b]).
$$

**Interpretation in the original equations:** for $t = 1$ the left-hand sides of all three equations are the same expression $x + y + z$, but the right-hand sides are $1$, $2$, $3$. The same quantity cannot equal three different numbers.

---

## Step 6: Determinant check

Since elimination used no row swaps and no scaling,

$$
\det A = 1\cdot(t-1)\cdot(t-1) = (t-1)^2.
$$

- $\det A \neq 0 \iff t \neq 1$ → unique solution.
- $\det A = 0 \iff t = 1$ → no unique solution (here, none at all).

---

## Step 7: Why "infinitely many solutions" never occurs

Infinitely many solutions would need a consistent system with a free variable. At $t = 1$ the system has a free-variable structure ($\operatorname{rank}(A) = 1 < 3$), but it is inconsistent because the right-hand sides $1, 2, 3$ are not compatible. For $t \neq 1$ there are no free variables. So this case never appears.

---

## Summary table

| Value of $t$ | $\operatorname{rank}(A)$ | $\operatorname{rank}([A\mid b])$ | Number of solutions |
|---|---|---|---|
| $t \neq 1$ | $3$ | $3$ | **Exactly one** |
| $t = 1$ | $1$ | $2$ | **None** |
| any $t$ | n/a | n/a | Infinitely many: **never** |

---

## Final answer

- For $t \neq 1$: unique solution
$$
(x,y,z) = \left(\frac{t-4}{t-1},\ \frac{1}{t-1},\ \frac{2}{t-1}\right).
$$
- For $t = 1$: **no solution** (the system is inconsistent).
- The critical value is $t = 1$, where the pivot $t-1$ becomes $0$ and division by it is no longer allowed.