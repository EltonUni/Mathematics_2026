**Given:**

$$
A=\begin{pmatrix}
3&2\\
5&4
\end{pmatrix}
$$

**Problem statement:** Find the inverse $A^{-1}$ of the matrix $A$ using the formula for the inverse of a $2 \times 2$ matrix. Then verify your answer by multiplying $A$ with the inverse you found, that is, by computing $AA^{-1}$ once and checking that it equals the identity matrix $I$.

**We need to:**

1. Write down the inverse formula for a $2 \times 2$ matrix.
2. Calculate the determinant $\det(A)$, which must be nonzero for the inverse to exist.
3. Substitute into the formula to obtain $A^{-1}$.
4. Check the result by calculating $AA^{-1}$ and confirming that it equals $I$.

**Step 1: Use the formula for a $2\times2$ matrix.**

For a matrix:

$$
A=\begin{pmatrix}
a&b\\
c&d
\end{pmatrix}
$$

The inverse is:

$$
A^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d&-b\\
-c&a
\end{pmatrix}
$$

**Step 2: Calculate the determinant.**

$$
\det(A)=ad-bc
$$

$$
=3(4)-2(5)
$$

$$
=12-10=2
$$

**Step 3: Calculate the inverse.**

Substitute the values:

$$
A^{-1}=\frac{1}{2}
\begin{pmatrix}
4&-2\\
-5&3
\end{pmatrix}
$$

Therefore:

$$
\boxed{
A^{-1}=
\begin{pmatrix}
2&-1\\
-\frac{5}{2}&\frac{3}{2}
\end{pmatrix}
}
$$

**Step 4: Check the result by calculating $AA^{-1}$.**

$$
AA^{-1}=
\begin{pmatrix}
3&2\\
5&4
\end{pmatrix}
\begin{pmatrix}
2&-1\\
-\frac52&\frac32
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
6-5&-3+3\\
10-10&-5+6
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
1&0\\
0&1
\end{pmatrix}
=I
$$

**Final Answer:**

$$
\boxed{
A^{-1}=
\begin{pmatrix}
2&-1\\
-\frac52&\frac32
\end{pmatrix}
}
$$

Since $AA^{-1}=I$, our answer is correct.