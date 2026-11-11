**Exercise 10. Detecting Dependence**

$$M = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix}$$

**1. Dependence between the rows.** Let $R_1 = (1, 2, 3)$, $R_2 = (2, 4, 6)$, $R_3 = (0, 1, 5)$. Comparing the first two rows entry by entry,

$$R_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2R_1.$$

Equivalently, $2R_1 - R_2 + 0 \cdot R_3 = 0$ is a nontrivial linear combination of the rows that equals the zero vector, so the rows are linearly dependent.

**2. Why the determinant is zero.** Apply the row operation $R_2 \to R_2 - 2R_1$. Adding a multiple of one row to another does not change the determinant, so

$$\det M = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}.$$

This matrix has a row of zeros. Expanding the determinant along that row gives $0$ (every term contains a factor $0$). Hence

$$\det M = 0.$$

**3. Connection with noninvertibility.** A square matrix is invertible if and only if its determinant is nonzero, which holds if and only if its rows are linearly independent. Here the rows are dependent ($R_2 = 2R_1$), so $\det M = 0$ and $M$ is **not invertible**. Geometrically, the three rows span only a plane instead of all of $\mathbb{R}^3$, so the matrix collapses space onto a lower-dimensional set and cannot be reversed.

**Answer:** Since $R_2 = 2R_1$, the rows are linearly dependent, hence $\det M = 0$ and $M$ is not invertible.