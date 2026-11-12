# Exercise 11

## Question

Consider the $3 \times 3$ matrix

$$M = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}.$$

1. Compute $\det(M)$ by using row operations that produce zeros below the diagonal, shortening the calculation.
2. State which row operations preserve the determinant and which ones change it.

## Solution

### Which operations do not change the determinant

Adding a multiple of one row to another row leaves the determinant unchanged. For comparison:

* Swapping two rows multiplies the determinant by $-1$.
* Multiplying a row by $c$ multiplies the determinant by $c$.

We use neither of these here, only the first type of operation.

### Row reduction

**Step 1.** $R_2 \to R_2 - R_1$ (determinant unchanged):

$$\det(M) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 4 & 6 \end{pmatrix}$$

**Step 2.** $R_3 \to R_3 - R_1$ (determinant unchanged):

$$\det(M) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}$$

**Step 3.** $R_3 \to R_3 - 2R_2$ (determinant unchanged):

$$\det(M) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$

**Step 4.** The matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$\det(M) = 1 \cdot 1 \cdot 1 = 1.$$

### Check

Cofactor expansion along the first row of the original matrix:

$$\det(M) = 1\,(3\cdot 6 - 4\cdot 4) - 2\,(1\cdot 6 - 4\cdot 1) + 3\,(1\cdot 4 - 3\cdot 1) = 2 - 4 + 3 = 1. \checkmark$$

### Answer

$\det(M) = 1$.