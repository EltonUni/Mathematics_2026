# Exercise 6: Transpose

**Step-by-Step Explanation:**
1. **Computing Transposes ($A^T$ and $B^T$):**
   The transpose of a matrix, denoted by the superscript $T$, flips the matrix over its main diagonal. Rows become columns, and columns become rows.
   * $A$ is $2 \times 3$, so $A^T$ will be $3 \times 2$:
     Row 1 of $A$ becomes Col 1 of $A^T$. Row 2 of $A$ becomes Col 2 of $A^T$.
   * $B$ is $3 \times 2$, so $B^T$ will be $2 \times 3$:
     Row 1 of $B$ becomes Col 1 of $B^T$, etc.

2. **Computing $AB$:**
   * $A$ ($2 \times 3$) times $B$ ($3 \times 2$) yields a $2 \times 2$ matrix.
   * Entry 1,1: $(1)(1) + (2)(2) + (3)(-1) = 1 + 4 - 3 = 2$
   * Entry 1,2: $(1)(0) + (2)(1) + (3)(3) = 0 + 2 + 9 = 11$
   * Entry 2,1: $(4)(1) + (5)(2) + (6)(-1) = 4 + 10 - 6 = 8$
   * Entry 2,2: $(4)(0) + (5)(1) + (6)(3) = 0 + 5 + 18 = 23$
   $$ AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix} $$

3. **Verifying $(AB)^T = B^T A^T$:**
   * First, take the transpose of $AB$:
     $(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$
   * Next, compute the product $B^T A^T$:
     $B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}$ and $A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}$
     * Entry 1,1: $(1)(1) + (2)(2) + (-1)(3) = 1 + 4 - 3 = 2$
     * Entry 1,2: $(1)(4) + (2)(5) + (-1)(6) = 4 + 10 - 6 = 8$
     * Entry 2,1: $(0)(1) + (1)(2) + (3)(3) = 0 + 2 + 9 = 11$
     * Entry 2,2: $(0)(4) + (1)(5) + (3)(6) = 0 + 5 + 18 = 23$
     $$ B^T A^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix} $$

**Final Result:**
* $A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}$
* $B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}$
* $AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}$
* Verification: Both $(AB)^T$ and $B^T A^T$ result in $\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$, confirming the property.