# Exercise 9: Composing Transformations

**Step-by-Step Explanation:**
1. **Computing $RSx$ (Scale first, then Rotate):**
   * Apply scaling $S$ to vector $x$:
     $$ Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (0)(2) \\ (0)(1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix} $$
     This stretched the vector's x-coordinate by a factor of 2.
   * Apply rotation $R$ to the result $Sx$:
     $$ RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} (0)(2) + (-1)(2) \\ (1)(2) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix} $$

2. **Computing $SRx$ (Rotate first, then Scale):**
   * Apply rotation $R$ to vector $x$:
     $$ Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (0)(1) + (-1)(2) \\ (1)(1) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix} $$
     This rotated the vector $90^\circ$ counterclockwise.
   * Apply scaling $S$ to the result $Rx$:
     $$ SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} (2)(-2) + (0)(1) \\ (0)(-2) + (1)(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix} $$

**Final Result:**
* $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$
* $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$
* **Explanation:** The order matters because the transformations are relative to fixed axes. If you scale horizontally first, the x-coordinate stretches. When you rotate it $90^\circ$, that stretched dimension becomes vertical. If you rotate first, the original y-coordinate becomes horizontal; applying the horizontal stretch now affects a completely different part of the original vector.