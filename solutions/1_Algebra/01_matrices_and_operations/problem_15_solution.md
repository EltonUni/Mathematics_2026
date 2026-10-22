# Exercise 15: Associativity of Multiplication and Different Calculation Paths

**Step-by-Step Explanation:**
Matrix multiplication is associative, meaning $(AB)C = A(BC)$. We will calculate both paths to prove they yield the same result.

**Path 1: Calculate $(AB)C$**
1. Compute the inner parentheses first: $AB$. ($A$ is $2 \times 3$, $B$ is $3 \times 2 \implies AB$ is $2 \times 2$)
   $$ AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} $$
   * Row 1 dot columns: $(1)(1)+(2)(2)+(0)(-1) = 5$, and $(1)(0)+(2)(1)+(0)(3) = 2$
   * Row 2 dot columns: $(0)(1)+(1)(2)+(1)(-1) = 1$, and $(0)(0)+(1)(1)+(1)(3) = 4$
   $$ AB = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} $$
2. Multiply this result by $C$. ($AB$ is $2 \times 2$, $C$ is $2 \times 2 \implies$ result is $2 \times 2$)
   $$ (AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} $$
   * Row 1 dot columns: $10 + 0 = 10$, and $5 - 2 = 3$
   * Row 2 dot columns: $2 + 0 = 2$, and $1 - 4 = -3$
   $$ (AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} $$

**Path 2: Calculate $A(BC)$**
1. Compute the inner parentheses first: $BC$. ($B$ is $3 \times 2$, $C$ is $2 \times 2 \implies BC$ is $3 \times 2$)
   $$ BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 2+0 & 1+0 \\ 4+0 & 2-1 \\ -2+0 & -1-3 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} $$
2. Multiply $A$ by this result. ($A$ is $2 \times 3$, $BC$ is $3 \times 2 \implies$ result is $2 \times 2$)
   $$ A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} $$
   * Row 1 dot columns: $2+8+0 = 10$, and $1+2+0 = 3$
   * Row 2 dot columns: $0+4-2 = 2$, and $0+1-4 = -3$
   $$ A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} $$

**Final Result:**
* Path 1: $(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$
* Path 2: $A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$
* **Explanation:** Both paths lead to the exact same final matrix, proving that matrix multiplication is associative. It means that as long as the left-to-right order of the matrices remains identical, you can group the multiplications however you like.
