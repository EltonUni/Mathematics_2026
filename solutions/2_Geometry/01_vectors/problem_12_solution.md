# Exercise 12. A Normal Vector to a Plane

## Given

Consider the three points in $\mathbb{R}^3$:

$$
A = (1, 0, 2), \qquad B = (2, 1, 0), \qquad C = (0, 3, 1).
$$

## Problem statement

For the given points $A = (1, 0, 2)$, $B = (2, 1, 0)$, and $C = (0, 3, 1)$:

1. Construct two non-collinear vectors lying in the plane determined by $A$, $B$, and $C$ (starting from a common vertex such as $A$).
2. Find a nonzero vector $n$ perpendicular to both in-plane vectors (a **normal vector** to the plane) using the cross product.
3. Verify using dot products that $n$ is perpendicular to both constructed vectors (as well as the third edge vector $\overrightarrow{BC}$).
4. Give a geometric interpretation of $n$ and show how it directly yields the scalar equation of the plane passing through $A$, $B$, and $C$.

---

## Step 1: Mechanism — Spanning Vectors and Normal Vector via Cross Product

Three non-collinear points $A, B, C \in \mathbb{R}^3$ uniquely determine a flat plane $\Pi$ in three-dimensional space:

1. **In-plane direction vectors:** Anchoring two displacement vectors at the same vertex $A$ gives two vectors lying entirely within the plane $\Pi$:
   $$
   u = \overrightarrow{AB} = B - A, \qquad v = \overrightarrow{AC} = C - A.
   $$
   Provided $u$ and $v$ are not scalar multiples of each other, they span the plane $\Pi$.

2. **Normal vector via cross product:** For any two non-collinear vectors $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$ in $\mathbb{R}^3$, their cross product
   $$
   n = u \times v =
   \begin{vmatrix}
   \mathbf{i} & \mathbf{j} & \mathbf{k}\\
   u_1 & u_2 & u_3\\
   v_1 & v_2 & v_3
   \end{vmatrix}
   $$
   is a nonzero vector orthogonal to both $u$ and $v$, and therefore perpendicular to every vector in the plane $\Pi$.

---

## Step 2: Construct Two Vectors Lying in the Plane

Using $A = (1, 0, 2)$ as the common initial point, construct $u = \overrightarrow{AB}$ and $v = \overrightarrow{AC}$:

$$
\begin{aligned}
u = \overrightarrow{AB} &= B - A = (2 - 1,\ 1 - 0,\ 0 - 2) = (1, 1, -2),\\[4pt]
v = \overrightarrow{AC} &= C - A = (0 - 1,\ 3 - 0,\ 1 - 2) = (-1, 3, -1).
\end{aligned}
$$

**Check for non-collinearity:**
Comparing the first and second components shows that $v$ is not a scalar multiple of $u$ ($\frac{-1}{1} = -1 \neq \frac{3}{1} = 3$). Hence $u$ and $v$ are linearly independent, confirming that $A$, $B$, and $C$ do not lie on a single line and uniquely define a plane.

Therefore:

$$
\boxed{u = \overrightarrow{AB} = (1, 1, -2), \qquad v = \overrightarrow{AC} = (-1, 3, -1)}
$$

---

## Step 3: Find a Vector $n$ Perpendicular to Both $u$ and $v$

Compute the cross product $n = u \times v = \overrightarrow{AB} \times \overrightarrow{AC}$ using the $3 \times 3$ determinant expansion:

$$
\begin{aligned}
n = u \times v &=
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}\\
1 & 1 & -2\\
-1 & 3 & -1
\end{vmatrix}\\[6pt]
&=
\begin{vmatrix} 1 & -2 \\ 3 & -1 \end{vmatrix}\mathbf{i}
-
\begin{vmatrix} 1 & -2 \\ -1 & -1 \end{vmatrix}\mathbf{j}
+
\begin{vmatrix} 1 & 1 \\ -1 & 3 \end{vmatrix}\mathbf{k}\\[6pt]
&= \big(1 \cdot (-1) - (-2) \cdot 3\big)\mathbf{i}
- \big(1 \cdot (-1) - (-2) \cdot (-1)\big)\mathbf{j}
+ \big(1 \cdot 3 - 1 \cdot (-1)\big)\mathbf{k}\\[6pt]
&= (-1 + 6)\mathbf{i} - (-1 - 2)\mathbf{j} + (3 + 1)\mathbf{k}\\[6pt]
&= 5\mathbf{i} + 3\mathbf{j} + 4\mathbf{k}\\[6pt]
&= (5, 3, 4).
\end{aligned}
$$

Confirm that $n$ is a nonzero vector:

$$
\|n\| = \sqrt{5^2 + 3^2 + 4^2} = \sqrt{25 + 9 + 16} = \sqrt{50} = 5\sqrt{2} \neq 0.
$$

Therefore:

$$
\boxed{n = (5, 3, 4)}
$$

---

## Step 4: Verify Perpendicularity Using Dot Products

