**Exercise 13. Determinant by Elimination**

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}$$

We use only operations of the type "add a multiple of one row to another row". These do not change the determinant. (For comparison: swapping two rows multiplies the determinant by $-1$, and multiplying a row by $c$ multiplies it by $c$. Neither is needed here.)

**Step 1.** $R_2 \to R_2 - 2R_1$ (determinant unchanged)

$$\det A = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix}$$

**Step 2.** $R_3 \to R_3 - R_1$ (determinant unchanged)

$$\det A = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix}$$

**Step 3.** $R_3 \to R_3 + 2R_2$ (determinant unchanged)

$$\det A = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$

**Step 4.** The matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$\det A = 1 \cdot 1 \cdot 1 = 1.$$

**Answer:** $\det A = 1$.

**Check.** Cofactor expansion along the first row of the original matrix:

$$\det A = 1\,(5\cdot 2 - 7\cdot 0) - 2\,(2\cdot 2 - 7\cdot 1) + 3\,(2\cdot 0 - 5\cdot 1) = 10 + 6 - 15 = 1. \checkmark$$