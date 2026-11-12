# Exercise 13

## Question

Consider the $3 \times 3$ matrix

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}.$$

1. Compute $\det(A)$ by elimination, that is, by using row operations to reduce $A$ to a triangular matrix.
2. For each row operation you use, state its effect on the determinant.

## Solution

### Effect of row operations on the determinant

* Adding a multiple of one row to another row does **not** change the determinant.
* Swapping two rows multiplies the determinant by $-1$.
* Multiplying a row by $c$ multiplies the determinant by $c$.

Only the first type of operation is needed here, so the determinant stays the same throughout.

### Elimination

**Step 1.** $R_2 \to R_2 - 2R_1$ (determinant unchanged):

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix}$$

**Step 2.** $R_3 \to R_3 - R_1$ (determinant unchanged):

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix}$$

**Step 3.** $R_3 \to R_3 + 2R_2$ (determinant unchanged):

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$

**Step 4.** The matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$\det(A) = 1 \cdot 1 \cdot 1 = 1.$$

### Check

Cofactor expansion along the first row of the original matrix:

$$\det(A) = 1\,(5\cdot 2 - 7\cdot 0) - 2\,(2\cdot 2 - 7\cdot 1) + 3\,(2\cdot 0 - 5\cdot 1) = 10 + 6 - 15 = 1. \checkmark$$

### Answer

$\det(A) = 1$.