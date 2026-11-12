Given:

$$
A^2=I
$$

We need to prove that $A^{-1}=A$ and give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition.

### Step 1: Prove that A⁻¹ = A

We know that:

$$
A^2=I
$$

Rewrite the equation:

$$
A\cdot A=I
$$

According to the definition of an inverse matrix, if:

$$
AB=BA=I
$$

then $B$ is the inverse of $A$.

Since:

$$
A\cdot A=I
$$

it follows that:

$$
\boxed{A^{-1}=A}
$$

### Step 2: Give an example of a 2 × 2 matrix

Choose the matrix:

$$
A=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
$$

This matrix is different from both $I$ and $-I$.

### Step 3: Verify the condition by multiplication

Calculate $A^2$:

$$
A^2=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
$$

Multiply the matrices:

$$
=
\begin{pmatrix}
0(0)+1(1)&0(1)+1(0)\\
1(0)+0(1)&1(1)+0(0)
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

Therefore:

$$
\boxed{A^2=I}
$$

And consequently:

$$
\boxed{
A^{-1}=A=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
}
$$

### Final Conclusion

If a square matrix satisfies $A^2=I$, then it is its own inverse.

Our example confirms this because multiplying the matrix by itself gives the identity matrix.