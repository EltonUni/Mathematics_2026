# Exercise 14

## Question

Consider the parameter-dependent matrix and the linear system

$$A = \begin{pmatrix} 1 & 2 \\ k & 4 \end{pmatrix}, \qquad Ax = b.$$

1. Find all values of $k$ for which the system $Ax = b$ has exactly one solution for every right-hand side $b$.
2. For the exceptional value of $k$, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example of a right-hand side $b$ for which the system has no solution.

## Solution

### Part 1: Compute the determinant

$$\det(A) = 1 \cdot 4 - 2 \cdot k = 4 - 2k.$$

### Part 2: Exactly one solution for every $b$

The system $Ax = b$ has exactly one solution for every $b$ if and only if $A$ is invertible, i.e. $\det(A) \neq 0$:

$$4 - 2k \neq 0 \iff k \neq 2.$$

So for every $k \neq 2$ the system has exactly one solution for every right-hand side $b$, namely $x = A^{-1}b$.

### Part 3: The exceptional value $k = 2$

Then

$$A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}, \qquad \det(A) = 0,$$

and the second row is twice the first row. Writing $b = \begin{pmatrix} b_1 \\ b_2 \end{pmatrix}$, the system is

$$x_1 + 2x_2 = b_1, \qquad 2x_1 + 4x_2 = b_2.$$

Subtracting $2$ times the first equation from the second gives $0 = b_2 - 2b_1$. So the system is solvable only when $b_2 = 2b_1$.

**Infinitely many solutions.** Take $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$. Both equations reduce to $x_1 + 2x_2 = 1$, so every pair $(x_1, x_2) = (1 - 2s,\ s)$ with $s \in \mathbb{R}$ is a solution. For example, $(1, 0)$ and $(-1, 1)$ both work.

**No solution.** Take $b = \begin{pmatrix} 1 \\ 3 \end{pmatrix}$. The equations are $x_1 + 2x_2 = 1$ and $2x_1 + 4x_2 = 3$. Subtracting $2$ times the first from the second gives $0 = 1$, a contradiction, so there is no solution.

### Answer

The system has exactly one solution for every $b$ if and only if $k \neq 2$. For $k = 2$, the right-hand side $b = (1, 2)^T$ gives infinitely many solutions and $b = (1, 3)^T$ gives none.