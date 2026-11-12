# Exercise 15

## Question

Let $A$ and $B$ be invertible $2 \times 2$ matrices with $\det(A) = -2$ and $\det(B) = 3$. The entries of $A$ and $B$ are not given.

1. Compute $\det(B^{-1} A^T B)$ using only properties of determinants, without using the entries of the matrices. Apply the properties in order: multiplicativity, the determinant of the inverse, and the determinant of the transpose.
2. Explain why the factors involving $B$ cancel.

## Solution

### Part 1: Compute $\det(B^{-1} A^T B)$

**Step 1: Multiplicativity.** The determinant of a product is the product of the determinants, $\det(XY) = \det(X) \cdot \det(Y)$. Applying it to the three factors,

$$\det(B^{-1} A^T B) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B).$$

**Step 2: Determinant of the inverse.** From $BB^{-1} = I$ and multiplicativity, $\det(B) \cdot \det(B^{-1}) = \det(I) = 1$, hence

$$\det(B^{-1}) = \frac{1}{\det(B)} = \frac{1}{3}.$$

**Step 3: Determinant of the transpose.** A matrix and its transpose have the same determinant:

$$\det(A^T) = \det(A) = -2.$$

**Step 4: Substitute.**

$$\det(B^{-1} A^T B) = \frac{1}{3} \cdot (-2) \cdot 3 = -2.$$

### Part 2: Why the factors involving $B$ cancel

The determinants are ordinary real numbers, which multiply commutatively, so we may reorder the factors:

$$\det(B^{-1}) \cdot \det(A^T) \cdot \det(B) = \det(A^T) \cdot \underbrace{\det(B^{-1}) \cdot \det(B)}_{=\,1} = \det(A^T).$$

This is the determinant version of the fact that $B^{-1} A^T B$ is similar to $A^T$: conjugating by an invertible matrix does not change the determinant.

Note that the matrices themselves cannot be reordered, since $B^{-1} A^T B \neq A^T$ in general. Only after taking determinants can we rearrange the factors.

### Answer

$\det(B^{-1} A^T B) = -2$.