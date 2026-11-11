**Exercise 5. Row Operations**

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$$

We use only operations of the type "add a multiple of one row to another row". These do **not** change the determinant. (For reference: swapping two rows multiplies the determinant by $-1$, and multiplying a row by $c$ multiplies the determinant by $c$. Neither operation is needed here.)

**Step 1.** $R_2 \to R_2 - 2R_1$ (adding a multiple of a row to another row: the determinant is unchanged)

$$\det A = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}$$

**Step 2.** $R_3 \to R_3 + R_1$ (again, the determinant is unchanged)

$$\det A = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}$$

**Step 3.** $R_3 \to R_3 + 2R_2$ (again, the determinant is unchanged)

$$\det A = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}$$

**Step 4.** The matrix is now upper triangular, so its determinant is the product of the diagonal entries:

$$\det A = 1 \cdot (-3) \cdot (-7) = 21.$$

**Answer:** $\det A = 21$.

**Check.** Cofactor expansion along the first row of the original matrix:

$$\det A = 1\,(1\cdot 2 - 0\cdot 4) - 2\,(2\cdot 2 - 0\cdot(-1)) + 3\,(2\cdot 4 - 1\cdot(-1)) = 2 - 8 + 27 = 21. \checkmark$$