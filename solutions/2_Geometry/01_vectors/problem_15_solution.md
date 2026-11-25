# Exercise 15. Comparing Directions Using the Cosine of the Angle

## Given

Consider the three vectors in $\mathbb{R}^3$:

$$
a = (1, 2, 1), \qquad b = (2, 4, 2), \qquad c = (2, 0, 3).
$$

## Problem statement

For the given vectors $a = (1, 2, 1)$, $b = (2, 4, 2)$, and $c = (2, 0, 3)$:

1. Compute the normalized dot product (cosine of the angle)
   $$
   \cos\theta_{uv} = \frac{u \cdot v}{\|u\|\,\|v\|}
   $$
   for each of the three pairs of vectors: $(a, b)$, $(a, c)$, and $(b, c)$.
2. Order the three pairs by **increasing angle** between the vectors, stating both exact and approximate angle values.
3. Explain algebraically and geometrically why the expression equals $1$ for $a$ and $b$ even though the two vectors have different lengths (and why $(a, c)$ and $(b, c)$ yield the exact same angle).

---

## Step 1: Mechanism — Normalized Dot Product and Angle Comparison

For any two **nonzero** vectors $u, v \in \mathbb{R}^3$, the dot product identity $u \cdot v = \|u\|\,\|v\|\cos\theta$ gives the cosine of the angle $\theta \in [0, \pi]$ (or $[0^\circ, 180^\circ]$) between them:

$$
\cos\theta = \frac{u \cdot v}{\|u\|\,\|v\|} = \left(\frac{u}{\|u\|}\right) \cdot \left(\frac{v}{\|v\|}\right).
$$

**Key properties for comparing directions:**
1. **Scale invariance (unit-vector dot product):** Dividing each vector by its own Euclidean norm strips away length, leaving the dot product of the unit direction vectors $e_u = \frac{u}{\|u\|}$ and $e_v = \frac{v}{\|v\|}$.
2. **Monotonicity of $\cos\theta$ on $[0^\circ, 180^\circ]$:** On the interval $[0^\circ, 180^\circ]$, $\cos\theta$ is a **strictly decreasing** function of $\theta$:
   - $\cos\theta = 1 \iff \theta = 0^\circ$ (identical direction and orientation),
   - $0 < \cos\theta < 1 \iff 0^\circ < \theta < 90^\circ$ (acute angle; larger cosine means smaller angle),
   - $\cos\theta = 0 \iff \theta = 90^\circ$ (perpendicular),
   - $-1 \le \cos\theta < 0 \iff 90^\circ < \theta \le 180^\circ$ (obtuse or opposite).

---

## Step 2: Compute the Lengths of $a$, $b$, and $c$

Before evaluating the three pairs, compute the Euclidean norm $\|v\| = \sqrt{v_1^2 + v_2^2 + v_3^2}$ of each vector once:

$$
\begin{aligned}
\|a\| &= \sqrt{1^2 + 2^2 + 1^2} = \sqrt{1 + 4 + 1} = \sqrt{6},\\[4pt]
\|b\| &= \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = \sqrt{4 \cdot 6} = 2\sqrt{6},\\[4pt]
\|c\| &= \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 0 + 9} = \sqrt{13}.
\end{aligned}
$$

Notice immediately that $\|b\| = 2\sqrt{6} = 2\|a\|$, reflecting the fact that $b = 2a$.

---

## Step 3: Compute $\frac{u \cdot v}{\|u\|\,\|v\|}$ for Each Pair

There are $\binom{3}{2} = 3$ unordered pairs of distinct vectors: $(a, b)$, $(a, c)$, and $(b, c)$.

### 1. Pair $(a, b)$: $a = (1, 2, 1)$ and $b = (2, 4, 2)$
- **Dot product:**
  $$
  a \cdot b = 1 \cdot 2 + 2 \cdot 4 + 1 \cdot 2 = 2 + 8 + 2 = 12.
  $$
- **Product of lengths:**
  $$
  \|a\|\,\|b\| = \sqrt{6} \cdot 2\sqrt{6} = 2 \cdot 6 = 12.
  $$
- **Cosine and angle:**
  $$
  \cos\theta_{ab} = \frac{a \cdot b}{\|a\|\,\|b\|} = \frac{12}{12} = 1 \implies \theta_{ab} = \arccos(1) = 0^\circ \quad (0\text{ rad}).
  $$

### 2. Pair $(a, c)$: $a = (1, 2, 1)$ and $c = (2, 0, 3)$
- **Dot product:**
  $$
  a \cdot c = 1 \cdot 2 + 2 \cdot 0 + 1 \cdot 3 = 2 + 0 + 3 = 5.
  $$
- **Product of lengths:**
  $$
  \|a\|\,\|c\| = \sqrt{6} \cdot \sqrt{13} = \sqrt{78}.
  $$
- **Cosine and angle:**
  $$
  \cos\theta_{ac} = \frac{a \cdot c}{\|a\|\,\|c\|} = \frac{5}{\sqrt{78}} = \frac{5\sqrt{78}}{78} \approx 0.5661
  \implies \theta_{ac} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 0.9690\text{ rad} \approx 55.52^\circ.
  $$

### 3. Pair $(b, c)$: $b = (2, 4, 2)$ and $c = (2, 0, 3)$
- **Dot product:**
  $$
  b \cdot c = 2 \cdot 2 + 4 \cdot 0 + 2 \cdot 3 = 4 + 0 + 6 = 10.
  $$
- **Product of lengths:**
  $$
  \|b\|\,\|c\| = 2\sqrt{6} \cdot \sqrt{13} = 2\sqrt{78}.
  $$
