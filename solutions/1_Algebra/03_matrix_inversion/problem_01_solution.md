**Given:**

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

**Problem statement:** Show that $B$ is the inverse of $A$, that is, $B = A^{-1}$. Do **not** use the inverse formula for a $2 \times 2$ matrix. Instead, compute both products $AB$ and $BA$, and relate the results to the definition of an inverse matrix.

**We need to:**

1. Calculate $AB$.
2. Calculate $BA$.
3. Compare both products with the definition of an inverse: a matrix $B$ is the inverse of $A$ if $AB = BA = I$, where $I$ is the identity matrix. Use this to decide whether $B = A^{-1}$.

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