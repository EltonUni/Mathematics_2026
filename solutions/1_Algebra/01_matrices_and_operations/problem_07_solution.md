# Exercise 7: Identity Matrix, Zero Matrix, and Powers

**Step-by-Step Explanation:**
1. **Identity Matrix ($I$):** For a $2 \times 2$ matrix, $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$. Multiplying any matrix $A$ by $I$ (from the left or the right) leaves $A$ unchanged, just like multiplying a number by $1$.
   * $AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
   * $IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$

2. **Zero Matrix ($0$):** A zero matrix of size $2 \times 2$ is $\begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$. Adding it to $A$ leaves $A$ unchanged, just like adding $0$ to a number.
   * $A+0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$

3. **Matrix Powers:**
   * $A^2 = A \times A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
     * Row 1 $\cdot$ Col 1 = $4 + 0 = 4$
     * Row 1 $\cdot$ Col 2 = $2 + 2 = 4$
     * Row 2 $\cdot$ Col 1 = $0 + 0 = 0$
     * Row 2 $\cdot$ Col 2 = $0 + 4 = 4$
     $$ A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} $$
   * $A^3 = A^2 \times A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
     * Row 1 $\cdot$ Col 1 = $8 + 0 = 8$
     * Row 1 $\cdot$ Col 2 = $4 + 8 = 12$
     * Row 2 $\cdot$ Col 1 = $0 + 0 = 0$
     * Row 2 $\cdot$ Col 2 = $0 + 8 = 8$
     $$ A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix} $$

**Final Result:**
* $AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$, $IA = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$, $A+0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
* $A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$, $A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$
* **Explanation:** The identity matrix $I$ acts as the multiplicative neutral element. The zero matrix $0$ acts as the additive neutral element. In successive powers of $A$, the main diagonal entries equal $2^n$, and the top-right entry equals $n \cdot 2^{n-1}$.