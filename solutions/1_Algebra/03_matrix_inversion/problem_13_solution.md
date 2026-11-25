# Exercise 13. Inverse of a Product of Matrices

## Given

The following matrices are given:

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

## Problem statement

Let $T=HS$.

Find $T^{-1}$ in two different ways:

1. Calculate $T$ first and then find its inverse directly using the inverse formula.
2. Calculate the inverses of $H$ and $S$ separately and use the product property $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results of both methods and show that they give the same inverse.

Additionally, calculate $H^{-1}S^{-1}$ as a wrong-order check, compare it with $S^{-1}H^{-1}$, and explain why the order of multiplication matters when finding the inverse of a product.

---

## Step 1: Calculate $T=HS$

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

---

## Step 2: Find the inverse of $T$ directly

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

---

## Step 3: Find the inverse using the product property

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

---

## Step 4: Compare the two inverse calculations

From Step 2, using the direct method:

$$
T^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
$$

From Step 3, using the product property:

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12&-\frac12\\
0&1
\end{pmatrix}
$$

Both methods give exactly the same result:

$$
\boxed{T^{-1}=S^{-1}H^{-1}}
$$

This confirms the inverse of a product property.

---

## Step 5: Calculate $H^{-1}S^{-1}$ (wrong-order check)

Now multiply the inverses in the opposite order:

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

---

## Step 6: Explain why the order matters

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

The inverse of a product reverses the multiplication order because we must undo the last operation first.

---

## Final Conclusion

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

The wrong-order calculation gives a different result:

$$
H^{-1}S^{-1}=
\begin{pmatrix}
\frac12&-1\\
0&1
\end{pmatrix}
$$

This demonstrates that matrix multiplication order matters and that the inverse of a product must be calculated in reverse order:

$$
\boxed{(AB)^{-1}=B^{-1}A^{-1}}
$$