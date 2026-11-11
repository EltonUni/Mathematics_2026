**Exercise 9. Area and the Determinant**

Let $u = \begin{pmatrix} 3 \\ 1 \end{pmatrix}$ and $v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$.

**1. Area of the parallelogram.** The area spanned by two vectors in $\mathbb{R}^2$ is the absolute value of the determinant of the matrix whose columns are the two vectors:

$$\text{Area} = \left|\det\begin{pmatrix} u & v \end{pmatrix}\right|.$$

Here

$$\det\begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix} = 3 \cdot 4 - 1 \cdot 1 = 12 - 1 = 11,$$

so

$$\text{Area} = |11| = 11.$$

**2. Reversing the order of the vectors.** Now put $v$ in the first column and $u$ in the second:

$$\det\begin{pmatrix} v & u \end{pmatrix} = \det\begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix} = 1 \cdot 1 - 3 \cdot 4 = 1 - 12 = -11.$$

**What changes.** The matrix $\begin{pmatrix} v & u \end{pmatrix}$ is obtained from $\begin{pmatrix} u & v \end{pmatrix}$ by swapping two columns, and swapping two columns multiplies the determinant by $-1$. So the determinant changes sign, from $11$ to $-11$. Geometrically, the sign records the orientation: $\det\begin{pmatrix} u & v \end{pmatrix} > 0$ means that rotating from $u$ to $v$ (through the smaller angle) is counterclockwise, and reversing the order makes it clockwise.

**What does not change.** The parallelogram spanned by $u$ and $v$ is the same set of points regardless of which vector is listed first, so its area is unchanged. Since area is the absolute value of the determinant,

$$\text{Area} = |-11| = 11.$$

**Answer:** The area is $11$. Reversing the order changes the determinant from $11$ to $-11$ (sign flip, orientation reversed), but the area remains $11$.