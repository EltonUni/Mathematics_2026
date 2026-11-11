Given:

$$
A=\begin{pmatrix}
2&1\\
1&1
\end{pmatrix},
\qquad
B=\begin{pmatrix}
1&-1\\
-1&2
\end{pmatrix}
$$

We need to check whether $B=A^{-1}$ by computing $AB$ and $BA$.

**Step 1: Calculate $AB$.**

$$
AB=
\begin{pmatrix}
2&1\\
1&1
\end{pmatrix}
\begin{pmatrix}
1&-1\\
-1&2
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
2(1)+1(-1)&2(-1)+1(2)\\
1(1)+1(-1)&1(-1)+1(2)
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

**Step 2: Calculate $BA$.**

$$
BA=
\begin{pmatrix}
1&-1\\
-1&2
\end{pmatrix}
\begin{pmatrix}
2&1\\
1&1
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
1(2)+(-1)(1)&1(1)+(-1)(1)\\
(-1)(2)+2(1)&(-1)(1)+2(1)
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

**Step 3: Conclusion.**

According to the definition of an inverse matrix, a matrix $B$ is the inverse of $A$ if:

$$
AB=BA=I
$$

Since both products equal the identity matrix:

$$
\boxed{B=A^{-1}}
$$

Therefore, **$B$ is the inverse of $A$.**