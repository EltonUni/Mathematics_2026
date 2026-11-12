# Exercise 4

## Question

Consider the $3 \times 3$ matrix

$$M = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.$$

1. Compute $\det(M)$ **without using cofactor expansion** to obtain the value. Instead, use the rule for triangular matrices.
2. State the general rule for the determinant of a triangular matrix (upper or lower).
3. Explain why the rule works, using this matrix as the example.

## Solution

### Part 1: The rule

For any triangular matrix $T$ (upper or lower), the determinant equals the product of the entries on the main diagonal:

$$\det(T) = t_{11} \cdot t_{22} \cdots t_{nn}$$

### Part 2: Applying the rule

The given matrix

$$M = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}$$

is upper triangular, since all entries below the main diagonal are zero. Its diagonal entries are $2$, $-3$ and $7$, so

$$\det(M) = 2 \cdot (-3) \cdot 7 = -42.$$

### Part 3: Why the rule works

Expand along the first column of $M$. The only nonzero entry in that column is $2$, so

$$\det(M) = 2 \cdot \det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}.$$

The remaining $2 \times 2$ matrix is again upper triangular, and expanding along its first column gives

$$\det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = (-3)(7) - 5 \cdot 0 = -21.$$

Therefore $\det(M) = 2 \cdot (-21) = -42$.

The same argument works for any size: expanding along the first column of an upper triangular matrix leaves only the top-left entry times a smaller triangular determinant, and repeating this multiplies all the diagonal entries together. For a lower triangular matrix, expand along the first row instead.

### Answer

$\det(M) = -42$.