# Exercise 11. Decomposition into Parallel and Perpendicular Components

## Given

Consider the two vectors in $\mathbb{R}^2$:

$$
u = (3, 4), \qquad v = (1, 2).
$$

## Problem statement

For the given vectors $u = (3, 4)$ and $v = (1, 2)$:

1. Decompose $u$ into the sum of two vectors $u = u_{\parallel} + u_{\perp}$, where $u_{\parallel}$ is parallel to $v$ and $u_{\perp}$ is perpendicular to $v$.
2. Verify both conditions $u = u_{\parallel} + u_{\perp}$ and $u_{\perp} \cdot v = 0$ by direct calculation.
3. Explain why these two equations serve as **independent checks** of correctness (neither implies the other), and give a geometric interpretation of the decomposition.

---

## Step 1: Mechanism — Orthogonal Vector Decomposition

Any vector $u \in \mathbb{R}^n$ can be uniquely decomposed with respect to a **nonzero** reference vector $v \in \mathbb{R}^n$ as

$$
u = u_{\parallel} + u_{\perp},
$$

where:

1. **Parallel component ($u_{\parallel}$):** Defined as the orthogonal projection of $u$ onto the line spanned by $v$:

   $$
   u_{\parallel} = \mathrm{proj}_v\,u = \frac{u \cdot v}{v \cdot v}\,v = \frac{u \cdot v}{\|v\|^2}\,v.
   $$

   Because $\frac{u \cdot v}{v \cdot v}$ is a scalar, $u_{\parallel}$ is guaranteed to be a scalar multiple of $v$ (hence parallel to $v$).

2. **Perpendicular component ($u_{\perp}$):** Defined as the difference between $u$ and its parallel projection:

   $$
   u_{\perp} = u - u_{\parallel} = u - \frac{u \cdot v}{v \cdot v}\,v.
   $$

---

## Step 2: Compute the Parallel Component $u_{\parallel}$

First compute the dot products $u \cdot v$ and $v \cdot v$ for $u = (3, 4)$ and $v = (1, 2)$:

$$
\begin{aligned}
u \cdot v &= 3 \cdot 1 + 4 \cdot 2 = 3 + 8 = 11,\\[4pt]
v \cdot v &= \|v\|^2 = 1^2 + 2^2 = 1 + 4 = 5.
\end{aligned}
$$

Substitute these values into the projection formula:

$$
\begin{aligned}
u_{\parallel} &= \frac{11}{5}(1, 2)\\[4pt]
&= \left(\frac{11}{5},\ \frac{22}{5}\right) = (2.2,\ 4.4).
\end{aligned}
$$

Notice that $u_{\parallel} = \frac{11}{5}v$ is explicitly a positive scalar multiple of $v$, confirming that it points in the exact same direction and orientation as $v$.

Therefore:

$$
\boxed{u_{\parallel} = \left(\frac{11}{5},\ \frac{22}{5}\right)}
$$

---

## Step 3: Compute the Perpendicular Component $u_{\perp}$

Subtract $u_{\parallel} = \left(\frac{11}{5},\ \frac{22}{5}\right)$ from $u = (3, 4)$ component by component:

$$
\begin{aligned}
u_{\perp} = u - u_{\parallel} &= (3, 4) - \left(\frac{11}{5},\ \frac{22}{5}\right)\\[4pt]
&= \left(\frac{15}{5} - \frac{11}{5},\ \frac{20}{5} - \frac{22}{5}\right)\\[4pt]
&= \left(\frac{4}{5},\ -\frac{2}{5}\right) = (0.8,\ -0.4).
\end{aligned}
$$

Therefore:

$$
\boxed{u_{\perp} = \left(\frac{4}{5},\ -\frac{2}{5}\right)}
$$

---

## Step 4: Perform Both Verification Checks

### 1. Reconstruction (sum) check: $u = u_{\parallel} + u_{\perp}$
Add the two computed components together:

$$
\begin{aligned}
u_{\parallel} + u_{\perp} &= \left(\frac{11}{5},\ \frac{22}{5}\right) + \left(\frac{4}{5},\ -\frac{2}{5}\right)\\[4pt]
&= \left(\frac{11 + 4}{5},\ \frac{22 - 2}{5}\right)\\[4pt]
&= \left(\frac{15}{5},\ \frac{20}{5}\right)\\[4pt]
&= (3, 4) = u. \quad \checkmark
\end{aligned}
$$

### 2. Orthogonality check: $u_{\perp} \cdot v = 0$
First note that $u_{\perp} = \left(\frac{4}{5}, -\frac{2}{5}\right) \neq \mathbf{0}$ and $v = (1, 2) \neq \mathbf{0}$. Compute their dot product:

$$
\begin{aligned}
u_{\perp} \cdot v &= \left(\frac{4}{5},\ -\frac{2}{5}\right) \cdot (1, 2)\\[4pt]
&= \frac{4}{5} \cdot 1 + \left(-\frac{2}{5}\right) \cdot 2\\[4pt]
&= \frac{4}{5} - \frac{4}{5}\\[4pt]
&= 0. \quad \checkmark
\end{aligned}
$$

