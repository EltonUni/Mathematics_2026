# Exercise 4: Matrix Multiplication and Noncommutativity

**Step-by-Step Explanation:**
Matrix multiplication involves calculating the dot product of the rows of the first matrix with the columns of the second matrix. 

1. **Computing $AB$:**
   * Row 1 of $A$ with Col 1 of $B$: $(1 \times 2) + (2 \times 3) = 2 + 6 = 8$
   * Row 1 of $A$ with Col 2 of $B$: $(1 \times 0) + (2 \times 1) = 0 + 2 = 2$
   * Row 2 of $A$ with Col 1 of $B$: $(0 \times 2) + (1 \times 3) = 0 + 3 = 3$
   * Row 2 of $A$ with Col 2 of $B$: $(0 \times 0) + (1 \times 1) = 0 + 1 = 1$
   $$ AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} $$

2. **Computing $BA$:**
   * Row 1 of $B$ with Col 1 of $A$: $(2 \times 1) + (0 \times 0) = 2 + 0 = 2$
   * Row 1 of $B$ with Col 2 of $A$: $(2 \times 2) + (0 \times 1) = 4 + 0 = 4$
   * Row 2 of $B$ with Col 1 of $A$: $(3 \times 1) + (1 \times 0) = 3 + 0 = 3$
   * Row 2 of $B$ with Col 2 of $A$: $(3 \times 2) + (1 \times 1) = 6 + 1 = 7$
   $$ BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix} $$

3. **Comparing the results:** The matrix $AB$ is completely different from the matrix $BA$. This illustrates noncommutativity: in matrix algebra, the order in which you multiply factors matters.

**Final Result:**
* $AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$
* $BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$
* $AB \neq BA$. This means matrix multiplication is not commutative; reversing the order changes the combination of rows and columns being multiplied, leading to a different result.