- **Cosine and angle:**
  $$
  \cos\theta_{bc} = \frac{b \cdot c}{\|b\|\,\|c\|} = \frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}} = \frac{5\sqrt{78}}{78} \approx 0.5661
  \implies \theta_{bc} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 0.9690\text{ rad} \approx 55.52^\circ.
  $$

---

## Step 4: Order the Pairs by Increasing Angle

Because $\cos\theta$ strictly decreases as $\theta$ increases from $0^\circ$ to $180^\circ$, larger cosine values correspond to smaller angles. Comparing the three cosine values:

$$
\cos\theta_{ab} = 1 > \cos\theta_{ac} = \cos\theta_{bc} = \frac{5}{\sqrt{78}} \approx 0.5661.
$$

Therefore, ordering the pairs by **increasing angle** gives:

$$
\theta_{ab} = 0^\circ < \theta_{ac} = \theta_{bc} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ.
$$

1. **Smallest angle (1st):** $(a, b)$, with $\theta_{ab} = 0^\circ$ ($\cos\theta_{ab} = 1$).
2. **Tied for larger angle (2nd, equal):** $(a, c)$ and $(b, c)$, both with $\theta_{ac} = \theta_{bc} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$ ($\cos\theta = \frac{5}{\sqrt{78}}$).

---

## Step 5: Why $\frac{a \cdot b}{\|a\|\,\|b\|} = 1$ Despite Different Lengths

1. **Positive scalar proportionality ($b = 2a$):**
   Comparing components shows that $b = (2, 4, 2) = 2(1, 2, 1) = 2a$. Since the scalar factor $k = 2$ is **strictly positive**, $b$ stretches $a$ to twice its length ($\|b\| = 2\sqrt{6}$ vs. $\|a\| = \sqrt{6}$) without changing its direction or reversing its orientation.

2. **Algebraic cancellation of length:**
   In the normalized ratio $\frac{a \cdot b}{\|a\|\,\|b\|}$, any positive scaling factor $k > 0$ cancels out identically between the numerator and the denominator:

   $$
   \frac{a \cdot (ka)}{\|a\|\,\|ka\|} = \frac{k(a \cdot a)}{\|a\| \cdot k\|a\|} = \frac{k\|a\|^2}{k\|a\|^2} = 1.
   $$

   Equivalently, normalizing $a$ and $b$ produces the **exact same unit vector**:

   $$
   e_a = \frac{a}{\|a\|} = \left(\frac{1}{\sqrt{6}},\ \frac{2}{\sqrt{6}},\ \frac{1}{\sqrt{6}}\right) = \frac{2a}{2\|a\|} = \frac{b}{\|b\|} = e_b,
   $$

   so $\frac{a \cdot b}{\|a\|\,\|b\|} = e_a \cdot e_b = e_a \cdot e_a = \|e_a\|^2 = 1$.

3. **Geometric takeaway (direction vs. length):**
   Because $a$ and $b$ lie along the exact same ray starting from the origin, the angle between them is $\theta_{ab} = 0^\circ$, so $\cos\theta_{ab} = \cos(0^\circ) = 1$. For the exact same reason, replacing $a$ by $b = 2a$ when comparing against $c$ does not change the angle at all, explaining why $\theta_{bc} = \theta_{ac}$.

---

## Summary Table

| Pair | Dot Product $u \cdot v$ | Product of Norms $\lVert u \rVert\,\lVert v \rVert$ | $\cos\theta = \frac{u \cdot v}{\lVert u \rVert\,\lVert v \rVert}$ | Exact Angle $\theta$ | Approximate Angle | Rank (Increasing Angle) |
|---|---|---|---|---|---|---|
| $(a, b)$ | $12$ | $\sqrt{6}\cdot 2\sqrt{6} = 12$ | $1$ | $0\text{ rad}$ ($0^\circ$) | $0^\circ$ | **1st (smallest)** |
| $(a, c)$ | $5$ | $\sqrt{6}\cdot\sqrt{13} = \sqrt{78}$ | $\frac{5}{\sqrt{78}}$ | $\arccos\!\left(\frac{5}{\sqrt{78}}\right)$ | $\approx 55.52^\circ$ | **2nd (tied)** |
| $(b, c)$ | $10$ | $2\sqrt{6}\cdot\sqrt{13} = 2\sqrt{78}$ | $\frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}}$ | $\arccos\!\left(\frac{5}{\sqrt{78}}\right)$ | $\approx 55.52^\circ$ | **2nd (tied)** |

---

## Final Answer

$$
\boxed{
\frac{a \cdot b}{\|a\|\,\|b\|} = 1 \quad (\theta_{ab} = 0^\circ), \qquad
\frac{a \cdot c}{\|a\|\,\|c\|} = \frac{5}{\sqrt{78}} \quad (\theta_{ac} \approx 55.52^\circ), \qquad
\frac{b \cdot c}{\|b\|\,\|c\|} = \frac{5}{\sqrt{78}} \quad (\theta_{bc} \approx 55.52^\circ)
}
$$

- **Order by increasing angle:** $(a, b)$ first ($\theta_{ab} = 0^\circ$), followed by $(a, c)$ and $(b, c)$ tied ($\theta_{ac} = \theta_{bc} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$).
- **Why $(a, b)$ gives $1$:** Because $b = 2a$ ($2 > 0$), $a$ and $b$ have the exact same unit direction vector ($\frac{a}{\|a\|} = \frac{b}{\|b\|}$), and dividing by $\|a\|\,\|b\|$ cancels the difference in length completely.