# Exercise 3

## Question

Consider the $3 \times 3$ matrix

$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}.$$

1. Compute $\det(A)$.
2. Form the matrix $B$ by swapping the first and second rows of $A$:
$$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}.$$
3. Using a property of determinants, predict $\det(B)$.
4. Verify your prediction by calculating $\det(B)$ directly.

## Solution

### Part 1: Compute $\det(A)$

We use cofactor expansion along the first row:

$$\det(A) = 1 \cdot \det\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} - 2 \cdot \det\begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} + 0 \cdot \det\begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix}$$

$$\det(A) = 1 \cdot (3 \cdot 1 - 1 \cdot 1) - 2 \cdot (0 \cdot 1 - 1 \cdot 2) + 0$$
$$\det(A) = 1 \cdot (3 - 1) - 2 \cdot (0 - 2)$$
$$\det(A) = 1 \cdot 2 - 2 \cdot (-2)$$
$$\det(A) = 2 + 4 = 6$$

### Part 2: Form matrix $B$

Matrix $B$ is formed by swapping the first and second rows of $A$:

$$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}$$

### Part 3: Predict $\det(B)$ using a determinant property

A fundamental property of determinants states that swapping any two rows of a square matrix multiplies its determinant by $-1$.

Since $B$ is obtained from $A$ by swapping one pair of rows, we predict:

$$\det(B) = -\det(A) = -6$$

### Part 4: Verify the prediction by calculation

We compute $\det(B)$ directly using cofactor expansion along the first row:

$$\det(B) = 0 \cdot \det\begin{pmatrix} 2 & 0 \\ 1 & 1 \end{pmatrix} - 3 \cdot \det\begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} + 1 \cdot \det\begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}$$

$$\det(B) = 0 - 3 \cdot (1 \cdot 1 - 0 \cdot 2) + 1 \cdot (1 \cdot 1 - 2 \cdot 2)$$
$$\det(B) = -3 \cdot (1 - 0) + 1 \cdot (1 - 4)$$
$$\det(B) = -3 \cdot 1 + 1 \cdot (-3)$$
$$\det(B) = -3 - 3 = -6$$

### Answer

$\det(A) = 6$. Swapping two rows gives $B$, and the property predicts $\det(B) = -6$. The direct calculation also gives $-6$, which confirms the prediction.