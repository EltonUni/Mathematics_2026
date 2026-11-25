# Exercise 15. Solving a Linear System Using Two Methods

## Given

The coefficient matrix and the right-hand side vector are:

$$
A=\begin{pmatrix}
2&1\\
1&3
\end{pmatrix},
\qquad
b=\begin{pmatrix}
7\\
8
\end{pmatrix}
$$

We need to solve:

$$
Ax=b
$$

## Problem statement

Solve the system using two different methods:

1. **Inverse matrix method:** Calculate \(A^{-1}\) and use \(x=A^{-1}b\) to find the solution.
2. **Gaussian elimination:** Solve the system by writing the augmented matrix and applying elementary row operations.

After solving:

- Compare the essential steps involved in both methods.
- Confirm that both methods produce the same solution.
- Decide which method is simpler for this particular system and explain why.

---

## Method 1: Using the inverse matrix

**Step 1: Find the inverse of \(A\).**

First, calculate the determinant:

$$
\det(A)=2(3)-1(1)=6-1=5
$$

Using the inverse formula:

$$
A^{-1}=\frac{1}{5}
\begin{pmatrix}
3&-1\\
-1&2
\end{pmatrix}
$$

**Step 2: Calculate \(x=A^{-1}b\).**

$$
x=
\frac15
\begin{pmatrix}
3&-1\\
-1&2
\end{pmatrix}
\begin{pmatrix}
7\\
8
\end{pmatrix}
$$

Multiply:

$$
x=\frac15
\begin{pmatrix}
3(7)-1(8)\\
-1(7)+2(8)
\end{pmatrix}
$$

$$
=\frac15
\begin{pmatrix}
21-8\\
-7+16
\end{pmatrix}
$$

$$
=\frac15
\begin{pmatrix}
13\\
9
\end{pmatrix}
$$

Therefore:

$$
\boxed{
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
}
$$

---

## Method 2: Using Gaussian elimination

**Step 1: Write the augmented matrix.**

$$
\left[
\begin{array}{cc|c}
2&1&7\\
1&3&8
\end{array}
\right]
$$

**Step 2: Eliminate the first entry in the second row.**

Apply:

$$
R_2\rightarrow 2R_2-R_1
$$

$$
\left[
\begin{array}{cc|c}
2&1&7\\
0&5&9
\end{array}
\right]
$$

**Step 3: Make the second pivot equal to 1.**

Apply:

$$
R_2\rightarrow\frac15R_2
$$

$$
\left[
\begin{array}{cc|c}
2&1&7\\
0&1&\frac95
\end{array}
\right]
$$

**Step 4: Eliminate the 1 above the second pivot.**

Apply:

$$
R_1\rightarrow R_1-R_2
$$

$$
\left[
\begin{array}{cc|c}
2&0&\frac{26}{5}\\
0&1&\frac95
\end{array}
\right]
$$

**Step 5: Solve for \(x\).**

Divide the first row by 2:

$$
R_1\rightarrow\frac12R_1
$$

$$
\left[
\begin{array}{cc|c}
1&0&\frac{13}{5}\\
0&1&\frac95
\end{array}
\right]
$$

Therefore:

$$
\boxed{
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
}
$$

---

## Step 3: Compare both methods

Both methods give the same solution:

$$
\boxed{
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
}
$$

**Comparison:**

| Method | Essential steps |
|---|---|
| Inverse method | Find determinant, calculate inverse, multiply by \(b\) |
| Gaussian elimination | Create augmented matrix, eliminate entries, solve |

**Which method was simpler?**

In this example, the inverse method was simpler because the matrix is only \(2\times2\), making its determinant and inverse easy to calculate.

For larger systems, Gaussian elimination is generally more practical because calculating a complete inverse requires more work.

---

## Final Answer

The unique solution is:

$$
\boxed{
x_1=\frac{13}{5},
\qquad
x_2=\frac95
}
$$

Both methods produce the same result.