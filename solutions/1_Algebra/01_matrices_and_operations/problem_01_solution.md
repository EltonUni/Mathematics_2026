# Exercise 1: Matrix Size and Entries

**Step-by-Step Explanation:**
1. **Determining Size:** The size (or dimension) of a matrix is always written as $m \times n$, where $m$ is the number of rows (horizontal lines) and $n$ is the number of columns (vertical lines).
   * Matrix $A$ has 2 rows and 3 columns.
   * Matrix $B$ has 3 rows and 2 columns.
2. **Reading Entries:** The notation $a_{ij}$ refers to the element located in the $i$-th row and the $j$-th column of matrix $A$.
   * $a_{12}$ means row 1, column 2 of $A$, which is $-1$.
   * $a_{23}$ means row 2, column 3 of $A$, which is $3$.
   * $b_{21}$ means row 2, column 1 of $B$, which is $-2$.
   * $b_{32}$ means row 3, column 2 of $B$, which is $1$.
3. **Extracting Vectors:** A single row can be written as a row vector (a $1 \times n$ matrix), and a single column can be written as a column vector (an $m \times 1$ matrix).
   * The second row of $A$ contains the elements $0, 4, 5$.
   * The first column of $B$ contains the elements $1, -2, 4$.

**Final Result:**
* **Sizes:** $A$ is a $2 \times 3$ matrix. $B$ is a $3 \times 2$ matrix.
* **Entries:** $a_{12} = -1$, $a_{23} = 3$, $b_{21} = -2$, $b_{32} = 1$.
* **Vectors:** 
  * Second row of $A$: $\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$
  * First column of $B$: $\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$