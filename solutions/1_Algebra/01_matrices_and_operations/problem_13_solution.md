# Exercise 13: A Recurrence Written in Matrix Form

**Problem Statement:**
Given the matrix $F$:
$$F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$$
and the Fibonacci sequence defined by $f_0 = 0, f_1 = 1, f_2 = 1, f_3 = 2, f_4 = 3, f_5 = 5, f_6 = 8, \dots$
1. Compute the powers $F^2$, $F^3$, $F^4$, and $F^5$.
2. Explain the relationship between the entries of $F^n$ and the Fibonacci sequence.
3. Multiply $F$ by a state vector $\begin{pmatrix} a \\ b \end{pmatrix}$ and explain how this operation models the step-by-step advancement of the Fibonacci recurrence.

**Step-by-Step Explanation:**
1. **Calculating Matrix Powers:**
   * $F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1(1)+1(1) & 1(1)+1(0) \\ 1(1)+0(1) & 1(1)+0(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$
   * $F^3 = F^2 F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 2(1)+1(1) & 2(1)+1(0) \\ 1(1)+1(1) & 1(1)+1(0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$
   * $F^4 = F^3 F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 3+2 & 3+0 \\ 2+1 & 2+0 \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$
   * $F^5 = F^4 F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 5+3 & 5+0 \\ 3+2 & 3+0 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$

   Comparing these entries to the sequence $0, 1, 1, 2, 3, 5, 8, \dots$ (the Fibonacci sequence), we observe that the entries of $F^n$ are sequential Fibonacci numbers, specifically:
   $$F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix}$$

2. **Analyzing the Matrix-Vector Step:**
   We multiply the matrix $F$ by a generic state vector $\begin{pmatrix} a \\ b \end{pmatrix}$:
   $$ F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} (1)a + (1)b \\ (1)a + (0)b \end{pmatrix} = \begin{pmatrix} a+b \\ a \end{pmatrix} $$

**Final Result:**
- $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$, $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$, $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$, $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$
- **Relationship:** The powers of matrix $F$ directly encode the Fibonacci sequence, where $F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix}$.
- **Explanation:** The multiplication step demonstrates how the recurrence advances: the top row calculates the new term by summing the current two terms ($a+b$), while the bottom row shifts the current term ($a$) down to serve as the previous term in the next step.