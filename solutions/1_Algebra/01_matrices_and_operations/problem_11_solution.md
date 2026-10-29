# Exercise 11: When Do Matrices Commute?

**Problem Statement:**
Given the matrix $A$ and a general $2 \times 2$ matrix $B$:
$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$$
Find the conditions on $a, b, c, d$ such that $A$ and $B$ commute (that is, $AB = BA$), and write out the general form of matrix $B$.

**Step-by-Step Explanation:**
For matrices to commute, the equation $AB = BA$ must hold true. We calculate both products and set corresponding entries equal to each other.

1. **Compute $AB$:**
   $$ AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} (1)a + (1)c & (1)b + (1)d \\ (0)a + (1)c & (0)b + (1)d \end{pmatrix} = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix} $$

2. **Compute $BA$:**
   $$ BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (a)1 + (b)0 & (a)1 + (b)1 \\ (c)1 + (d)0 & (c)1 + (d)1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix} $$

3. **Set $AB = BA$ and equate entries:**
   * Top-left: $a+c = a \implies c = 0$
   * Bottom-left: $c = c$ (Holds automatically, confirming $c = 0$)
   * Bottom-right: $d = c+d \implies c = 0$
   * Top-right: $b+d = a+b \implies d = a$ (Subtracting $b$ from both sides)

4. **Constructing the matrix $B$:**
   From our system of equations, we require $c = 0$ and $d = a$, while $b$ can be any real number.
   Substituting these into $B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, we obtain $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$.

**Final Result:**
- **Conditions:** $c = 0$ and $d = a$.
- **General Form:** The matrix $B$ must take the form $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$ for any real numbers $a$ and $b$.