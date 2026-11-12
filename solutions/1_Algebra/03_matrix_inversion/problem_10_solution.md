**Given:**

$$
D=
\begin{pmatrix}
2&0&0\\
0&-3&0\\
0&0&5
\end{pmatrix},
\qquad
E=
\begin{pmatrix}
2&0&0\\
0&0&0\\
0&0&5
\end{pmatrix}
$$

**Problem statement:** Decide which of the two diagonal matrices $D$ and $E$ is invertible, and justify your decision. For the invertible matrix, find its inverse **without using Gauss-Jordan elimination**, using instead the special structure of a diagonal matrix. Then check your result by multiplication.

**We need to:**

1. Determine which of the matrices $D$ and $E$ is invertible, and explain why.
2. Find the inverse of the invertible matrix without Gauss-Jordan elimination.
3. Check the result by multiplying the matrix with the inverse you found and confirming that the product equals the identity matrix $I$.

**Step 1: Determine which matrix is invertible.**

A diagonal matrix is invertible if and only if all its diagonal elements are non-zero.

For matrix $D$:

$$
\det(D)=2\cdot(-3)\cdot5=-30
$$

Since:

$$
\det(D)\neq0
$$

Matrix $D$ is invertible.

For matrix $E$:

$$
\det(E)=2\cdot0\cdot5=0
$$

Since:

$$
\det(E)=0
$$

Matrix $E$ is not invertible.

**Step 2: Find the inverse of D.**

To find the inverse of a diagonal matrix, take the reciprocal of each diagonal element.

$$
D^{-1}=
\begin{pmatrix}
\frac12&0&0\\
0&-\frac13&0\\
0&0&\frac15
\end{pmatrix}
$$

Therefore:

$$
\boxed{
D^{-1}=
\begin{pmatrix}
\frac12&0&0\\
0&-\frac13&0\\
0&0&\frac15
\end{pmatrix}
}
$$

**Step 3: Check the result by multiplication.**

Calculate $DD^{-1}$:

$$
DD^{-1}=
\begin{pmatrix}
2&0&0\\
0&-3&0\\
0&0&5
\end{pmatrix}
\begin{pmatrix}
\frac12&0&0\\
0&-\frac13&0\\
0&0&\frac15
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
2\cdot\frac12&0&0\\
0&(-3)\cdot(-\frac13)&0\\
0&0&5\cdot\frac15
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}
=I
$$

The result is correct.

**Final Conclusion:**

- Matrix $D$ is invertible because its determinant is $-30$, which is not zero.
- Matrix $E$ is not invertible because its determinant is zero.
- The inverse of $D$ is:

$$
\boxed{
D^{-1}=
\begin{pmatrix}
\frac12&0&0\\
0&-\frac13&0\\
0&0&\frac15
\end{pmatrix}
}
$$