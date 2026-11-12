# Exercise 7. Choosing a Method Deliberately

The guiding idea: a method should be judged by **the structure of the matrix** and **the number of right-hand sides**, not by its name. Each method has a cost, and part of that cost may be reusable or wasted.

---

## Case 1: Triangular system

$$
\begin{cases}
2x - y = 3,\\
4y = 8.
\end{cases}
$$

### Chosen method: back substitution

**Why this method.** The coefficient matrix

$$
A = \begin{pmatrix} 2 & -1\\ 0 & 4 \end{pmatrix}
$$

is **upper triangular**. The elimination phase of Gauss is already done: the zero below the diagonal is exactly what elimination would produce. Applying Gaussian elimination or computing $A^{-1}$ would only redo work that the structure has already given us. Back substitution costs about $n^2/2$ operations, far less than inverting.

### Step 1: Solve the last equation

$$
4y = 8 \;\Longrightarrow\; y = 2.
$$

### Step 2: Substitute upward into the first equation

$$
2x - y = 3 \;\Longrightarrow\; 2x - 2 = 3 \;\Longrightarrow\; 2x = 5 \;\Longrightarrow\; x = \tfrac{5}{2}.
$$

### Step 3: Check in both equations

| Equation | Substitution $(x,y) = (\tfrac52, 2)$ | Result |
|---|---|---|
| $2x - y = 3$ | $5 - 2$ | $3$ ✓ |
| $4y = 8$ | $4\cdot 2$ | $8$ ✓ |

**Solution:** $(x,y) = \left(\tfrac{5}{2},\ 2\right)$.

---

## Case 2: Three systems $Ax = b_i$ with the same invertible $A$, and $A^{-1}$ known

### Chosen method: multiply by the known inverse

**Plan.**

1. Do **not** run elimination three times.
2. For each right-hand side compute

$$
x_i = A^{-1} b_i, \qquad i = 1, 2, 3.
$$

Equivalently, collect the right-hand sides in a matrix $B = [\,b_1\ b_2\ b_3\,]$ and compute $X = A^{-1}B$ in one product.

**Why this is the right choice.**

- The expensive part (obtaining $A^{-1}$) is **already paid for**, so inversion is not a cost anymore.
- Each new solution is just one matrix–vector product, about $n^2$ multiplications.
- Elimination, by contrast, would redo about $\tfrac{n^3}{3}$ operations for every $b_i$ if done naively from scratch.

**What is reusable and what is unnecessary.**

| Part of the computation | Status |
|---|---|
| $A^{-1}$ | **Reusable**: one matrix serves all three right-hand sides |
| Row reduction of $A$ | **Unnecessary**: the information it would produce is already contained in $A^{-1}$ |
| Products $A^{-1}b_i$ | The only work that remains, and it is cheap |

**Remark.** If $A^{-1}$ were *not* known, the best way to reuse work would be to eliminate **once** on the augmented matrix $[A \mid b_1\ b_2\ b_3]$ (or to store an LU factorization). The conclusion depends on what has already been computed, not on the name of the method.

---

## Case 3: One $3\times 3$ system, no inverse given, only one solution vector needed

### Chosen method: Gaussian elimination with back substitution

**Plan.**

1. Form the augmented matrix $[A \mid b]$.
2. Use row operations to reach **row echelon form** (upper triangular).
3. Solve by **back substitution**.
4. Check the result in the original equations.

**Why this is the right choice.**

- There is **only one right-hand side**, so any work spent on a method that pays off over many right-hand sides is wasted.
- Computing $A^{-1}$ costs roughly **three times** as much as one elimination (it amounts to solving for $n = 3$ right-hand sides, the columns of the identity), and then still needs a product $A^{-1}b$.
- Gaussian elimination is about $\tfrac{n^3}{3}$ operations, and it also reveals directly whether the system is consistent, which the inverse cannot do if $A$ turns out to be singular.

**What is reusable and what is unnecessary.**

| Part of the computation | Status |
|---|---|
| Forward elimination on $[A \mid b]$ | **Needed**, and it is the main cost |
| Back substitution | **Needed**, cheap ($\approx n^2/2$) |
| Full reduction to RREF (Gauss–Jordan) | **Unnecessary**: extra work above the pivots that back substitution does more cheaply |
| Computing $A^{-1}$ | **Unnecessary**: it solves far more than the single question asked |
| The elimination steps themselves | **Reusable only if** a new right-hand side appears later (then keep them as an LU factorization) |

---

## Summary

| Situation | Method | Reason |
|---|---|---|
| 1. Triangular matrix | Back substitution | Elimination is already built into the structure |
| 2. Same $A$, three $b_i$, $A^{-1}$ known | $x_i = A^{-1}b_i$ | The expensive part is already done and reused |
| 3. One $3\times 3$ system, one $b$, no inverse | Gaussian elimination + back substitution | A single right-hand side does not justify computing $A^{-1}$ |

The general rule: **use the structure that is already there** (triangular form, a known inverse) and **avoid paying for information the question does not need** (an inverse for one right-hand side).