Apply the orthogonality criterion ($n \perp w \iff n \cdot w = 0$) to test $n = (5, 3, 4)$ against both in-plane vectors:

1. **Dot product with $u = \overrightarrow{AB} = (1, 1, -2)$:**

   $$
   \begin{aligned}
   n \cdot u &= (5, 3, 4) \cdot (1, 1, -2)\\
   &= 5 \cdot 1 + 3 \cdot 1 + 4 \cdot (-2)\\
   &= 5 + 3 - 8\\
   &= 0. \quad \checkmark
   \end{aligned}
   $$

2. **Dot product with $v = \overrightarrow{AC} = (-1, 3, -1)$:**

   $$
   \begin{aligned}
   n \cdot v &= (5, 3, 4) \cdot (-1, 3, -1)\\
   &= 5 \cdot (-1) + 3 \cdot 3 + 4 \cdot (-1)\\
   &= -5 + 9 - 4\\
   &= 0. \quad \checkmark
   \end{aligned}
   $$

3. **Additional consistency check with the third triangle side $\overrightarrow{BC}$:**
   Since $\overrightarrow{BC} = C - B = (0 - 2,\ 3 - 1,\ 1 - 0) = (-2, 2, 1)$ also lies in the plane, it must likewise be orthogonal to $n$:

   $$
   n \cdot \overrightarrow{BC} = (5, 3, 4) \cdot (-2, 2, 1) = -10 + 6 + 4 = 0. \quad \checkmark
   $$

---

## Step 5: Geometric Meaning and Bridge to the Plane Equation

1. **Normal direction to the plane:**
   Because $n = (5, 3, 4)$ is perpendicular to two linearly independent vectors $u$ and $v$ in the plane $\Pi$, it is perpendicular to **every linear combination** $s\,u + t\,v$ ($s, t \in \mathbb{R}$), i.e., to every displacement vector between any two points on $\Pi$. In geometry, $n$ is called a **normal vector** to the plane (and any nonzero scalar multiple $k\,n = (5k, 3k, 4k)$ is equally valid as a normal vector).

2. **Direct bridge to the scalar equation of the plane:**
   An arbitrary point $P = (x, y, z) \in \mathbb{R}^3$ lies in the plane $\Pi$ if and only if the displacement vector $\overrightarrow{AP} = (x - 1,\ y - 0,\ z - 2)$ is perpendicular to $n = (5, 3, 4)$:

   $$
   n \cdot \overrightarrow{AP} = 0 \iff 5(x - 1) + 3(y - 0) + 4(z - 2) = 0 \iff 5x + 3y + 4z = 13.
   $$

   Substituting the three original points confirms that all three lie on this plane:
   - Point $A = (1, 0, 2)$: $5(1) + 3(0) + 4(2) = 5 + 0 + 8 = 13$ $\checkmark$
   - Point $B = (2, 1, 0)$: $5(2) + 3(1) + 4(0) = 10 + 3 + 0 = 13$ $\checkmark$
   - Point $C = (0, 3, 1)$: $5(0) + 3(3) + 4(1) = 0 + 9 + 4 = 13$ $\checkmark$

---

## Summary Table

| Quantity / Check | Formula / Operation | Calculation | Result |
|---|---|---|---|
| In-plane vector $u = \overrightarrow{AB}$ | $B - A$ | $(2 - 1,\ 1 - 0,\ 0 - 2)$ | $(1, 1, -2)$ |
| In-plane vector $v = \overrightarrow{AC}$ | $C - A$ | $(0 - 1,\ 3 - 0,\ 1 - 2)$ | $(-1, 3, -1)$ |
| Normal vector $n = u \times v$ | $3 \times 3$ determinant | $((-1 + 6),\ -(-1 - 2),\ (3 + 1))$ | $(5, 3, 4)$ ($\lVert n \rVert = 5\sqrt{2} \neq 0$) |
| Orthogonality check 1 | $n \cdot u$ | $5(1) + 3(1) + 4(-2)$ | $0$ ($n \perp \overrightarrow{AB}$) ✓ |
| Orthogonality check 2 | $n \cdot v$ | $5(-1) + 3(3) + 4(-1)$ | $0$ ($n \perp \overrightarrow{AC}$) ✓ |
| Plane equation | $n \cdot \overrightarrow{AP} = 0$ | $5(x - 1) + 3y + 4(z - 2) = 0$ | $5x + 3y + 4z = 13$ |

---

## Final Answer

$$
\boxed{
\overrightarrow{AB} = (1, 1, -2), \qquad
\overrightarrow{AC} = (-1, 3, -1), \qquad
n = (5, 3, 4)
}
$$

The dot products $n \cdot \overrightarrow{AB} = 0$ and $n \cdot \overrightarrow{AC} = 0$ verify that $n = (5, 3, 4)$ is perpendicular to both in-plane vectors, making $n$ a normal vector to the plane $5x + 3y + 4z = 13$.