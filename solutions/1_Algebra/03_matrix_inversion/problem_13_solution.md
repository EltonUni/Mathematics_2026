Given:

$$
S=\begin{pmatrix}
2&0\\
0&1
\end{pmatrix},
\qquad
H=\begin{pmatrix}
1&1\\
0&1
\end{pmatrix}
$$

We need to find $T^{-1}$ in two ways, calculate $H^{-1}S^{-1}$, and explain why the order matters.

### Step 1: Calculate T = HS

$$
T=
\begin{pmatrix}
1&1\\
0&1
\end{pmatrix}
\begin{pmatrix}
2&0\\
0&1
\end{pmatrix}
$$

$$
T=
\begin{pmatrix}
2&1\\
0&1
\end{pmatrix}
$$

### Step 2: Find the inverse of T

First, calculate the determinant:

$$
\det(T)=2(1)-1(0)=2
$$

Using the inverse formula:

$$
T^{-1}=\frac{1}{2}
\begin{pmatrix}
1&-1\\
0&2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
T^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
}
$$

### Step 3: Find the inverse using the product property

We know that:

$$
(HS)^{-1}=S^{-1}H^{-1}
$$

Calculate the individual inverses:

$$
S^{-1}=
\begin{pmatrix}
\frac12&0\\
0&1
\end{pmatrix}
$$

$$
H^{-1}=
\begin{pmatrix}
1&-1\\
0&1
\end{pmatrix}
$$

Multiply them in reversed order:

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12&0\\
0&1
\end{pmatrix}
\begin{pmatrix}
1&-1\\
0&1
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
$$

Therefore:

$$
\boxed{
(HS)^{-1}=S^{-1}H^{-1}
=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
}
$$

### Step 4: Calculate H⁻¹S⁻¹ (incorrect order)

$$
H^{-1}S^{-1}=
\begin{pmatrix}
1&-1\\
0&1
\end{pmatrix}
\begin{pmatrix}
\frac12&0\\
0&1
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
\frac12&-1\\
0&1
\end{pmatrix}
$$

Compare:

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
$$

$$
H^{-1}S^{-1}=
\begin{pmatrix}
\frac12&-1\\
0&1
\end{pmatrix}
$$

Since:

$$
\boxed{H^{-1}S^{-1}\neq S^{-1}H^{-1}}
$$

The incorrect order gives a different matrix.

### Step 5: Explain the rule

The original transformation is:

$$
T=HS
$$

This means:

1. First, apply $S$ (horizontal scaling by 2).
2. Then, apply $H$ (horizontal shear).

To undo these operations, we must reverse their order:

1. First, undo the shear using $H^{-1}$.
2. Then, undo the scaling using $S^{-1}$.

Therefore:

$$
\boxed{(HS)^{-1}=S^{-1}H^{-1}}
$$

**Final Conclusion:**

Both correct methods give the same inverse:

$$
\boxed{
T^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
}
$$

The inverse of a product reverses the multiplication order because we must undo the last operation first.