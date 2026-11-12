**Given:**

$$
A=\begin{pmatrix}
1&1&0\\
0&1&1\\
1&0&1
\end{pmatrix}
$$

**Problem statement:** Find the inverse $A^{-1}$ of the $3 \times 3$ matrix $A$ using Gauss-Jordan elimination. Start from the augmented matrix $[A\mid I]$ and apply row operations until the left side becomes the identity matrix $I$. Then read off the inverse from the right side, and check your result by multiplication.

**We need to:**

1. Write the augmented matrix $[A\mid I]$.
2. Apply row operations to transform the left side into $I$, showing the successive augmented matrices.
3. Read the inverse $A^{-1}$ from the right side.
4. Check the result by multiplying $A$ with the inverse you found and confirming that the product equals $I$.

**Step 1: Write the augmented matrix $[A\mid I]$.**

$$
\left[
\begin{array}{ccc|ccc}
1&1&0&1&0&0\\
0&1&1&0&1&0\\
1&0&1&0&0&1
\end{array}
\right]
$$

**Step 2: Eliminate the 1 below the first pivot.**

Apply:

$$
R_3\rightarrow R_3-R_1
$$

$$
\left[
\begin{array}{ccc|ccc}
1&1&0&1&0&0\\
0&1&1&0&1&0\\
0&-1&1&-1&0&1
\end{array}
\right]
$$

**Step 3: Eliminate the -1 in the second column.**

Apply:

$$
R_3\rightarrow R_3+R_2
$$

$$
\left[
\begin{array}{ccc|ccc}
1&1&0&1&0&0\\
0&1&1&0&1&0\\
0&0&2&-1&1&1
\end{array}
\right]
$$

**Step 4: Make the third pivot equal to 1.**

Apply:

$$
R_3\rightarrow \frac{1}{2}R_3
$$

$$
\left[
\begin{array}{ccc|ccc}
1&1&0&1&0&0\\
0&1&1&0&1&0\\
0&0&1&-\frac12&\frac12&\frac12
\end{array}
\right]
$$

**Step 5: Eliminate the 1 above the third pivot.**

Apply:

$$
R_2\rightarrow R_2-R_3
$$

$$
\left[
\begin{array}{ccc|ccc}
1&1&0&1&0&0\\
0&1&0&\frac12&\frac12&-\frac12\\
0&0&1&-\frac12&\frac12&\frac12
\end{array}
\right]
$$

**Step 6: Eliminate the 1 above the second pivot.**

Apply:

$$
R_1\rightarrow R_1-R_2
$$

$$
\left[
\begin{array}{ccc|ccc}
1&0&0&\frac12&-\frac12&\frac12\\
0&1&0&\frac12&\frac12&-\frac12\\
0&0&1&-\frac12&\frac12&\frac12
\end{array}
\right]
$$

**Step 7: Read the inverse matrix.**

The left side is now the identity matrix. Therefore, the right side is the inverse:

$$
\boxed{
A^{-1}=
\begin{pmatrix}
\frac12&-\frac12&\frac12\\
\frac12&\frac12&-\frac12\\
-\frac12&\frac12&\frac12
\end{pmatrix}
}
$$

**Step 8: Check the result by multiplication.**

Calculate $AA^{-1}$:

$$
\begin{aligned}
AA^{-1}
&=
\begin{pmatrix}
1&1&0\\
0&1&1\\
1&0&1
\end{pmatrix}
\begin{pmatrix}
\frac12&-\frac12&\frac12\\
\frac12&\frac12&-\frac12\\
-\frac12&\frac12&\frac12
\end{pmatrix}\\
&=
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}
=I
\end{aligned}
$$

Since $AA^{-1}=I$, the result is correct.

**Final Answer:**

$$
\boxed{
A^{-1}=\frac12
\begin{pmatrix}
1&-1&1\\
1&1&-1\\
-1&1&1
\end{pmatrix}
}
$$