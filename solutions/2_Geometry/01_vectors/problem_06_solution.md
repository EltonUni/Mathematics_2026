# Exercise 6. Projection and Perpendicular Component

## Given

Consider the two vectors in $\mathbb{R}^2$:

$$
u = (4, 2), \qquad v = (1, 1).
$$

## Problem statement

For the given vectors $u = (4, 2)$ and $v = (1, 1)$:

1. Compute the orthogonal projection $\mathrm{proj}_v\,u$ of $u$ onto the direction of $v$.
2. Compute the residual vector $r = u - \mathrm{proj}_v\,u$.
3. Verify algebraically that $r \cdot v = 0$, and check that $\mathrm{proj}_v\,u + r = u$.
4. Explain the result geometrically in terms of orthogonal projection onto a line and decomposition into parallel and perpendicular components.

---

## Step 1: Mechanism — Orthogonal Projection Formula

For any vector $u \in \mathbb{R}^n$ and any **nonzero** vector $v \in \mathbb{R}^n$, the **orthogonal projection** of $u$ onto the line spanned by $v$ is given by

$$
\mathrm{proj}_v\,u = \frac{u \cdot v}{v \cdot v}\,v = \frac{u \cdot v}{\|v\|^2}\,v.
$$

**Why this formula works:**
- Letting $e = \frac{v}{\|v\|}$ be the unit vector in the direction of $v$, the signed scalar length of $u$ along $v$ is $u \cdot e = \frac{u \cdot v}{\|v\|}$.
- Multiplying that signed scalar component by the direction vector $e$ yields the vector projection:
  $$
  \mathrm{proj}_v\,u = (u \cdot e)\,e = \left(\frac{u \cdot v}{\|v\|}\right)\frac{v}{\|v\|} = \frac{u \cdot v}{\|v\|^2}\,v = \frac{u \cdot v}{v \cdot v}\,v.
  $$
- Subtracting $\mathrm{proj}_v\,u$ from $u$ isolates the remaining component:
  $$
  r = u - \mathrm{proj}_v\,u.
  $$

---

## Step 2: Compute the Projection $\mathrm{proj}_v\,u$

First compute the two dot products $u \cdot v$ and $v \cdot v$ for $u = (4, 2)$ and $v = (1, 1)$:

$$
\begin{aligned}
u \cdot v &= 4 \cdot 1 + 2 \cdot 1 = 4 + 2 = 6,\\
v \cdot v &= \|v\|^2 = 1^2 + 1^2 = 1 + 1 = 2.
\end{aligned}
$$

Substitute these values into the projection formula:

$$
\begin{aligned}
\mathrm{proj}_v\,u &= \frac{6}{2}\,(1, 1)\\
&= 3(1, 1)\\
&= (3, 3).
\end{aligned}
$$

Therefore:

$$
\boxed{\mathrm{proj}_v\,u = (3, 3)}
$$

---

## Step 3: Compute the Residual Vector $r = u - \mathrm{proj}_v\,u$

Subtract $\mathrm{proj}_v\,u = (3, 3)$ from $u = (4, 2)$ component by component:

$$
\begin{aligned}
r = u - \mathrm{proj}_v\,u &= (4, 2) - (3, 3)\\
&= (4 - 3,\ 2 - 3)\\
&= (1, -1).
\end{aligned}
$$

Therefore:

$$
\boxed{r = (1, -1)}
$$

---

## Step 4: Verify Perpendicularity ($r \cdot v = 0$) and Reconstruction

### 1. Perpendicularity check
Compute the dot product of $r = (1, -1)$ and $v = (1, 1)$:

$$
\begin{aligned}
r \cdot v &= (1, -1) \cdot (1, 1)\\
&= 1 \cdot 1 + (-1) \cdot 1\\
&= 1 - 1\\
&= 0. \quad \checkmark
\end{aligned}
$$

Since both $r = (1, -1)$ ($\|r\| = \sqrt{2} > 0$) and $v = (1, 1)$ ($\|v\| = \sqrt{2} > 0$) are nonzero vectors and $r \cdot v = 0$, the residual vector $r$ is **perpendicular** to $v$ (and hence also perpendicular to $\mathrm{proj}_v\,u = 3v$).

### 2. Decomposition check
Adding the projection and residual vectors recovers the original vector $u$:

$$
\mathrm{proj}_v\,u + r = (3, 3) + (1, -1) = (4, 2) = u. \quad \checkmark
$$

---

## Step 5: Geometric Explanation

1. **Supporting line and orthogonal shadow:** The nonzero vector $v = (1, 1)$ spans the line $y = x$ through the origin in $\mathbb{R}^2$. Dropping a perpendicular segment from the tip of $u = (4, 2)$ onto the line $y = x$ meets that line at $(3, 3)$, which is the closest point on the line to $(4, 2)$. The vector $\mathrm{proj}_v\,u = (3, 3)$ is the orthogonal shadow of $u$ along the direction of $v$.
2. **Perpendicular step ($r \cdot v = 0$):** Because $u = \mathrm{proj}_v\,u + r$, the vector $r = (1, -1)$ connects the foot of the perpendicular at $(3, 3)$ directly to the tip of $u$ at $(4, 2)$. Since this connecting segment was constructed by dropping a perpendicular onto the line spanned by $v$, $r$ meets $v$ at a $90^\circ$ angle, explaining geometrically why $r \cdot v = 0$.
3. **Right-triangle decomposition:** Together, $\mathrm{proj}_v\,u$, $r$, and $u$ form a **right triangle** in $\mathbb{R}^2$ with hypotenuse $u$ and perpendicular legs $\mathrm{proj}_v\,u$ and $r$. Their squared lengths satisfy the Pythagorean theorem:
   $$
   \|\mathrm{proj}_v\,u\|^2 + \|r\|^2 = (3^2 + 3^2) + (1^2 + (-1)^2) = 18 + 2 = 20 = 4^2 + 2^2 = \|u\|^2. \quad \checkmark
   $$

---

## Summary Table

| Quantity | Formula / Operation | Calculation | Result |
|---|---|---|---|
| Dot products $u \cdot v$ and $v \cdot v$ | Componentwise sum of products | $4(1)+2(1)$ and $1^2+1^2$ | $u \cdot v = 6$, $v \cdot v = 2$ |
| Orthogonal projection $\mathrm{proj}_v\,u$ | $\frac{u \cdot v}{v \cdot v}\,v$ | $\frac{6}{2}(1, 1)$ | $(3, 3)$ |
| Residual component $r$ | $u - \mathrm{proj}_v\,u$ | $(4, 2) - (3, 3)$ | $(1, -1)$ |
| Orthogonality check $r \cdot v$ | $(1, -1) \cdot (1, 1)$ | $1(1) + (-1)(1)$ | $0$ ($r \perp v$) ✓ |

---

## Final Answer

$$
\boxed{
\mathrm{proj}_v\,u = (3, 3), \qquad
r = (1, -1), \qquad
r \cdot v = 0
}
$$

Geometrically, $u = (3, 3) + (1, -1)$ decomposes $u$ into a component $\mathrm{proj}_v\,u = (3, 3)$ parallel to $v$ and a component $r = (1, -1)$ perpendicular to $v$.