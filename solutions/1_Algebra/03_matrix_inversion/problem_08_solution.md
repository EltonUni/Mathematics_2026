Given:

$$
S=\begin{pmatrix}
2&0\\
0&\frac12
\end{pmatrix}
$$

We need to find $S^{-1}$, explain its geometric meaning, and check both transformations on a vector.

**Step 1: Calculate the inverse of S.**

Using the formula for a $2\times2$ matrix:

$$
S^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d&-b\\
-c&a
\end{pmatrix}
$$

Calculate the determinant:

$$
\det(S)=2\cdot\frac12-0=1
$$

Substitute the values:

$$
S^{-1}=
\begin{pmatrix}
\frac12&0\\
0&2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
S^{-1}=
\begin{pmatrix}
\frac12&0\\
0&2
\end{pmatrix}
}
$$

**Step 2: Explain the geometric meaning.**

The original matrix $S$ describes a scaling of the plane:

- The $x$-coordinate is multiplied by $2$ (horizontal stretching).
- The $y$-coordinate is multiplied by $\frac12$ (vertical compression).

The inverse transformation does the opposite:

- The $x$-coordinate is multiplied by $\frac12$ (horizontal compression).
- The $y$-coordinate is multiplied by $2$ (vertical stretching).

In other words, $S^{-1}$ reverses the original scaling and restores the original vector.

**Step 3: Check both transformations using a simple vector.**

Choose:

$$
v=\begin{pmatrix}2\\2\end{pmatrix}
$$

First, apply $S$:

$$
Sv=
\begin{pmatrix}
2&0\\
0&\frac12
\end{pmatrix}
\begin{pmatrix}
2\\2
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
4\\1
\end{pmatrix}
$$

Now apply $S^{-1}$ to the resulting vector:

$$
S^{-1}(Sv)=
\begin{pmatrix}
\frac12&0\\
0&2
\end{pmatrix}
\begin{pmatrix}
4\\1
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
2\\2
\end{pmatrix}
$$

We get our original vector back!

**Step 4: Final conclusion.**

$$
\boxed{S^{-1}S=I}
$$

The inverse transformation undoes the original scaling.

Our final answer is:

$$
\boxed{
S^{-1}=
\begin{pmatrix}
\frac12&0\\
0&2
\end{pmatrix}
}
$$