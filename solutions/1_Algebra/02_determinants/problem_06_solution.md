# Exercise 6

## Question

Consider the parameter-dependent matrix

$$A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}.$$

1. Compute $\det(A(t))$ as a function of $t$.
2. Find all values of $t$ for which $A(t)$ is not invertible.
3. Explain the connection between these values and a zero determinant.

## Solution

### Part 1: Compute the determinant

For a $2 \times 2$ matrix, $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$, so

$$\det(A(t)) = t \cdot t - 1 \cdot 2 = t^2 - 2.$$

### Part 2: Find where the determinant is zero

$$t^2 - 2 = 0 \iff t^2 = 2 \iff t = \sqrt{2} \ \text{ or } \ t = -\sqrt{2}.$$

### Part 3: Relate to invertibility

A square matrix is invertible if and only if its determinant is nonzero. Therefore $A(t)$ is not invertible exactly when $\det(A(t)) = 0$, that is, when $t = \pm\sqrt{2}$. For every other value of $t$, we have $\det(A(t)) = t^2 - 2 \neq 0$, so $A(t)$ is invertible.

### Why this makes sense

For $t = \sqrt{2}$ the matrix is

$$A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix},$$

and the second row equals $\sqrt{2}$ times the first row: $\sqrt{2}\cdot(\sqrt{2},\ 1) = (2,\ \sqrt{2})$. The rows are linearly dependent, so the matrix is singular.

Similarly, for $t = -\sqrt{2}$ the second row equals $-\sqrt{2}$ times the first row: $-\sqrt{2}\cdot(-\sqrt{2},\ 1) = (2,\ -\sqrt{2})$.

### Answer

$A(t)$ is not invertible exactly for $t = \sqrt{2}$ and $t = -\sqrt{2}$, the two values where $\det(A(t)) = t^2 - 2 = 0$.