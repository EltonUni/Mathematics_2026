# Exercise 5

## Question

Consider the $3 \times 3$ matrix

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}.$$

1. Compute $\det(A)$ by simplifying the matrix with row operations until it is triangular.
2. For each row operation you use, explain how it affects the determinant (adding a multiple of one row to another, swapping two rows, and multiplying a row by a constant).

## Solution

### Effect of row operations on the determinant

* Adding a multiple of one row to another row does **not** change the determinant.
* Swapping two rows multiplies the determinant by $-1$.
* Multiplying a row by a constant $c$ multiplies the determinant by $c$.

Only the first type of operation is needed here, so the determinant stays the same throughout.

### Row reduction

**Step 1.** $R_2 \to R_2 - 2R_1$ (adding a multiple of a row to another row, so the determinant is unchanged):

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}$$

**Step 2.** $R_3 \to R_3 + R_1$ (again, the determinant is unchanged):

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}$$

**Step 3.** $R_3 \to R_3 + 2R_2$ (again, the determinant is unchanged):

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}$$

**Step 4.** The matrix is now upper triangular, so its determinant is the product of the diagonal entries:

$$\det(A) = 1 \cdot (-3) \cdot (-7) = 21.$$

### Check

Cofactor expansion along the first row of the original matrix:

$$\det(A) = 1\,(1\cdot 2 - 0\cdot 4) - 2\,(2\cdot 2 - 0\cdot(-1)) + 3\,(2\cdot 4 - 1\cdot(-1)) = 2 - 8 + 27 = 21. \checkmark$$

### Answer

$\det(A) = 21$.