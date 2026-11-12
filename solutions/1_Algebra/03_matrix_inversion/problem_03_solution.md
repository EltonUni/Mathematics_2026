**Given:**

$$
A=\begin{pmatrix}
2&4\\
1&2
\end{pmatrix}
$$

**Problem statement:** Explain why the inverse $A^{-1}$ of the matrix $A$ does not exist. Give two different explanations: first, using the determinant (it is zero), and second, using the dependence between the rows of $A$.

**We need to:**

1. Calculate $\det(A)$ and show that it equals zero, which means $A$ cannot be invertible.
2. Find the relation between the rows of $A$ and show that they are linearly dependent, which also means $A$ cannot be invertible.
3. Conclude that both explanations lead to the same result: $A^{-1}$ does not exist.

**Method 1: Using the determinant**

For a $2\times2$ matrix:

$$
\det(A)=ad-bc
$$

Calculate:

$$
\det(A)=2(2)-4(1)
$$

$$
=4-4=0
$$

A matrix has an inverse only if its determinant is not zero.

Since:

$$
\det(A)=0
$$

Therefore:

$$
\boxed{A^{-1}\text{ does not exist}}
$$

**Method 2: Using dependence between the rows**

The rows of matrix $A$ are:

$$
R_1=(2,4)
$$

$$
R_2=(1,2)
$$

Notice that:

$$
R_1=2R_2
$$

This means the two rows are linearly dependent.

A matrix with linearly dependent rows is singular and cannot have an inverse.

Therefore:

$$
\boxed{A^{-1}\text{ does not exist}}
$$

**Final Conclusion:**

Both methods prove that $A$ has no inverse because:

1. Its determinant equals zero.
2. Its rows are linearly dependent.