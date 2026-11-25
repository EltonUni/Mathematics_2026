# Exercise 14. A Matrix That Is Its Own Inverse

## Given

$$
A^2=I
$$

## Problem statement

Given that $A^2=I$:

1. Prove that $A^{-1}=A$.
2. Give an example of a $2\times2$ matrix different from both $I$ and $-I$ that satisfies this condition.
3. Verify the example by explicitly multiplying the matrix by itself and showing that the result is the identity matrix.
4. Use the multiplication verification to confirm that the example is its own inverse.

---

## Step 1: Prove that $A^{-1}=A$

We know that:

$$
A^2=I
$$

Rewrite the equation:

$$
A\cdot A=I
$$

According to the definition of an inverse matrix, if a square matrix $B$ satisfies:

$$
AB=BA=I
$$

then $B$ is the inverse of $A$.

Setting $B=A$, since:

$$
A\cdot A=I
$$

it follows directly that:

$$
\boxed{A^{-1}=A}
$$

---

## Step 2: Give an example of a $2\times2$ matrix

Choose the permutation (reflection) matrix:

$$
A=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
$$

This matrix is different from both $I=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ and $-I=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}$.

---

## Step 3: Verify the condition by multiplication

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

---

## Step 4: Confirm that the example is its own inverse

From Step 3, multiplying $A$ by itself on either side gives the identity matrix:

$$
A\cdot A = A^2 = I.
$$

Because $A\cdot A = I$ matches the inverse condition $AB = BA = I$ with $B = A$, the matrix $A$ is its own inverse:

$$
\boxed{
A^{-1}=A=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
}
$$

---

## Final Conclusion

If a square matrix satisfies $A^2=I$, then it is its own inverse ($A^{-1}=A$).

Our example $A=\begin{pmatrix}0&1\\1&0\end{pmatrix}$ is distinct from $I$ and $-I$, and multiplying it by itself gives $A^2=I$, confirming that $A^{-1}=A$.