Both checks hold, confirming that $u = \left(\frac{11}{5}, \frac{22}{5}\right) + \left(\frac{4}{5}, -\frac{2}{5}\right)$ is the valid orthogonal decomposition of $u$ along $v$.

---

## Step 5: Why These Are Two Independent Checks & Geometric Meaning

### 1. Why neither check implies the other (independence)
A valid orthogonal decomposition of $u$ along $v$ requires **two distinct conditions** beyond $u_{\parallel}$ being parallel to $v$: the two parts must **sum to $u$**, and the second part must be **perpendicular to $v$**. Neither condition automatically guarantees the other:

- **Passing $u_{\parallel} + u_{\perp} = u$ alone does not ensure $u_{\perp} \cdot v = 0$:**
  Infinitely many pairs of vectors add up to $u = (3, 4)$. For example, if you miscalculated the projection scalar and wrote $\tilde{u}_{\parallel} = 2v = (2, 4)$ and then computed $\tilde{u}_{\perp} = u - \tilde{u}_{\parallel} = (1, 0)$, their sum would still equal $(3, 4)$, yet $\tilde{u}_{\perp} \cdot v = 1(1) + 0(2) = 1 \neq 0$ (an oblique split rather than a right-angled one). The sum check tests only **subtraction/addition arithmetic**.
- **Passing $u_{\perp} \cdot v = 0$ alone does not ensure $u_{\parallel} + u_{\perp} = u$:**
  Every scalar multiple $k(2, -1)$ ($k \in \mathbb{R}$) is perpendicular to $v = (1, 2)$. For instance, $\hat{u}_{\perp} = (2, -1)$ satisfies $\hat{u}_{\perp} \cdot v = 2(1) + (-1)(2) = 0$, but pairing it with $u_{\parallel} = \left(\frac{11}{5}, \frac{22}{5}\right)$ fails to reconstruct $u$. The dot-product check tests specifically that the **projection coefficient** $\frac{u \cdot v}{v \cdot v} = \frac{11}{5}$ was calculated accurately.

Because each check catches a different type of error (arithmetic subtraction errors vs. projection-coefficient errors), performing both provides a complete verification.

### 2. Geometric and Pythagorean confirmation
Geometrically, $u_{\parallel} = \left(\frac{11}{5}, \frac{22}{5}\right)$ lies along the line $y = 2x$ spanned by $v$, while $u_{\perp} = \left(\frac{4}{5}, -\frac{2}{5}\right)$ turns $90^\circ$ from that line to reach the tip of $u = (3, 4)$. Together, $u_{\parallel}$, $u_{\perp}$, and $u$ form a **right triangle** with hypotenuse $u$, which is confirmed by the Pythagorean theorem:

$$
\|u_{\parallel}\|^2 + \|u_{\perp}\|^2 = \left(\frac{121}{25} + \frac{484}{25}\right) + \left(\frac{16}{25} + \frac{4}{25}\right) = \frac{605}{25} + \frac{20}{25} = \frac{625}{25} = 25 = 3^2 + 4^2 = \|u\|^2. \quad \checkmark
$$

---

## Summary Table

| Component / Check | Formula / Operation | Calculation | Result |
|---|---|---|---|
| Parallel component $u_{\parallel}$ | $\frac{u \cdot v}{v \cdot v}\,v$ | $\frac{11}{5}(1, 2)$ | $\left(\frac{11}{5},\ \frac{22}{5}\right)$ |
| Perpendicular component $u_{\perp}$ | $u - u_{\parallel}$ | $(3, 4) - \left(\frac{11}{5}, \frac{22}{5}\right)$ | $\left(\frac{4}{5},\ -\frac{2}{5}\right)$ |
| Check 1: Reconstruction | $u_{\parallel} + u_{\perp}$ | $\left(\frac{11}{5} + \frac{4}{5},\ \frac{22}{5} - \frac{2}{5}\right)$ | $(3, 4) = u$ ✓ |
| Check 2: Orthogonality | $u_{\perp} \cdot v$ | $\frac{4}{5}(1) + \left(-\frac{2}{5}\right)(2)$ | $0$ ($u_{\perp} \perp v$) ✓ |

---

## Final Answer

$$
\boxed{
u_{\parallel} = \left(\frac{11}{5},\ \frac{22}{5}\right), \qquad
u_{\perp} = \left(\frac{4}{5},\ -\frac{2}{5}\right), \qquad
u = \left(\frac{11}{5},\ \frac{22}{5}\right) + \left(\frac{4}{5},\ -\frac{2}{5}\right)
}
$$

Both checks pass: $u_{\parallel} + u_{\perp} = (3, 4) = u$ and $u_{\perp} \cdot v = 0$. They are independent checks because infinitely many vector pairs sum to $u$ without being perpendicular to $v$, and infinitely many vectors are perpendicular to $v$ without summing with $u_{\parallel}$ to give $u$.