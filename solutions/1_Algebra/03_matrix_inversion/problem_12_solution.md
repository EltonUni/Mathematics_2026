Given:

$$
A^{-1}=
\begin{pmatrix}
2&-1\\
-3&2
\end{pmatrix}
$$

Without finding $A$, calculate the following, and justify each proposed inverse identity using the relevant property:

(a) $(3A)^{-1}$

(b) $(A^T)^{-1}$

(c) $(A^2)^{-1}$

### Step 1: Calculate $(3A)^{-1}$

Use the scalar multiplication property:

$$
(kA)^{-1}=\frac{1}{k}A^{-1}
$$

Therefore:

$$
(3A)^{-1}=\frac13 A^{-1}
$$

Substitute the given matrix:

$$
=\frac13
\begin{pmatrix}
2&-1\\
-3&2
\end{pmatrix}
$$

$$
\boxed{
(3A)^{-1}=
\begin{pmatrix}
\frac23&-\frac13\\
-1&\frac23
\end{pmatrix}
}
$$

**Justification:** Multiply $3A$ by the proposed inverse:

$$
(3A)\left(\frac13A^{-1}\right)=\left(3\cdot\frac13\right)AA^{-1}=I
$$

Since the product is $I$, the matrix $\frac13A^{-1}$ is the inverse of $3A$.

### Step 2: Calculate $(A^T)^{-1}$

Use the transpose property:

$$
(A^T)^{-1}=(A^{-1})^T
$$

Transpose the given inverse matrix by switching rows and columns:

$$
(A^T)^{-1}=
\begin{pmatrix}
2&-3\\
-1&2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
(A^T)^{-1}=
\begin{pmatrix}
2&-3\\
-1&2
\end{pmatrix}
}
$$

**Justification:** Multiply $A^T$ by the proposed inverse and use $(XY)^T=Y^TX^T$:

$$
A^T(A^{-1})^T=(A^{-1}A)^T=I^T=I
$$

Since the product is $I$, the matrix $(A^{-1})^T$ is the inverse of $A^T$.

### Step 3: Calculate $(A^2)^{-1}$

Use the inverse of a product property:

$$
(AB)^{-1}=B^{-1}A^{-1}
$$

Since $A^2=A\cdot A$:

$$
(A^2)^{-1}=A^{-1}A^{-1}
$$

Now multiply the given inverse matrix by itself:

$$
=
\begin{pmatrix}
2&-1\\
-3&2
\end{pmatrix}
\begin{pmatrix}
2&-1\\
-3&2
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
2(2)+(-1)(-3)&2(-1)+(-1)(2)\\
(-3)(2)+2(-3)&(-3)(-1)+2(2)
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
4+3&-2-2\\
-6-6&3+4
\end{pmatrix}
$$

Therefore:

$$
\boxed{
(A^2)^{-1}=
\begin{pmatrix}
7&-4\\
-12&7
\end{pmatrix}
}
$$

**Justification:** Multiply $A^2$ by the proposed inverse:

$$
A^2\left(A^{-1}A^{-1}\right)=A\left(AA^{-1}\right)A^{-1}=A\,I\,A^{-1}=AA^{-1}=I
$$

Since the product is $I$, the matrix $A^{-1}A^{-1}$ is the inverse of $A^2$.

For square matrices, a product equal to $I$ on one side is enough to show that the matrices are inverses of each other.

### Final Answers

$$
\boxed{
(3A)^{-1}=
\begin{pmatrix}
\frac23&-\frac13\\
-1&\frac23
\end{pmatrix}
}
$$

$$
\boxed{
(A^T)^{-1}=
\begin{pmatrix}
2&-3\\
-1&2
\end{pmatrix}
}
$$

$$
\boxed{
(A^2)^{-1}=
\begin{pmatrix}
7&-4\\
-12&7
\end{pmatrix}
}
$$

**Properties used:**

1. Scalar multiplication: $(kA)^{-1}=\frac1k A^{-1}$.
2. Transpose: $(A^T)^{-1}=(A^{-1})^T$.
3. Product: $(AB)^{-1}=B^{-1}A^{-1}$.