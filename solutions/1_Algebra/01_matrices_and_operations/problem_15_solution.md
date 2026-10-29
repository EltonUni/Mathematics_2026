# Exercise 15: Associativity of Multiplication and Different Calculation Paths

**Problem Statement:**
Given the matrices $A$, $B$, and $C$:
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}, \quad C = \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}$$
1. Compute the product using Path 1: $(AB)C$.
2. Compute the product using Path 2: $A(BC)$.
3. Verify that matrix multiplication is associative, and explicitly compare the computational efficiency (number of intermediate scalar multiplications) between the two paths.

**Step-by-Step Explanation:**
Matrix multiplication is associative, meaning $(AB)C = A(BC)$. We will calculate both paths to confirm they yield the same matrix and compare their computational workload.

### Path 1: Calculate $(AB)C$
1. **Compute $AB$:** ($A$ is $2 \times 3$, $B$ is $3 \times 2 \implies AB$ is $2 \times 2$)
   $$ AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} $$
   * Row 1 dot columns: $(1)(1)+(2)(2)+(0)(-1) = 5$, and $(1)(0)+(2)(1)+(0)(3) = 2$
   * Row 2 dot columns: $(0)(1)+(1)(2)+(1)(-1) = 1$, and $(0)(0)+(1)(1)+(1)(3) = 4$
   $$ AB = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} $$

2. **Multiply $(AB)$ by $C$:** ($AB$ is $2 \times 2$, $C$ is $2 \times 2 \implies$ result is $2 \times 2$)
   $$ (AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} $$
   * Row 1 dot columns: $(5)(2)+(2)(0) = 10$, and $(5)(1)+(2)(-1) = 3$
   * Row 2 dot columns: $(1)(2)+(4)(0) = 2$, and $(1)(1)+(4)(-1) = -3$
   $$ (AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} $$

---

### Path 2: Calculate $A(BC)$
1. **Compute $BC$:** ($B$ is $3 \times 2$, $C$ is $2 \times 2 \implies BC$ is $3 \times 2$)
   $$ BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 2+0 & 1+0 \\ 4+0 & 2-1 \\ -2+0 & -1-3 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} $$

2. **Multiply $A$ by $(BC)$:** ($A$ is $2 \times 3$, $BC$ is $3 \times 2 \implies$ result is $2 \times 2$)
   $$ A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} $$
   * Row 1 dot columns: $(1)(2)+(2)(4)+(0)(-2) = 10$, and $(1)(1)+(2)(1)+(0)(-4) = 3$
   * Row 2 dot columns: $(0)(2)+(1)(4)+(1)(-2) = 2$, and $(0)(1)+(1)(1)+(1)(-4) = -3$
   $$ A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} $$

---

### Computational Cost Comparison (Scalar Multiplications):
To multiply an $m \times n$ matrix by an $n \times p$ matrix, the number of required scalar multiplications is $m \times n \times p$:

* **Path 1: $(AB)C$**
  * Step 1 ($AB$): $(2 \times 3) \times (3 \times 2) \implies 2 \times 3 \times 2 = 12$ scalar multiplications.
  * Step 2 ($(AB)C$): $(2 \times 2) \times (2 \times 2) \implies 2 \times 2 \times 2 = 8$ scalar multiplications.
  * **Total for Path 1:** $12 + 8 = 20$ scalar multiplications.

* **Path 2: $A(BC)$**
  * Step 1 ($BC$): $(3 \times 2) \times (2 \times 2) \implies 3 \times 2 \times 2 = 12$ scalar multiplications.
  * Step 2 ($A(BC)$): $(2 \times 3) \times (3 \times 2) \implies 2 \times 3 \times 2 = 12$ scalar multiplications.
  * **Total for Path 2:** $12 + 12 = 24$ scalar multiplications.

**Final Result:**
- **Path 1:** $(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$
- **Path 2:** $A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$
- **Associativity:** Verified. Both grouping strategies yield the exact same $2 \times 2$ result.
- **Efficiency Comparison:** Path 1 requires **20 scalar multiplications**, whereas Path 2 requires **24 scalar multiplications**. Thus, Path 1 is computationally more efficient.