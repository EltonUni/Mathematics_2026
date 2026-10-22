# Exercise 12: Formula for a Matrix Power

**Step-by-Step Explanation:**
1. **Calculating initial powers to find a pattern:**
   * $A^2 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & 1+1 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$
   * $A^3 = A^2 A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & 1+2 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$
   * $A^4 = A^3 A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & 1+3 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$
   
   **Conjecture:** Based on this pattern, it appears that the top-right entry perfectly matches the exponent. Thus, $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$.

2. **Mathematical Verification (Induction):**
   To prove this works for *all* powers, we assume our formula is true for some power $n$, meaning $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$. 
   We then multiply this by $A$ to see if it yields the correct formula for $n+1$:
   $$ A^{n+1} = A^n \cdot A = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} $$
   $$ A^{n+1} = \begin{pmatrix} (1)(1) + (n)(0) & (1)(1) + (n)(1) \\ (0)(1) + (1)(0) & (0)(1) + (1)(1) \end{pmatrix} $$
   $$ A^{n+1} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix} $$
   The resulting matrix perfectly matches our conjecture for the power $n+1$.

**Final Result:**
* $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$, $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$, $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$.
* **Conjecture:** $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$.
* **Proof:** Assuming $A^n$, multiplying by $A$ algebraically yields $\begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}$, proving the pattern holds infinitely.