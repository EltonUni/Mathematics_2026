# Exercise 3: When Can Matrices Be Multiplied?

**Problem Statement:**
Given the following matrix sizes:
* $A$ is a $2 \times 3$ matrix
* $B$ is a $3 \times 4$ matrix
* $C$ is a $4 \times 2$ matrix
* $D$ is a $2 \times 2$ matrix

Determine whether each of the following matrix products is defined. If a product is defined, state the size of the resulting matrix:
$AB$, $BA$, $BC$, $CB$, $AC$, $CA$, $AD$, $DA$.

**Step-by-Step Explanation:**
For a matrix product $XY$ to be defined, the **inner dimensions** must match. This means the number of columns in the first matrix ($X$) must equal the number of rows in the second matrix ($Y$). If they match, the **outer dimensions** give the size of the resulting matrix.

1. **$AB$**: $A$ is $2 \times 3$, $B$ is $3 \times 4$. The inner dimensions are $3$ and $3$. They match. The outer dimensions are $2$ and $4$.
2. **$BA$**: $B$ is $3 \times 4$, $A$ is $2 \times 3$. The inner dimensions are $4$ and $2$. They do not match.
3. **$BC$**: $B$ is $3 \times 4$, $C$ is $4 \times 2$. Inner dimensions $4$ and $4$ match. Outer dimensions are $3$ and $2$.
4. **$CB$**: $C$ is $4 \times 2$, $B$ is $3 \times 4$. Inner dimensions $2$ and $3$ do not match.
5. **$AC$**: $A$ is $2 \times 3$, $C$ is $4 \times 2$. Inner dimensions $3$ and $4$ do not match.
6. **$CA$**: $C$ is $4 \times 2$, $A$ is $2 \times 3$. Inner dimensions $2$ and $2$ match. Outer dimensions are $4$ and $3$.
7. **$AD$**: $A$ is $2 \times 3$, $D$ is $2 \times 2$. Inner dimensions $3$ and $2$ do not match.
8. **$DA$**: $D$ is $2 \times 2$, $A$ is $2 \times 3$. Inner dimensions $2$ and $2$ match. Outer dimensions are $2$ and $3$.

**Final Result:**
- **$AB$**: Defined, size $2 \times 4$
- **$BA$**: Undefined
- **$BC$**: Defined, size $3 \times 2$
- **$CB$**: Undefined
- **$AC$**: Undefined
- **$CA$**: Defined, size $4 \times 3$
- **$AD$**: Undefined
- **$DA$**: Defined, size $2 \times 3$