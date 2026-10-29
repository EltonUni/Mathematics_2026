# Exercise 8: Row Operations and Their Reversibility

**Problem Statement:**
Given the initial matrix:
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}$$
Perform the following elementary row operations in order, showing the resulting matrix after each step, and specify the inverse row operation needed to reverse each step:
1. $R_2 \leftarrow R_2 - 2R_1$
2. $R_3 \leftarrow R_3 + R_1$
3. Interchange $R_2$ and $R_3$

**Step-by-Step Explanation:**
1. **Operation 1: $R_2 \leftarrow R_2 - 2R_1$**
   Subtract twice the first row from the second row.
   * New $R_2 = (2 - 2(1)), (4 - 2(2)), (1 - 2(-1)) = 0, 0, 3$
   Matrix after step 1:
   $$ \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix} $$
   * **Reversal:** To undo this, add twice the first row back to the second row: $R_2 \leftarrow R_2 + 2R_1$.

2. **Operation 2: $R_3 \leftarrow R_3 + R_1$**
   Add the first row to the third row.
   * New $R_3 = (-1 + 1), (1 + 2), (3 + (-1)) = 0, 3, 2$
   Matrix after step 2:
   $$ \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix} $$
   * **Reversal:** To undo this, subtract the first row from the third row: $R_3 \leftarrow R_3 - R_1$.

3. **Operation 3: Interchange $R_2$ and $R_3$**
   Swap the positions of the second and third rows.
   Matrix after step 3:
   $$ \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix} $$
   * **Reversal:** To undo this, swap the second and third rows again: Interchange $R_2$ and $R_3$.

**Final Result:**
- Matrix after Step 1: $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}$
- Matrix after Step 2: $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}$
- Matrix after Step 3: $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}$
- **Reversing Operations:** The operations that reverse these steps are $R_2 \leftarrow R_2 + 2R_1$, $R_3 \leftarrow R_3 - R_1$, and interchanging $R_2$ and $R_3$, respectively.