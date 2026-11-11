Given:

$$
A=\begin{pmatrix}
1&2\\
0&1
\end{pmatrix},
\qquad
B=\begin{pmatrix}
3&1\\
2&4
\end{pmatrix}
$$

We need to solve:

$$
AX=B
$$

**Step 1: Decide which side to multiply by $A^{-1}$.**

Since $A$ is on the left of $X$, we must multiply both sides by $A^{-1}$ on the **left**.

$$
A^{-1}AX=A^{-1}B
$$

Since $A^{-1}A=I$:

$$
IX=A^{-1}B
$$

Therefore:

$$
X=A^{-1}B
$$

**Step 2: Calculate $A^{-1}$.**

Using the inverse formula:

$$
A^{-1}=\frac{1}{1(1)-2(0)}
\begin{pmatrix}
1&-2\\
0&1
\end{pmatrix}
$$

$$
\boxed{
A^{-1}=
\begin{pmatrix}
1&-2\\
0&1
\end{pmatrix}
}
$$

**Step 3: Calculate X.**

$$
X=
\begin{pmatrix}
1&-2\\
0&1
\end{pmatrix}
\begin{pmatrix}
3&1\\
2&4
\end{pmatrix}
$$

Multiply the matrices:

$$
X=
\begin{pmatrix}
1(3)-2(2)&1(1)-2(4)\\
0(3)+1(2)&0(1)+1(4)
\end{pmatrix}
$$

$$
\boxed{
X=
\begin{pmatrix}
-1&-7\\
2&4
\end{pmatrix}
}
$$

**Step 4: Check the result by calculating AX.**

$$
AX=
\begin{pmatrix}
1&2\\
0&1
\end{pmatrix}
\begin{pmatrix}
-1&-7\\
2&4
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
-1+4&-7+8\\
2&4
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
3&1\\
2&4
\end{pmatrix}
=B
$$

The result matches the original matrix $B$.

**Final Answer:**

$$
\boxed{
X=
\begin{pmatrix}
-1&-7\\
2&4
\end{pmatrix}
}
$$

Since $AX=B$, our solution is correct.