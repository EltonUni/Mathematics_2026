**Exercise 11. Shortening the Calculation with Row Operations**

$$M = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}$$

**Which operations do not change the determinant.** Adding a multiple of one row to another row leaves the determinant unchanged. (For comparison: swapping two rows multiplies it by $-1$, and multiplying a row by $c$ multiplies it by $c$. We use neither here.)

**Step 1.** $R_2 \to R_2 - R_1$ (determinant unchanged)

$$\det M = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 4 & 6 \end{pmatrix}$$

**Step 2.** $R_3 \to R_3 - R_1$ (determinant unchanged)

$$\det M = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}$$

**Step 3.** $R_3 \to R_3 - 2R_2$ (determinant unchanged)

$$\det M = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$

**Step 4.** The matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$\det M = 1 \cdot 1 \cdot 1 = 1.$$

**Answer:** $\det M = 1$.

**Check.** Cofactor expansion along the first row of the original matrix:

$$\det M = 1\,(3\cdot 6 - 4\cdot 4) - 2\,(1\cdot 6 - 4\cdot 1) + 3\,(1\cdot 4 - 3\cdot 1) = 2 - 4 + 3 = 1. \checkmark$$