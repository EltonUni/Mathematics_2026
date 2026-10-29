# Exercise 9: Composing Transformations

**Problem Statement:**
Given the scaling matrix $S$, rotation matrix $R$, and vector $x$:
$$S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \quad R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}, \quad x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$$
1. Compute $RSx$ (scaling first, followed by rotation).
2. Compute $SRx$ (rotation first, followed by scaling).
3. Compare the two results and explain geometrically why the order of geometric transformations matters.

**Step-by-Step Explanation:**
1. **Computing $RSx$ (Scale first, then Rotate):**
   * Apply scaling $S$ to vector $x$:
     $$ Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (0)(2) \\ (0)(1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix} $$
     This stretches the vector's x-coordinate by a factor of 2.
   * Apply rotation $R$ to the result $Sx$:
     $$ RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} (0)(2) + (-1)(2) \\ (1)(2) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix} $$

2. **Computing $SRx$ (Rotate first, then Scale):**
   * Apply rotation $R$ to vector $x$:
     $$ Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (0)(1) + (-1)(2) \\ (1)(1) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix} $$
     This rotates the vector $90^\circ$ counterclockwise.
   * Apply scaling $S$ to the result $Rx$:
     $$ SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} (2)(-2) + (0)(1) \\ (0)(-2) + (1)(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix} $$

**Final Result:**
- $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$
- $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$
- **Explanation:** The order matters because the transformations are relative to fixed coordinate axes. When scaling horizontally first, the x-coordinate stretches, and rotating $90^\circ$ turns that stretched component into a vertical component. When rotating first, the original y-coordinate becomes the horizontal component; applying the horizontal stretch now affects a completely different dimension of the original vector.