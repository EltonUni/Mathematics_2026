# Exercise 8

## Question

Let $A$ and $B$ be square matrices of the same size with $\det(A) = 3$ and $\det(B) = -5$.

1. Compute $\det(AB)$.
2. Compute $\det(BA)$.
3. Compute $\det(A^{-1}B)$.
4. Explain why $\det(AB) = \det(BA)$ even though in general $AB \neq BA$.

## Solution

### Part 1: $\det(AB)$

The determinant is multiplicative: $\det(AB) = \det(A) \cdot \det(B)$. Therefore

$$\det(AB) = 3 \cdot (-5) = -15.$$

### Part 2: $\det(BA)$

By the same rule,

$$\det(BA) = \det(B) \cdot \det(A) = (-5) \cdot 3 = -15.$$

### Part 3: $\det(A^{-1}B)$

Since $\det(A) = 3 \neq 0$, the matrix $A$ is invertible, so $A^{-1}$ exists. From $A A^{-1} = I$ we get $\det(A) \cdot \det(A^{-1}) = \det(I) = 1$, hence

$$\det(A^{-1}) = \frac{1}{\det(A)} = \frac{1}{3}.$$

Using multiplicativity again,

$$\det(A^{-1}B) = \det(A^{-1}) \cdot \det(B) = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.$$

### Part 4: Why $\det(AB) = \det(BA)$ even though usually $AB \neq BA$

Matrix multiplication is not commutative, so $AB$ and $BA$ are in general different matrices. However, the determinant of a product is the product of the determinants, and the determinants are just real numbers, which do multiply commutatively:

$$\det(AB) = \det(A) \cdot \det(B) = \det(B) \cdot \det(A) = \det(BA).$$

So the two different matrices $AB$ and $BA$ always have the same determinant, even though their entries may differ.

### Answer

$$\det(AB) = -15, \qquad \det(BA) = -15, \qquad \det(A^{-1}B) = -\frac{5}{3}.$$