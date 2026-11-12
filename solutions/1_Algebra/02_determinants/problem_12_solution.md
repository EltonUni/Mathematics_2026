# Exercise 12

## Question

Consider the parameter-dependent matrix

$$A(t) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & t \\ 0 & 1 & 1 \end{pmatrix}.$$

1. Before computing the determinant, perform the row operation $R_2 \leftarrow R_2 - 2R_1$.
2. Compute $\det(A(t))$ as a function of $t$.
3. Find all values of $t$ for which $A(t)$ is not invertible.
4. For the special value of $t$ you found, describe the relation between the rows of $A(t)$.

## Solution

### Part 1: Row operation

Perform $R_2 \leftarrow R_2 - 2R_1$. Adding a multiple of one row to another row does not change the determinant, so

$$\det(A(t)) = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & t-6 \\ 0 & 1 & 1 \end{pmatrix}.$$

### Part 2: Compute the determinant

Expand along the first column. The only nonzero entry is the $1$ in the top-left corner, so

$$\det(A(t)) = 1 \cdot \det\begin{pmatrix} 0 & t-6 \\ 1 & 1 \end{pmatrix} = 0 \cdot 1 - (t-6) \cdot 1 = -(t-6) = 6 - t.$$

### Part 3: Find where the matrix is not invertible

A square matrix is not invertible if and only if its determinant is zero:

$$6 - t = 0 \iff t = 6.$$

### Part 4: What happens to the rows for $t = 6$

After the row operation, the second row is $(0, 0, t-6)$. For $t = 6$ it becomes $(0, 0, 0)$, a zero row. Going back, this means that for $t = 6$

$$R_2 - 2R_1 = (0, 0, 0), \quad \text{i.e.} \quad R_2 = 2R_1,$$

since $2R_1 = (2, 4, 6)$ and $R_2 = (2, 4, 6)$ when $t = 6$. So the second row is a multiple of the first row, the rows are linearly dependent, the determinant vanishes, and the matrix is not invertible.

For every $t \neq 6$ the second row after the operation is $(0, 0, t-6) \neq 0$, the rows are independent, and $A(t)$ is invertible.

### Answer

$A(t)$ is not invertible exactly for $t = 6$, where $R_2 = 2R_1$.