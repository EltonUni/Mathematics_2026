# Exercise 5: Matrix Times Vector

**Problem Statement:**
Given the matrix $A$ and the vector $x$:
$$A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \quad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$$
Compute the product $Ax$ using standard matrix-vector multiplication, and then show how this product can be computed as a linear combination of the columns of $A$.

**Step-by-Step Explanation:**
1. **Standard Matrix-Vector Multiplication ($Ax$):**
   We treat $x$ as a $2 \times 1$ matrix and compute the dot product of the rows of $A$ with the vector $x$.
   * Row 1 dot $x$: $(2 \times 4) + (-1 \times 2) = 8 - 2 = 6$
   * Row 2 dot $x$: $(1 \times 4) + (3 \times 2) = 4 + 6 = 10$
   Resulting vector: $\begin{pmatrix} 6 \\ 10 \end{pmatrix}$

2. **Linear Combination Perspective:**
   Multiplying a matrix by a vector can be viewed as scaling the columns of the matrix by the entries in the vector, and then adding those scaled columns together.
   * The first column of $A$ is $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$. The first entry of $x$ is $4$.
   * The second column of $A$ is $\begin{pmatrix} -1 \\ 3 \end{pmatrix}$. The second entry of $x$ is $2$.
   * Calculation: $4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix}$
   * Multiply scalars: $\begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix}$
   * Add vectors: $\begin{pmatrix} 8-2 \\ 4+6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$

**Final Result:**
- $Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$
- As a linear combination: $4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$