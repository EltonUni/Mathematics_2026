Given:

$$
A=\begin{pmatrix}
1&1\\
0&1
\end{pmatrix},
\qquad
B=\begin{pmatrix}
2&0\\
0&3
\end{pmatrix}
$$

We need to compute $(AB)^{-1}$ and $B^{-1}A^{-1}$ and show that they are equal.

**Step 1: Calculate AB.**

$$
AB=
\begin{pmatrix}
1&1\\
0&1
\end{pmatrix}
\begin{pmatrix}
2&0\\
0&3
\end{pmatrix}
$$

$$
AB=
\begin{pmatrix}
2&3\\
0&3
\end{pmatrix}
$$

**Step 2: Calculate $(AB)^{-1}$.**

Using the inverse formula:

$$
M^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d&-b\\
-c&a
\end{pmatrix}
$$

First, calculate the determinant:

$$
\det(AB)=2(3)-3(0)=6
$$

Now calculate the inverse:

$$
(AB)^{-1}=
\frac{1}{6}
\begin{pmatrix}
3&-3\\
0&2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
(AB)^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&\frac13
\end{pmatrix}
}
$$

**Step 3: Calculate $A^{-1}$ and $B^{-1}$.**

For matrix $A$:

$$
A^{-1}=
\begin{pmatrix}
1&-1\\
0&1
\end{pmatrix}
$$

For matrix $B$:

$$
B^{-1}=
\begin{pmatrix}
\frac12&0\\
0&\frac13
\end{pmatrix}
$$

**Step 4: Calculate $B^{-1}A^{-1}$.**

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12&0\\
0&\frac13
\end{pmatrix}
\begin{pmatrix}
1&-1\\
0&1
\end{pmatrix}
$$

Multiply:

$$
=
\begin{pmatrix}
\frac12&-\frac12\\
0&\frac13
\end{pmatrix}
$$

Therefore:

$$
\boxed{
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&\frac13
\end{pmatrix}
}
$$

**Step 5: Compare the results.**

We obtained:

$$
(AB)^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&\frac13
\end{pmatrix}
$$

And:

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&\frac13
\end{pmatrix}
$$

Therefore:

$$
\boxed{(AB)^{-1}=B^{-1}A^{-1}}
$$

**Step 6: Explain the reversed order.**

When multiplying two matrices, the order matters.

To understand why the inverse reverses the order, consider:

$$
AB
$$

To undo the multiplication, we must first undo $A$ and then undo $B$.

Therefore, the inverse is:

$$
\boxed{(AB)^{-1}=B^{-1}A^{-1}}
$$

**Final Conclusion:**

The results are identical. This confirms the inverse of a product is the product of the inverses in reversed order.