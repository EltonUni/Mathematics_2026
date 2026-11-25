# Exercise 4. Dot Product and Perpendicularity

## Given

Consider the vectors in $\mathbb{R}^3$:

$$
u = (1, 2, -1), \qquad v = (2, -1, 3), \qquad w = (2, -1, a),
$$

where $a \in \mathbb{R}$ is an unknown real parameter.

## Problem statement

Using the given vectors $u = (1, 2, -1)$, $v = (2, -1, 3)$, and $w = (2, -1, a)$:

1. Compute the dot product $u \cdot v$ and determine whether $u$ and $v$ are perpendicular.
2. Find the value of the parameter $a$ such that $w = (2, -1, a)$ is perpendicular to $u$.
3. Verify the result by direct substitution into the dot product and explain the geometric meaning of the calculation.

---

## Step 1: Mechanism — Dot Product and Orthogonality Criterion

For any two vectors $x = (x_1, x_2, x_3)$ and $y = (y_1, y_2, y_3)$ in $\mathbb{R}^3$, the **dot product** (scalar product) is defined algebraically by summing the products of corresponding components:

$$
x \cdot y = x_1 y_1 + x_2 y_2 + x_3 y_3.
$$

Geometrically, for nonzero vectors $x$ and $y$, the dot product is related to the angle $\theta \in [0, \pi]$ between them by

$$
x \cdot y = \|x\|\,\|y\|\cos\theta.
$$

**Perpendicularity (orthogonality) criterion:** Since $\|x\| > 0$ and $\|y\| > 0$ for nonzero vectors, we have

$$
x \perp y \iff \theta = 90^\circ \left(\frac{\pi}{2}\text{ rad}\right) \iff \cos\theta = 0 \iff x \cdot y = 0.
$$

This allows the dot product to serve both as a **test** (checking whether two given vectors are perpendicular) and as a **design equation** (solving $x \cdot y = 0$ for an unknown coordinate).

---

## Step 2: Compute $u \cdot v$ and Test Perpendicularity

Substitute the components of $u = (1, 2, -1)$ and $v = (2, -1, 3)$ into the dot product formula:

$$
\begin{aligned}
u \cdot v &= 1 \cdot 2 + 2 \cdot (-1) + (-1) \cdot 3\\
&= 2 - 2 - 3\\
&= -3.
\end{aligned}
$$

**Conclusion on perpendicularity:**
Because $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**. Moreover, since $u \cdot v < 0$ (and both vectors are nonzero), $\cos\theta < 0$, which indicates that the angle between $u$ and $v$ is **obtuse** ($\theta > 90^\circ$).

Therefore:

$$
\boxed{u \cdot v = -3 \neq 0 \implies u \text{ and } v \text{ are not perpendicular}}
$$

---

## Step 3: Solve for $a$ so that $w \perp u$

For $w = (2, -1, a)$ to be perpendicular to $u = (1, 2, -1)$, their dot product must equal zero:

$$
u \cdot w = 0.
$$

Compute $u \cdot w$ in terms of $a$:

$$
\begin{aligned}
u \cdot w &= 1 \cdot 2 + 2 \cdot (-1) + (-1) \cdot a\\
&= 2 - 2 - a\\
&= -a.
\end{aligned}
$$

Set the expression equal to $0$ and solve for $a$:

$$
-a = 0 \implies a = 0.
$$

Substituting $a = 0$ gives the perpendicular vector:

$$
w = (2, -1, 0).
$$

Therefore:

$$
\boxed{a = 0, \qquad w = (2, -1, 0)}
$$

---

## Step 4: Verify the Result and Geometric Interpretation

### 1. Verification
First confirm that $w = (2, -1, 0) \neq \mathbf{0}$ (its length is $\|w\| = \sqrt{2^2 + (-1)^2 + 0^2} = \sqrt{5} > 0$). Now compute $u \cdot w$ directly:

$$
\begin{aligned}
u \cdot w &= (1, 2, -1) \cdot (2, -1, 0)\\
&= 1 \cdot 2 + 2 \cdot (-1) + (-1) \cdot 0\\
&= 2 - 2 + 0\\
&= 0. \quad \checkmark
\end{aligned}
$$

Since both $u$ and $w$ are nonzero and $u \cdot w = 0$, $w = (2, -1, 0)$ is indeed perpendicular to $u$.

### 2. Geometric interpretation
- All vectors $x = (x_1, x_2, x_3) \in \mathbb{R}^3$ satisfying $u \cdot x = 0$, i.e.,
  $$
  x_1 + 2x_2 - x_3 = 0,
  $$
  form a **plane through the origin** perpendicular to the normal vector $u = (1, 2, -1)$.
- Notice that $v = (2, -1, 3)$ and $w = (2, -1, a)$ share the same $x$- and $y$-coordinates $(2, -1)$, whose contribution to the dot product with $u$ is already $1(2) + 2(-1) = 0$.
- In $v = (2, -1, 3)$, the third coordinate $z = 3$ makes the dot product nonzero. Changing the third coordinate to $a = 0$ moves the tip along a line parallel to the $z$-axis until it reaches the plane $x_1 + 2x_2 - x_3 = 0$. The resulting vector $w = (2, -1, 0)$ lies in this plane and is therefore perpendicular to $u$.

---

## Summary Table

| Vector Pair | Dot Product Calculation | Value | Geometric Relationship |
|---|---|---|---|
| $u = (1, 2, -1)$ and $v = (2, -1, 3)$ | $1(2) + 2(-1) + (-1)(3)$ | $-3 \neq 0$ | **Not perpendicular** (obtuse angle) |
| $u = (1, 2, -1)$ and $w = (2, -1, a)$ | $1(2) + 2(-1) + (-1)(a)$ | $-a$ | Perpendicular iff $-a = 0 \iff a = 0$ |
| $u = (1, 2, -1)$ and $w = (2, -1, 0)$ | $1(2) + 2(-1) + (-1)(0)$ | $0$ ✓ | **Perpendicular** ($90^\circ$ angle) |

---

## Final Answer

$$
\boxed{
u \cdot v = -3 \text{ (not perpendicular)}, \qquad
a = 0 \implies w = (2, -1, 0) \perp u
}
$$