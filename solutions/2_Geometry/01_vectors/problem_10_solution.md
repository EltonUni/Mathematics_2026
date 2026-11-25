# Exercise 10. Triangle Area from Vectors

## Given

Consider the three vertices of a triangle in $\mathbb{R}^3$:

$$
A = (0, 0, 0), \qquad B = (2, 1, 0), \qquad C = (1, 3, 2).
$$

## Problem statement

For the triangle $\triangle ABC$ with vertices $A = (0, 0, 0)$, $B = (2, 1, 0)$, and $C = (1, 3, 2)$:

1. Construct the edge vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ starting at vertex $A$.
2. Compute the cross product $\overrightarrow{AB} \times \overrightarrow{AC}$ and its Euclidean length $\|\overrightarrow{AB} \times \overrightarrow{AC}\|$ to find the area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
3. Compute the area of $\triangle ABC$, and verify the result independently using the dot product / Lagrange identity.
4. Explain geometrically why the factor $\frac{1}{2}$ appears in the triangle area formula.

---

## Step 1: Mechanism — Cross Product Magnitude as Area

For any two non-collinear vectors $u, v \in \mathbb{R}^3$ anchored at the same initial point, the length of their cross product satisfies the geometric identity

$$
\|u \times v\| = \|u\|\,\|v\|\sin\theta,
$$

where $\theta \in (0, \pi)$ is the interior angle between $u$ and $v$.

- Taking $\|u\|$ as the length of the base of the parallelogram spanned by $u$ and $v$, the quantity $h = \|v\|\sin\theta$ is the perpendicular height to that base.
- Consequently, the length of the cross product equals the **area of the parallelogram** spanned by $u$ and $v$:
  $$
  \text{Area}_{\text{parallelogram}} = \|u \times v\|.
  $$
- Taking half of this value gives the **area of the triangle** having $u$ and $v$ as two adjacent sides:
  $$
  \text{Area}_{\text{triangle}} = \frac{1}{2}\|u \times v\|.
  $$

---

## Step 2: Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$

Subtract the coordinates of the initial vertex $A = (0, 0, 0)$ from the terminal vertices $B = (2, 1, 0)$ and $C = (1, 3, 2)$:

$$
\begin{aligned}
\overrightarrow{AB} &= B - A = (2 - 0,\ 1 - 0,\ 0 - 0) = (2, 1, 0),\\[4pt]
\overrightarrow{AC} &= C - A = (1 - 0,\ 3 - 0,\ 2 - 0) = (1, 3, 2).
\end{aligned}
$$

Notice that $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of each other (the third component of $\overrightarrow{AB}$ is $0$ while that of $\overrightarrow{AC}$ is $2$), so the three points $A, B, C$ are non-collinear and form a non-degenerate triangle.

Therefore:

$$
\boxed{\overrightarrow{AB} = (2, 1, 0), \qquad \overrightarrow{AC} = (1, 3, 2)}
$$

---

## Step 3: Compute the Cross Product and Parallelogram Area

### 1. Compute $\overrightarrow{AB} \times \overrightarrow{AC}$
Expand the $3 \times 3$ determinant with $\overrightarrow{AB} = (2, 1, 0)$ in the second row and $\overrightarrow{AC} = (1, 3, 2)$ in the third row:

$$
\begin{aligned}
\overrightarrow{AB} \times \overrightarrow{AC} &=
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}\\
2 & 1 & 0\\
1 & 3 & 2
\end{vmatrix}\\[6pt]
&=
\begin{vmatrix} 1 & 0 \\ 3 & 2 \end{vmatrix}\mathbf{i}
-
\begin{vmatrix} 2 & 0 \\ 1 & 2 \end{vmatrix}\mathbf{j}
+
\begin{vmatrix} 2 & 1 \\ 1 & 3 \end{vmatrix}\mathbf{k}\\[6pt]
&= (1 \cdot 2 - 0 \cdot 3)\mathbf{i} - (2 \cdot 2 - 0 \cdot 1)\mathbf{j} + (2 \cdot 3 - 1 \cdot 1)\mathbf{k}\\[6pt]
&= 2\mathbf{i} - 4\mathbf{j} + 5\mathbf{k}\\[6pt]
&= (2, -4, 5).
\end{aligned}
$$

*(Quick orthogonality check: $(2, -4, 5) \cdot (2, 1, 0) = 4 - 4 + 0 = 0$ and $(2, -4, 5) \cdot (1, 3, 2) = 2 - 12 + 10 = 0$. $\checkmark$)*

### 2. Compute the area of the parallelogram
Take the Euclidean length of $\overrightarrow{AB} \times \overrightarrow{AC} = (2, -4, 5)$ and simplify the radical:

$$
\begin{aligned}
\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\| &= \sqrt{2^2 + (-4)^2 + 5^2}\\
&= \sqrt{4 + 16 + 25}\\
&= \sqrt{45}\\
&= \sqrt{9 \cdot 5} = 3\sqrt{5}.
\end{aligned}
$$

Therefore:

