# Exercise 5. Angle Between Vectors

## Given

Consider the two vectors in $\mathbb{R}^3$:

$$
u = (1, 1, 0), \qquad v = (1, 0, 1).
$$

## Problem statement

For the given vectors $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

1. Compute the dot product $u \cdot v$ and use its sign to predict the type of angle $\theta$ between $u$ and $v$ before computing $\theta$.
2. Compute the exact angle $\theta$ (in both radians and degrees) using the dot product and vector norms.
3. Compare the computed angle with the initial prediction, and verify the result geometrically.

---

## Step 1: Mechanism — Dot Product Sign and Angle Formula

For any two **nonzero** vectors $u, v \in \mathbb{R}^3$, the dot product is related to the angle $\theta \in [0, \pi]$ (or $[0^\circ, 180^\circ]$) between them by

$$
u \cdot v = \|u\|\,\|v\|\cos\theta.
$$

### 1. Qualitative prediction from the sign of $u \cdot v$
Because $\|u\| > 0$ and $\|v\| > 0$ for nonzero vectors, the product $\|u\|\,\|v\|$ is strictly positive. Therefore, the sign of $u \cdot v$ matches the sign of $\cos\theta$:

- $u \cdot v > 0 \iff \cos\theta > 0 \iff 0^\circ \le \theta < 90^\circ$ (**acute angle**, or $0^\circ$ if parallel with the same orientation),
- $u \cdot v = 0 \iff \cos\theta = 0 \iff \theta = 90^\circ$ (**right angle / perpendicular**),
- $u \cdot v < 0 \iff \cos\theta < 0 \iff 90^\circ < \theta \le 180^\circ$ (**obtuse angle**, or $180^\circ$ if opposite).

### 2. Exact angle formula
Dividing both sides by $\|u\|\,\|v\|$ isolates $\cos\theta$, and taking the inverse cosine on $[0, \pi]$ yields the unique angle between the vectors:

$$
\cos\theta = \frac{u \cdot v}{\|u\|\,\|v\|}, \qquad \theta = \arccos\!\left(\frac{u \cdot v}{\|u\|\,\|v\|}\right).
$$

---

## Step 2: Predict the Type of Angle Using the Sign of $u \cdot v$

Compute the dot product of $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

$$
\begin{aligned}
u \cdot v &= 1 \cdot 1 + 1 \cdot 0 + 0 \cdot 1\\
&= 1 + 0 + 0\\
&= 1.
\end{aligned}
$$

**Prediction:**
Since $u \cdot v = 1 > 0$, we have $\cos\theta > 0$. Furthermore, $u = (1, 1, 0)$ and $v = (1, 0, 1)$ are not scalar multiples of each other ($\theta \neq 0^\circ$). Thus, the angle between $u$ and $v$ must be **strictly acute**:

$$
0^\circ < \theta < 90^\circ \qquad \left(0 < \theta < \frac{\pi}{2}\text{ rad}\right).
$$

---

## Step 3: Compute the Exact Angle

First compute the Euclidean lengths (norms) of $u$ and $v$:

$$
\begin{aligned}
\|u\| &= \sqrt{1^2 + 1^2 + 0^2} = \sqrt{1 + 1 + 0} = \sqrt{2},\\
\|v\| &= \sqrt{1^2 + 0^2 + 1^2} = \sqrt{1 + 0 + 1} = \sqrt{2}.
\end{aligned}
$$

Now substitute $u \cdot v = 1$, $\|u\| = \sqrt{2}$, and $\|v\| = \sqrt{2}$ into the cosine formula:

$$
\begin{aligned}
\cos\theta &= \frac{u \cdot v}{\|u\|\,\|v\|}\\
&= \frac{1}{\sqrt{2} \cdot \sqrt{2}}\\
&= \frac{1}{2}.
\end{aligned}
$$

Since $\theta \in [0, \pi]$ and $\cos\theta = \frac{1}{2}$, taking the inverse cosine gives:

$$
\theta = \arccos\!\left(\frac{1}{2}\right) = \frac{\pi}{3}\text{ rad} = 60^\circ.
$$

Therefore:

$$
\boxed{\theta = \frac{\pi}{3}\text{ rad} = 60^\circ}
$$

---

## Step 4: Comparison with Prediction and Geometric Verification

### 1. Comparison with the prediction
The computed value $\theta = 60^\circ$ ($\frac{\pi}{3}\text{ rad}$) satisfies $0^\circ < 60^\circ < 90^\circ$, confirming that the angle is indeed **acute**, just as predicted immediately from $u \cdot v = 1 > 0$. Checking the sign of the dot product first also acts as a safeguard against arithmetic or calculator errors (any result $\ge 90^\circ$ would immediately be flagged as wrong).

### 2. Geometric verification (equilateral triangle in $\mathbb{R}^3$)
Consider the triangle in $\mathbb{R}^3$ with vertices at the origin $O = (0, 0, 0)$, $P = (1, 1, 0)$ (tip of $u$), and $Q = (1, 0, 1)$ (tip of $v$). The three side lengths are:

- $\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}$,
- $\|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}$,
- $\|v - u\| = \|(0, -1, 1)\| = \sqrt{0^2 + (-1)^2 + 1^2} = \sqrt{2}$.

Because all three sides have equal length $\sqrt{2}$, $\triangle OPQ$ is an **equilateral triangle**, so every interior angle—including the angle $\theta$ between $u$ and $v$ at the origin—must equal $60^\circ$. $\checkmark$

---

## Summary Table

| Stage | Quantity / Criterion | Calculation | Result |
|---|---|---|---|
| Qualitative test | Sign of $u \cdot v$ | $1(1) + 1(0) + 0(1) = 1 > 0$ | **Acute angle** ($0^\circ < \theta < 90^\circ$) |
| Vector lengths | $\|u\|$ and $\|v\|$ | $\sqrt{1^2+1^2+0^2}$ and $\sqrt{1^2+0^2+1^2}$ | $\|u\| = \sqrt{2}$, $\|v\| = \sqrt{2}$ |
| Cosine of angle | $\cos\theta = \frac{u \cdot v}{\|u\|\,\|v\|}$ | $\frac{1}{\sqrt{2}\cdot\sqrt{2}}$ | $\cos\theta = \frac{1}{2}$ |
| Exact angle | $\theta = \arccos(1/2)$ | $\frac{\pi}{3}\text{ rad}$ or $60^\circ$ | Matches acute prediction ✓ |

---

## Final Answer

$$
\boxed{
u \cdot v = 1 > 0 \text{ (acute prediction)}, \qquad
\theta = \frac{\pi}{3}\text{ rad} = 60^\circ
}
$$

The computed angle of $60^\circ$ agrees with the initial qualitative prediction that the angle is acute.