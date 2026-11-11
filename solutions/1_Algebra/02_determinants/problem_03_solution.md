**1. Compute $\det A$**
For the given matrix $A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}$, we can compute the determinant using cofactor expansion along the first row:

$\det A = 1 \cdot \det\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} - 2 \cdot \det\begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} + 0 \cdot \det\begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix}$

$\det A = 1 \cdot (3(1) - 1(1)) - 2 \cdot (0(1) - 1(2)) + 0$
$\det A = 1 \cdot (3 - 1) - 2 \cdot (0 - 2)$
$\det A = 1 \cdot (2) - 2 \cdot (-2)$
$\det A = 2 + 4 = 6$

**2. Form matrix $B$**
Matrix $B$ is formed by swapping the first and second rows of $A$:
$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}$

**3. Predict $\det B$ using a determinant property**
A fundamental property of determinants states that swapping any two rows of a square matrix multiplies its determinant by $-1$.
Since $B$ is obtained by swapping one pair of rows in $A$, we predict:
$\det B = -\det A = -6$

**4. Verify the prediction by calculation**
Let's compute $\det B$ directly using cofactor expansion along the first row:

$\det B = 0 \cdot \det\begin{pmatrix} 2 & 0 \\ 1 & 1 \end{pmatrix} - 3 \cdot \det\begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} + 1 \cdot \det\begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}$

$\det B = 0 - 3 \cdot (1(1) - 0(2)) + 1 \cdot (1(1) - 2(2))$
$\det B = -3 \cdot (1 - 0) + 1 \cdot (1 - 4)$
$\det B = -3(1) + 1(-3)$
$\det B = -3 - 3 = -6$

The calculation yields $-6$, which confirms our prediction.