Given:

$$
A=\begin{pmatrix}
3&2\\
5&4
\end{pmatrix}
$$

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