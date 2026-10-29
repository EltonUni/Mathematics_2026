# Exercise 10: Columns of a Matrix Product

**Problem Statement:**
Given the matrices $A$ and $B$:
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}$$
1. Compute $Ab_1$ and $Ab_2$, where $b_1$ and $b_2$ are the column vectors of matrix $B$.
2. Compute the full matrix product $AB$.
3. Compare the columns of $AB$ with $Ab_1$ and $Ab_2$ and explain the relationship between matrix multiplication and column vectors.

**Step-by-Step Explanation:**
1. **Computing $Ab_1$ and $Ab_2$:**
   The matrix $B$ has two columns: $b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}$ and $b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$.
   * Multiply $A$ by $b_1$:
     $$ Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} (1)(1) + (2)(-1) + (0)(3) \\ (0)(1) + (1)(-1) + (1)(3) \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix} $$
   * Multiply $A$ by $b_2$:
     $$ Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (2)(0) + (0)(1) \\ (0)(2) + (1)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix} $$

2. **Computing the full matrix product $AB$:**
   * Column 1 of $AB$: Row 1 dot $b_1 = -1$, Row 2 dot $b_1 = 2$.
   * Column 2 of $AB$: Row 1 dot $b_2 = 2$, Row 2 dot $b_2 = 1$.
   $$ AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix} $$

**Final Result:**
- $Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$, $Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$
- $AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}$
- **Explanation:** Comparing the results, the columns of the matrix product $AB$ are exactly the vectors calculated from $Ab_1$ and $Ab_2$. Matrix multiplication is a compact way of multiplying matrix $A$ by each column vector of $B$ individually and combining them into a single matrix.