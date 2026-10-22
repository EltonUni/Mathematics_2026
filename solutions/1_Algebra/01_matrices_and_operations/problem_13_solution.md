# Exercise 13: A Recurrence Written in Matrix Form

**Step-by-Step Explanation:**
1. **Calculating Matrix Powers:**
   * $F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1(1)+1(1) & 1(1)+1(0) \\ 1(1)+0(1) & 1(1)+0(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$
   * $F^3 = F^2 F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 2(1)+1(1) & 2(1)+1(0) \\ 1(1)+1(1) & 1(1)+1(0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$
   * $F^4 = F^3 F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 3+2 & 3+0 \\ 2+1 & 2+0 \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$
   * $F^5 = F^4 F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 5+3 & 5+0 \\ 3+2 & 3+0 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$

   Comparing these entries to the sequence $0, 1, 1, 2, 3, 5, 8 \dots$ (the Fibonacci sequence), we can see that the entries of the matrix are sequential Fibonacci numbers.

2. **Analyzing the Matrix-Vector Step:**
   We multiply the matrix $F$ by a generic state vector $\begin{pmatrix} a \\ b \end{pmatrix}$:
   $$ F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} (1)a + (1)b \\ (1)a + (0)b \end{pmatrix} = \begin{pmatrix} a+b \\ a \end{pmatrix} $$
   
**Final Result:**
* $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$, $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$, $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$, $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$
* **Relationship:** The powers of matrix $F$ generate the Fibonacci sequence.
* **Explanation:** The multiplication step shows exactly how the sequence advances. The top row of $F$ ($1$ and $1$) calculates the next term by adding the current two terms ($a+b$). The bottom row of $F$ ($1$ and $0$) takes the top term ($a$) and shifts it down to the bottom position, storing it as the "previous" term for the next cycle.