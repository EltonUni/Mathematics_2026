Given:

$$
A(t)=
\begin{pmatrix}
1&t\\
t&1
\end{pmatrix}
$$

We need to find all values of $t$ for which the matrix is invertible and calculate its inverse.

**Step 1: Calculate the determinant.**

For a $2\times2$ matrix:

$$
\det(A)=ad-bc
$$

Therefore:

$$
\det(A(t))=1(1)-t(t)
$$

$$
=1-t^2
$$

A matrix is invertible if its determinant is not zero.

$$
1-t^2\neq0
$$

$$
t^2\neq1
$$

$$
t\neq\pm1
$$

Therefore, the matrix is invertible when:

$$
\boxed{t\in\mathbb{R},\quad t\neq-1,\;t\neq1}
$$

**Step 2: Find the inverse formula.**

Using the inverse formula for a $2\times2$ matrix:

$$
A^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d&-b\\
-c&a
\end{pmatrix}
$$

Substitute the values:

$$
A(t)^{-1}=
\frac{1}{1-t^2}
\begin{pmatrix}
1&-t\\
-t&1
\end{pmatrix}
$$

Therefore:

$$
\boxed{
A(t)^{-1}=
\frac{1}{1-t^2}
\begin{pmatrix}
1&-t\\
-t&1
\end{pmatrix},
\quad t\neq\pm1
}
$$

**Step 3: Explain what happens at the excluded values.**

When $t=1$:

$$
A(1)=
\begin{pmatrix}
1&1\\
1&1
\end{pmatrix}
$$

The two rows are identical, so the determinant is zero.

When $t=-1$:

$$
A(-1)=
\begin{pmatrix}
1&-1\\
-1&1
\end{pmatrix}
$$

The second row is the negative of the first row, so the determinant is also zero.

In both cases, the rows are linearly dependent, meaning the matrix has no inverse.

Additionally, the inverse formula has a denominator of $1-t^2$, which becomes zero at $t=\pm1$. Therefore, the formula is undefined at these values.

**Final Answer:**

$$
\boxed{t\neq\pm1}
$$

$$
\boxed{
A(t)^{-1}=
\frac{1}{1-t^2}
\begin{pmatrix}
1&-t\\
-t&1
\end{pmatrix}
}
$$

At $t=1$ and $t=-1$, the inverse does not exist because the determinant equals zero.