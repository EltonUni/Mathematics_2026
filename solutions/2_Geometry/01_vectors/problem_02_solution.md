# Exercise 2. Distance as the Length of a Vector

## Given

Consider the two points in $\mathbb{R}^3$:

$$
A = (1, 2, 3), \qquad B = (4, -2, 6).
$$

## Problem statement

For the given points $A = (1, 2, 3)$ and $B = (4, -2, 6)$:

1. Construct the displacement vector $\overrightarrow{AB}$ from $A$ to $B$.
2. Compute the length (Euclidean norm) $\|\overrightarrow{AB}\|$.
3. Compute the distance $d(A, B)$ between the two points directly using the 3D coordinate distance formula.
4. Explain algebraically and geometrically why both calculations produce the exact same result, and verify symmetry using $\overrightarrow{BA}$.

---

## Step 1: Mechanism — Displacement Vectors, Euclidean Norm, and Distance

To connect points and vectors in $\mathbb{R}^3$, we use three closely related definitions:

1. **Displacement vector between two points:** For points $A = (x_A, y_A, z_A)$ and $B = (x_B, y_B, z_B)$, the vector starting at $A$ and ending at $B$ is obtained by subtracting the coordinates of the initial point $A$ from the terminal point $B$:
   $$
   \overrightarrow{AB} = B - A = (x_B - x_A,\ y_B - y_A,\ z_B - z_A).
   $$
2. **Euclidean length (norm) of a vector:** For any vector $v = (v_1, v_2, v_3) \in \mathbb{R}^3$, its length is given by the square root of the sum of the squares of its components:
   $$
   \|v\| = \sqrt{v_1^2 + v_2^2 + v_3^2}.
   $$
3. **Coordinate distance formula:** The Euclidean distance between $A$ and $B$ is defined as:
   $$
   d(A, B) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2}.
   $$

---

## Step 2: Construct $\overrightarrow{AB}$

Subtract the coordinates of $A = (1, 2, 3)$ from the coordinates of $B = (4, -2, 6)$:

$$
\begin{aligned}
\overrightarrow{AB} &= (4 - 1,\ -2 - 2,\ 6 - 3)\\
&= (3,\ -4,\ 3).
\end{aligned}
$$

This means that moving from point $A$ to point $B$ requires shifting $+3$ units along the $x$-axis, $-4$ units along the $y$-axis, and $+3$ units along the $z$-axis.

Therefore:

$$
\boxed{\overrightarrow{AB} = (3, -4, 3)}
$$

---

## Step 3: Compute the Length $\|\overrightarrow{AB}\|$

Apply the Euclidean norm formula to the components $(v_1, v_2, v_3) = (3, -4, 3)$ of $\overrightarrow{AB}$:

$$
\begin{aligned}
\|\overrightarrow{AB}\| &= \sqrt{3^2 + (-4)^2 + 3^2}\\
&= \sqrt{9 + 16 + 9}\\
&= \sqrt{34}.
\end{aligned}
$$

Since $34 = 2 \cdot 17$ has no perfect-square factors other than $1$, $\sqrt{34}$ is already in simplest radical form ($\sqrt{34} \approx 5.831$).

Therefore:

$$
\boxed{\|\overrightarrow{AB}\| = \sqrt{34}}
$$

---

## Step 4: Compute the Distance Using the Coordinate Formula

Substitute the coordinates of $A = (1, 2, 3)$ and $B = (4, -2, 6)$ directly into the 3D coordinate distance formula:

$$
\begin{aligned}
d(A, B) &= \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2}\\
&= \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2}\\
&= \sqrt{3^2 + (-4)^2 + 3^2}\\
&= \sqrt{9 + 16 + 9}\\
&= \sqrt{34}.
\end{aligned}
$$

Therefore:

$$
\boxed{d(A, B) = \sqrt{34}}
$$

---

## Step 5: Verification and Explanation of Why Both Give the Same Result

### 1. Algebraic equivalence
By definition, the components $(v_1, v_2, v_3)$ of $\overrightarrow{AB}$ are equal to the coordinate differences:

$$
v_1 = x_B - x_A, \qquad v_2 = y_B - y_A, \qquad v_3 = z_B - z_A.
$$

Substituting these definitions directly into the vector length formula yields:

$$
\|\overrightarrow{AB}\| = \sqrt{v_1^2 + v_2^2 + v_3^2} = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2} = d(A, B).
$$

Thus, the point-distance formula is not a separate rule—it is literally the definition of the length of the difference vector $\overrightarrow{AB}$.

### 2. Geometric interpretation (3D Pythagorean theorem)
Geometrically, the segment connecting $A$ and $B$ is the main space diagonal of a rectangular box with side lengths:

$$
|\Delta x| = |3| = 3, \qquad |\Delta y| = |-4| = 4, \qquad |\Delta z| = |3| = 3.
$$

Applying the Pythagorean theorem twice—first on the $xy$-base ($\sqrt{3^2 + (-4)^2} = 5$) and then vertically along $z$ ($\sqrt{5^2 + 3^2} = \sqrt{34}$)—gives the length of the directed arrow $\overrightarrow{AB}$, which is precisely the straight-line distance between $A$ and $B$.

### 3. Symmetry check using $\overrightarrow{BA}$
Reversing the direction gives $\overrightarrow{BA} = A - B = (-3, 4, -3)$. Computing its length confirms that distance does not depend on orientation:

$$
\|\overrightarrow{BA}\| = \sqrt{(-3)^2 + 4^2 + (-3)^2} = \sqrt{9 + 16 + 9} = \sqrt{34} = \|\overrightarrow{AB}\|. \quad \checkmark
$$

---

## Summary Table

| Quantity | Formula / Mechanism | Calculation | Result |
|---|---|---|---|
| Displacement vector $\overrightarrow{AB}$ | $B - A$ | $(4 - 1,\ -2 - 2,\ 6 - 3)$ | $(3, -4, 3)$ |
| Vector length $\|\overrightarrow{AB}\|$ | $\sqrt{v_1^2 + v_2^2 + v_3^2}$ | $\sqrt{3^2 + (-4)^2 + 3^2}$ | $\sqrt{34}$ |
| Coordinate distance $d(A, B)$ | $\sqrt{(x_B-x_A)^2 + (y_B-y_A)^2 + (z_B-z_A)^2}$ | $\sqrt{3^2 + (-4)^2 + 3^2}$ | $\sqrt{34}$ |
| Reverse check $\|\overrightarrow{BA}\|$ | $\|A - B\|$ | $\sqrt{(-3)^2 + 4^2 + (-3)^2}$ | $\sqrt{34}$ ✓ |

---

## Final Answer

$$
\boxed{
\overrightarrow{AB} = (3, -4, 3), \qquad
\|\overrightarrow{AB}\| = d(A, B) = \sqrt{34}
}
$$

Both calculations yield $\sqrt{34}$ because the coordinate distance formula is simply the Euclidean norm of the displacement vector $\overrightarrow{AB} = B - A$ via the 3D Pythagorean theorem.