# Exercise 12: Formula for a Matrix Power

**Problem Statement:**
Given the matrix $A$:
$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$$
1. Compute $A^2$, $A^3$, and $A^4$.
2. Formulate a conjecture for the general formula for $A^n$ where $n \ge 1$ is an integer.
3. Prove your conjecture using mathematical induction.

**Step-by-Step Explanation:**
1. **Calculating initial powers to find a pattern:**
   * $A^2 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & 1+1 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$
   * $A^3 = A^2 A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & 1+2 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$
   * $A^4 = A^3 A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & 1+3 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$
   
   **Conjecture:** Based on this pattern, the top-right entry matches the exponent $n$. Thus, $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$.

2. **Mathematical Verification (Induction):**
   * **Base Case ($n=1$):** $A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, which matches our formula.
   * **Inductive Hypothesis:** Assume the formula holds for $n = k$, meaning $A^k = \begin{pmatrix} 1 & k \\ 0 & 1 \end{pmatrix}$.
   * **Inductive Step:** Multiply $A^k$ by $A$ to show it holds for $n = k+1$:
     $$ A^{k+1} = A^k \cdot A = \begin{pmatrix} 1 & k \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} $$
     $$ A^{k+1} = \begin{pmatrix} (1)(1) + (k)(0) & (1)(1) + (k)(1) \\ (0)(1) + (1)(0) & (0)(1) + (1)(1) \end{pmatrix} $$
     $$ A^{k+1} = \begin{pmatrix} 1 & k+1 \\ 0 & 1 \end{pmatrix} $$
   The resulting matrix matches our conjecture for $n = k+1$, completing the proof by induction.

**Final Result:**
- $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$, $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$, $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$
- **Conjecture:** $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$ for all integers $n \ge 1$.
- **Proof:** Proven by mathematical induction for all $n \ge 1$.