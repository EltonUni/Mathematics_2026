# Exercise 2: Addition and Scalar Multiplication

**Step-by-Step Explanation:**
1. **Checking Compatibility:** To add or subtract matrices, they must have exactly the same size. Both $A$ and $B$ are $2 \times 2$ matrices, so these operations are valid. Operations are performed entry-by-entry.
2. **Computing $A+B$:** We add the corresponding elements from each matrix:
   $$ \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix} $$
3. **Computing $A-B$:** We subtract the elements of $B$ from the corresponding elements of $A$:
   $$ \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix} $$
4. **Computing $3A-2B$:** First, perform scalar multiplication by multiplying every entry in $A$ by $3$, and every entry in $B$ by $2$.
   * $3A = \begin{pmatrix} 3(1) & 3(2) \\ 3(-1) & 3(3) \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}$
   * $2B = \begin{pmatrix} 2(4) & 2(-2) \\ 2(0) & 2(5) \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}$
   * Now, subtract $2B$ from $3A$:
   $$ \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix} $$

**Final Result:**
* $A+B = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$
* $A-B = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$
* $3A-2B = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$