Given:

$$
Ax=b
$$

where

$$
A=\begin{pmatrix}
2&1\\
1&3
\end{pmatrix},
\qquad
b=\begin{pmatrix}
5\\
7
\end{pmatrix}
$$

We use the formula:

$$
x=A^{-1}b
$$

**Step 1: Find the inverse of A.**

First, calculate the determinant:

$$
\det(A)=2(3)-1(1)
$$

$$
=6-1=5
$$

Using the inverse formula:

$$
A^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d&-b\\
-c&a
\end{pmatrix}
$$

Substitute the values:

$$
A^{-1}=\frac{1}{5}
\begin{pmatrix}
3&-1\\
-1&2
\end{pmatrix}
$$

**Step 2: Calculate x = A⁻¹b.**

$$
x=
\frac{1}{5}
\begin{pmatrix}
3&-1\\
-1&2
\end{pmatrix}
\begin{pmatrix}
5\\
7
\end{pmatrix}
$$

Multiply the matrices:

$$
x=\frac{1}{5}
\begin{pmatrix}
3(5)-1(7)\\
-1(5)+2(7)
\end{pmatrix}
$$

$$
=\frac{1}{5}
\begin{pmatrix}
15-7\\
-5+14
\end{pmatrix}
$$

$$
=\frac{1}{5}
\begin{pmatrix}
8\\
9
\end{pmatrix}
$$

Therefore:

$$
\boxed{
x=\begin{pmatrix}
\frac85\\
\frac95
\end{pmatrix}
}
$$

**Step 3: Check the result by substitution.**

Substitute the values into the original equation:

$$
Ax=
\begin{pmatrix}
2&1\\
1&3
\end{pmatrix}
\begin{pmatrix}
\frac85\\
\frac95
\end{pmatrix}
$$

Multiply:

$$
=
\begin{pmatrix}
\frac{16}{5}+\frac95\\
\frac85+\frac{27}{5}
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
\frac{25}{5}\\
\frac{35}{5}
\end{pmatrix}
=
\begin{pmatrix}
5\\
7
\end{pmatrix}
$$

Since:

$$
Ax=b
$$

The solution is correct.

**Final Answer:**

$$
\boxed{
x=\begin{pmatrix}
\frac85\\
\frac95
\end{pmatrix}
}
$$