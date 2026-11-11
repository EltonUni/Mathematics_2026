Given:

$$
A=\begin{pmatrix}
1&2\\
3&5
\end{pmatrix}
$$

**Step 1: Write the augmented matrix $[A\mid I]$.**

$$
\left[
\begin{array}{cc|cc}
1&2&1&0\\
3&5&0&1
\end{array}
\right]
$$

Our goal is to transform the left side into the identity matrix.

**Step 2: Eliminate the 3 below the first pivot.**

Apply the row operation:

$$
R_2\rightarrow R_2-3R_1
$$

$$
\left[
\begin{array}{cc|cc}
1&2&1&0\\
0&-1&-3&1
\end{array}
\right]
$$

**Step 3: Make the second pivot equal to 1.**

Apply:

$$
R_2\rightarrow -R_2
$$

$$
\left[
\begin{array}{cc|cc}
1&2&1&0\\
0&1&3&-1
\end{array}
\right]
$$

**Step 4: Eliminate the 2 above the second pivot.**

Apply:

$$
R_1\rightarrow R_1-2R_2
$$

$$
\left[
\begin{array}{cc|cc}
1&0&-5&2\\
0&1&3&-1
\end{array}
\right]
$$

**Step 5: Read the inverse matrix.**

The left side is now the identity matrix. Therefore, the right side is the inverse:

$$
\boxed{
A^{-1}=
\begin{pmatrix}
-5&2\\
3&-1
\end{pmatrix}
}
$$

**Why does this method work?**

Every elementary row operation is equivalent to multiplying the matrix on the left by an elementary matrix.

If we transform $A$ into $I$, we obtain:

$$
EA=I
$$

Therefore:

$$
E=A^{-1}
$$

The same operations applied to the identity matrix produce $E$, which is why the right side becomes the inverse of $A$.

**Final Answer:**

$$
\boxed{
A^{-1}=
\begin{pmatrix}
-5&2\\
3&-1
\end{pmatrix}
}
$$