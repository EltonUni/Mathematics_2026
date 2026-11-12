# Exercise 1

## Question

Consider the two $2 \times 2$ matrices

$$A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.$$

1. Compute the determinant of $A$ and the determinant of $B$.
2. Determine which of the two matrices is invertible, and justify your answer.

## Solution

For a $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is calculated as $\det(M) = ad - bc$.

### Part 1: Determinants

**Matrix $A$:**

$$\det(A) = (3)(4) - (-2)(5)$$
$$\det(A) = 12 - (-10)$$
$$\det(A) = 12 + 10$$
$$\det(A) = 22$$

**Matrix $B$:**

$$\det(B) = (1)(14) - (7)(2)$$
$$\det(B) = 14 - 14$$
$$\det(B) = 0$$

### Part 2: Which matrix is invertible?

A square matrix is invertible if and only if its determinant is non-zero.

* $\det(A) = 22 \neq 0$, so **$A$ is invertible**.
* $\det(B) = 0$, so $B$ is not invertible.

### Answer

$\det(A) = 22$ and $\det(B) = 0$. Only the first matrix, $A$, is invertible, because it is the only one with a non-zero determinant.