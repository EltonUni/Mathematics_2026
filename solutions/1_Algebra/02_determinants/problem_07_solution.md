# Exercise 7

## Question

Let $A$ be a $3 \times 3$ matrix with $\det(A) = -4$.

Without recomputing any determinant from the entries of $A$, use properties of determinants to find each of the following, and justify each answer with the property you use:

1. $\det(2A)$
2. $\det(A^T)$
3. $\det(A^2)$
4. $\det(-A)$

## Solution

### Part 1: $\det(2A)$

Multiplying a matrix by a scalar $c$ multiplies each of its $n$ rows by $c$, and each row scaling multiplies the determinant by $c$. Hence $\det(cA) = c^n \det(A)$. For $n = 3$ and $c = 2$:

$$\det(2A) = 2^3 \det(A) = 8 \cdot (-4) = -32.$$

### Part 2: $\det(A^T)$

A matrix and its transpose have the same determinant: $\det(A^T) = \det(A)$. Therefore

$$\det(A^T) = -4.$$

### Part 3: $\det(A^2)$

The determinant is multiplicative: $\det(AB) = \det(A) \cdot \det(B)$. Therefore

$$\det(A^2) = \det(A \cdot A) = (\det(A))^2 = (-4)^2 = 16.$$

### Part 4: $\det(-A)$

This is the scalar rule with $c = -1$ and $n = 3$:

$$\det(-A) = (-1)^3 \det(A) = -(-4) = 4.$$

### Answer

$$\det(2A) = -32, \qquad \det(A^T) = -4, \qquad \det(A^2) = 16, \qquad \det(-A) = 4.$$