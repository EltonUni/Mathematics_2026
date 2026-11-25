# Exercise 3. Vector Normalization

## Given

Consider the vector in $\mathbb{R}^2$:

$$
v = (3, 4).
$$

## Problem statement

For the given vector $v = (3, 4)$:

1. Compute the length $\|v\|$ and find a unit vector $e$ with the same direction and orientation as $v$.
2. Verify by direct calculation that $\|e\| = 1$.
3. Reconstruct $v$ in the magnitude–direction form $v = \|v\|e$.
4. Explain geometrically and algebraically what changes during normalization and what remains unchanged.

---

## Step 1: Mechanism — Vector Normalization

For any **nonzero** vector $v \in \mathbb{R}^n$ ($v \neq \mathbf{0}$), its **unit vector** (normalized vector) $e$ in the same direction and orientation is obtained by scaling $v$ by the reciprocal of its length:

$$
e = \frac{v}{\|v\|} = \frac{1}{\|v\|} v.
$$

Why this works:
- Because $v \neq \mathbf{0}$, its Euclidean norm satisfies $\|v\| > 0$, so division by $\|v\|$ is well-defined.
- Multiplying a vector by a **strictly positive** scalar $c = \frac{1}{\|v\|} > 0$ stretches or shrinks its length by the factor $c$ without reversing its sense or tilting its line of action.
- By homogeneity of the norm ($\|cv\| = |c|\,\|v\|$), the resulting vector automatically has length $1$.

---

## Step 2: Compute the Length $\|v\|$

Apply the 2D Euclidean norm formula to $v = (3, 4)$:

$$
\begin{aligned}
\|v\| &= \sqrt{3^2 + 4^2}\\
&= \sqrt{9 + 16}\\
&= \sqrt{25}\\
&= 5.
\end{aligned}
$$

Thus, the vector $v$ has length $5$.

---

## Step 3: Construct the Unit Vector $e$

Divide each component of $v = (3, 4)$ by $\|v\| = 5$:

$$
\begin{aligned}
e = \frac{v}{\|v\|} &= \frac{1}{5}(3, 4)\\
&= \left(\frac{3}{5},\ \frac{4}{5}\right) = (0.6,\ 0.8).
\end{aligned}
$$

Therefore:

$$
\boxed{e = \left(\frac{3}{5},\ \frac{4}{5}\right)}
$$

---

## Step 4: Verify that $\|e\| = 1$

Compute the Euclidean length of $e = \left(\frac{3}{5},\ \frac{4}{5}\right)$ directly:

$$
\begin{aligned}
\|e\| &= \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2}\\
&= \sqrt{\frac{9}{25} + \frac{16}{25}}\\
&= \sqrt{\frac{25}{25}}\\
&= \sqrt{1} = 1. \quad \checkmark
\end{aligned}
$$

This confirms that $e$ is a unit vector.

---

## Step 5: Reconstruct $v$ in the Form $v = \|v\|e$

Multiply the scalar length $\|v\| = 5$ by the unit vector $e = \left(\frac{3}{5},\ \frac{4}{5}\right)$:

$$
\begin{aligned}
\|v\|e &= 5 \cdot \left(\frac{3}{5},\ \frac{4}{5}\right)\\
&= \left(5 \cdot \frac{3}{5},\ 5 \cdot \frac{4}{5}\right)\\
&= (3, 4) = v. \quad \checkmark
\end{aligned}
$$

This decomposition separates $v$ cleanly into two independent pieces of information: its **magnitude** ($\|v\| = 5$) and its **pure direction and orientation** ($e = \left(\frac{3}{5}, \frac{4}{5}\right)$).

---

## Step 6: What Changes vs. What Remains Unchanged

### What changes during normalization
1. **Length (magnitude):** The norm is rescaled from $\|v\| = 5$ down to $\|e\| = 1$ (multiplied by $\frac{1}{5}$).
2. **Component values and position:** Each coordinate is scaled by $\frac{1}{5}$, moving the vector's tip from $(3, 4)$ onto the **unit circle** $x^2 + y^2 = 1$ at the point $\left(\frac{3}{5}, \frac{4}{5}\right)$.

### What remains unchanged
1. **Direction (supporting line):** Both $v$ and $e$ lie along the exact same line through the origin, preserving the component ratio (slope):
   $$
   \frac{4/5}{3/5} = \frac{4}{3}.
   $$
2. **Orientation (sense):** Because the scaling factor $\frac{1}{5}$ is **strictly positive**, the vector still points in the same sense (into the first quadrant, rather than the opposite vector $-e = \left(-\frac{3}{5}, -\frac{4}{5}\right)$ in the third quadrant).
3. **Angle with the coordinate axes:** The angle $\theta$ with the positive $x$-axis satisfies
   $$
   \cos\theta = \frac{3}{5}, \qquad \sin\theta = \frac{4}{5} \qquad (\theta \approx 53.13^\circ)
   $$
   for both $v$ and $e$. Indeed, the components of the unit vector $e$ are literally $(\cos\theta, \sin\theta)$.

---

## Summary Table

| Property | Original Vector $v$ | Unit Vector $e = \frac{v}{\|v\|}$ | Status |
|---|---|---|---|
| Components | $(3, 4)$ | $\left(\frac{3}{5}, \frac{4}{5}\right)$ | Scaled by $\frac{1}{5}$ |
| Length (norm) | $\|v\| = 5$ | $\|e\| = 1$ | **Changed** (normalized to $1$) |
| Component ratio ($y/x$) | $\frac{4}{3}$ | $\frac{4}{3}$ | **Unchanged** (same direction) |
| Quadrant / Orientation | First quadrant ($+,+$) | First quadrant ($+,+$) | **Unchanged** (same orientation) |
| Angle with $+x$-axis | $\arccos(3/5) \approx 53.13^\circ$ | $\arccos(3/5) \approx 53.13^\circ$ | **Unchanged** |

---

## Final Answer

$$
\boxed{
e = \left(\frac{3}{5},\ \frac{4}{5}\right), \qquad
\|e\| = 1, \qquad
v = 5\left(\frac{3}{5},\ \frac{4}{5}\right)
}
$$

Normalization changes only the vector's **length** (from $5$ to $1$) while keeping its **direction**, **orientation**, and **angles with the axes** completely unchanged.