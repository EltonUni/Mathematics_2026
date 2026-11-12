# Exercise 2

## Question

Consider the $3 \times 3$ matrix

$$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}.$$

1. Compute $\det(A)$ using Sarrus' rule.
2. Verify your result independently by using a property of the determinant (cofactor expansion).

## Solution

### Part 1: Sarrus' rule

To compute the determinant of the $3 \times 3$ matrix $A$ using Sarrus' rule, we write out the matrix and repeat the first two columns to the right.

$$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}$$

$$\begin{matrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{matrix} \quad \begin{matrix} 1 & 2 \\ 0 & 3 \\ 2 & 1 \end{matrix}$$

First, calculate the sum of the products of the main diagonals (top-left to bottom-right):

$$D_1 = (1 \cdot 3 \cdot 5) + (2 \cdot 4 \cdot 2) + (-1 \cdot 0 \cdot 1)$$
$$D_1 = 15 + 16 + 0 = 31$$

Next, calculate the sum of the products of the anti-diagonals (bottom-left to top-right):

$$D_2 = (2 \cdot 3 \cdot (-1)) + (1 \cdot 4 \cdot 1) + (5 \cdot 0 \cdot 2)$$
$$D_2 = -6 + 4 + 0 = -2$$

Subtract $D_2$ from $D_1$ to find the determinant:

$$\det(A) = D_1 - D_2 = 31 - (-2) = 33$$

### Part 2: Independent check (cofactor expansion)

We verify this result by performing a cofactor expansion (Laplace expansion) along the first column. This property of the determinant lets us break it down into smaller $2 \times 2$ determinants. The first column is a convenient choice because it contains a zero.

$$\det(A) = 1 \cdot \det\begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix} - 0 \cdot \det\begin{pmatrix} 2 & -1 \\ 1 & 5 \end{pmatrix} + 2 \cdot \det\begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix}$$

$$\det(A) = 1 \cdot (3 \cdot 5 - 4 \cdot 1) - 0 + 2 \cdot (2 \cdot 4 - (-1) \cdot 3)$$
$$\det(A) = 1 \cdot (15 - 4) + 2 \cdot (8 + 3)$$
$$\det(A) = 1 \cdot 11 + 2 \cdot 11$$
$$\det(A) = 11 + 22 = 33$$

### Answer

Both methods give the same result, so $\det(A) = 33$.