$$
\boxed{\text{Area}_{\text{parallelogram}} = 3\sqrt{5} \approx 6.708}
$$

---

## Step 4: Compute the Area of $\triangle ABC$ and Verify

Multiply the area of the spanned parallelogram by $\frac{1}{2}$:

$$
\begin{aligned}
\text{Area}_{\triangle ABC} &= \frac{1}{2}\|\overrightarrow{AB} \times \overrightarrow{AC}\|\\
&= \frac{1}{2} \cdot 3\sqrt{5}\\
&= \frac{3\sqrt{5}}{2}.
\end{aligned}
$$

### Independent verification via the dot product (Lagrange identity)
Using $\|\overrightarrow{AB} \times \overrightarrow{AC}\|^2 = \|\overrightarrow{AB}\|^2\|\overrightarrow{AC}\|^2 - (\overrightarrow{AB} \cdot \overrightarrow{AC})^2$:

- $\|\overrightarrow{AB}\|^2 = 2^2 + 1^2 + 0^2 = 5$,
- $\|\overrightarrow{AC}\|^2 = 1^2 + 3^2 + 2^2 = 1 + 9 + 4 = 14$,
- $\overrightarrow{AB} \cdot \overrightarrow{AC} = 2(1) + 1(3) + 0(2) = 2 + 3 + 0 = 5$.

Substituting these into the identity gives:

$$
\|\overrightarrow{AB} \times \overrightarrow{AC}\|^2 = 5 \cdot 14 - 5^2 = 70 - 25 = 45 \implies \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \sqrt{45} = 3\sqrt{5},
$$

and therefore $\text{Area}_{\triangle ABC} = \frac{3\sqrt{5}}{2}$. $\checkmark$

Therefore:

$$
\boxed{\text{Area}_{\triangle ABC} = \frac{3\sqrt{5}}{2} \approx 3.354}
$$

---

## Step 5: Geometric Explanation of the Factor $\frac{1}{2}$

1. **Completing the parallelogram:**
   Starting from vertex $A$, the two edge vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ span a parallelogram $ABDC$, whose fourth opposite vertex is $D = A + \overrightarrow{AB} + \overrightarrow{AC} = (3, 4, 2)$. The quantity $\|\overrightarrow{AB} \times \overrightarrow{AC}\| = \|\overrightarrow{AB}\|\,\|\overrightarrow{AC}\|\sin\theta$ measures the area of this **entire parallelogram** $ABDC$.
2. **Splitting along the diagonal $BC$:**
   The third side $BC$ of $\triangle ABC$ is a **diagonal** of the parallelogram $ABDC$. This diagonal divides the parallelogram into two triangles: $\triangle ABC$ and $\triangle DCB$.
3. **Congruence and equal area:**
   Because opposite sides of a parallelogram are equal in length ($AB = DC$ and $AC = DB$) and the two triangles share the common diagonal $BC$, $\triangle ABC$ and $\triangle DCB$ are **congruent** (by the Side–Side–Side criterion) and therefore have the exact same area. Since the two non-overlapping triangles together make up the entire parallelogram $ABDC$, each triangle has **half** ($\frac{1}{2}$) the parallelogram's area:

   $$
   \text{Area}_{\triangle ABC} = \frac{1}{2}\text{Area}_{ABDC} = \frac{1}{2}\|\overrightarrow{AB} \times \overrightarrow{AC}\|.
   $$

---

## Summary Table

| Quantity | Formula / Mechanism | Calculation | Result |
|---|---|---|---|
| Edge vector $\overrightarrow{AB}$ | $B - A$ | $(2 - 0,\ 1 - 0,\ 0 - 0)$ | $(2, 1, 0)$ |
| Edge vector $\overrightarrow{AC}$ | $C - A$ | $(1 - 0,\ 3 - 0,\ 2 - 0)$ | $(1, 3, 2)$ |
| Cross product $\overrightarrow{AB} \times \overrightarrow{AC}$ | $3 \times 3$ determinant | $(2 - 0,\ -(4 - 0),\ 6 - 1)$ | $(2, -4, 5)$ |
| Parallelogram area | $\lVert \overrightarrow{AB} \times \overrightarrow{AC} \rVert$ | $\sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{45}$ | $3\sqrt{5}$ |
| Triangle area $\triangle ABC$ | $\frac{1}{2}\lVert \overrightarrow{AB} \times \overrightarrow{AC} \rVert$ | $\frac{1}{2} \cdot 3\sqrt{5}$ | $\frac{3\sqrt{5}}{2}$ |

---

## Final Answer

$$
\boxed{
\overrightarrow{AB} = (2, 1, 0), \qquad
\overrightarrow{AC} = (1, 3, 2), \qquad
\text{Area}_{\text{parallelogram}} = 3\sqrt{5}, \qquad
\text{Area}_{\triangle ABC} = \frac{3\sqrt{5}}{2}
}
$$

The factor $\frac{1}{2}$ appears because the diagonal $BC$ splits the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$ into two congruent triangles of equal area.