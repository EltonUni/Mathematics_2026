# Exercise 14. Closest Point on a Line

## Given

Consider the point $P = (4, 1)$ in $\mathbb{R}^2$ and the line $L$ passing through the origin $O = (0, 0)$ with direction vector $v = (1, 2)$:

$$
P = (4, 1), \qquad L = \{t\,v : t \in \mathbb{R}\} = \{t(1, 2) : t \in \mathbb{R}\}.
$$

## Problem statement

For the given point $P = (4, 1)$ and line $L$ through the origin with direction vector $v = (1, 2)$:

1. Use orthogonal projection to find the closest point $Q$ on the line $L$ to the point $P$.
2. Compute the shortest distance $d(P, L)$ from $P$ to the line $L$, and verify it with the standard 2D point-to-line distance formula.
3. Verify using the dot product that the vector $\overrightarrow{QP}$ connecting the closest point $Q$ to $P$ is perpendicular to the direction vector $v$ of the line.
4. Explain geometrically why orthogonal projection solves the minimum-distance problem.

---

## Step 1: Mechanism — Orthogonal Projection as Minimum Distance

Represent the point $P = (4, 1)$ by its position vector $p = \overrightarrow{OP} = (4, 1)$ anchored at the origin $O = (0, 0)$. Every point $X$ on the line $L$ through the origin has position vector $x = t\,v$ for some scalar $t \in \mathbb{R}$.

1. **Closest point via projection:** The point $Q \in L$ closest to $P$ is the foot of the perpendicular dropped from $P$ onto $L$. Its position vector $q = \overrightarrow{OQ}$ is given by the orthogonal projection of $p$ onto $v$:

   $$
   q = \mathrm{proj}_v\,p = \frac{p \cdot v}{v \cdot v}\,v = \frac{p \cdot v}{\|v\|^2}\,v.
   $$

2. **Perpendicular error vector and distance:** The displacement vector from the closest point $Q$ to $P$ is

   $$
   \overrightarrow{QP} = p - q = p - \mathrm{proj}_v\,p.
   $$

   The shortest distance from $P$ to the line $L$ is the Euclidean length of this perpendicular segment:

   $$
   d(P, L) = d(P, Q) = \|\overrightarrow{QP}\| = \|p - \mathrm{proj}_v\,p\|.
   $$

---

## Step 2: Find the Closest Point $Q$ on the Line

Compute the dot products $p \cdot v$ and $v \cdot v$ for $p = (4, 1)$ and $v = (1, 2)$:

$$
\begin{aligned}
p \cdot v &= 4 \cdot 1 + 1 \cdot 2 = 4 + 2 = 6,\\[4pt]
v \cdot v &= \|v\|^2 = 1^2 + 2^2 = 1 + 4 = 5.
\end{aligned}
$$

Substitute these values into the projection formula to obtain the position vector $q = \overrightarrow{OQ}$ of the closest point $Q$:

$$
\begin{aligned}
q = \mathrm{proj}_v\,p &= \frac{6}{5}(1, 2)\\[4pt]
&= \left(\frac{6}{5},\ \frac{12}{5}\right) = (1.2,\ 2.4).
\end{aligned}
$$

Notice that $Q$ corresponds to the parameter value $t = \frac{6}{5}$ along the line $L = \{t(1, 2) : t \in \mathbb{R}\}$.

Therefore, the closest point on the line $L$ is:

$$
\boxed{Q = \left(\frac{6}{5},\ \frac{12}{5}\right)}
$$

---

## Step 3: Compute the Distance from $P$ to the Line

### 1. Construct the vector $\overrightarrow{QP}$ from $Q$ to $P$
Subtract the coordinates of $Q = \left(\frac{6}{5},\ \frac{12}{5}\right)$ from $P = (4, 1)$:

$$
\begin{aligned}
\overrightarrow{QP} = p - q &= (4, 1) - \left(\frac{6}{5},\ \frac{12}{5}\right)\\[4pt]
&= \left(\frac{20}{5} - \frac{6}{5},\ \frac{5}{5} - \frac{12}{5}\right)\\[4pt]
&= \left(\frac{14}{5},\ -\frac{7}{5}\right) = (2.8,\ -1.4).
\end{aligned}
$$

### 2. Compute the length $\|\overrightarrow{QP}\|$
Apply the Euclidean norm formula and simplify the radical:

$$
\begin{aligned}
d(P, L) = \|\overrightarrow{QP}\| &= \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2}\\[4pt]
&= \sqrt{\frac{196}{25} + \frac{49}{25}}\\[4pt]
&= \sqrt{\frac{245}{25}}\\[4pt]
&= \frac{\sqrt{49 \cdot 5}}{5} = \frac{7\sqrt{5}}{5} \approx 3.130.
\end{aligned}
$$

### 3. Independent check via the 2D point-to-line distance formula
The line through $(0, 0)$ with direction $v = (1, 2)$ has Cartesian equation $y = 2x$, or $2x - y = 0$. Applying the point-to-line formula $d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$ at $P = (4, 1)$ gives:

$$
d(P, L) = \frac{|2(4) - 1(1) + 0|}{\sqrt{2^2 + (-1)^2}} = \frac{|8 - 1|}{\sqrt{5}} = \frac{7}{\sqrt{5}} = \frac{7\sqrt{5}}{5}. \quad \checkmark
$$

Therefore:

$$
\boxed{d(P, L) = \frac{7\sqrt{5}}{5}}
$$

---

## Step 4: Verify Perpendicularity of $\overrightarrow{QP}$ to the Line Direction $v$

First observe that both $\overrightarrow{QP} = \left(\frac{14}{5},\ -\frac{7}{5}\right)$ and $v = (1, 2)$ are nonzero vectors. Compute their dot product:

$$
\begin{aligned}
\overrightarrow{QP} \cdot v &= \left(\frac{14}{5},\ -\frac{7}{5}\right) \cdot (1, 2)\\[4pt]
&= \frac{14}{5} \cdot 1 + \left(-\frac{7}{5}\right) \cdot 2\\[4pt]
&= \frac{14}{5} - \frac{14}{5}\\[4pt]
&= 0. \quad \checkmark
\end{aligned}
$$

Since $\overrightarrow{QP} \cdot v = 0$, the vector $\overrightarrow{QP}$ connecting the closest point $Q$ to $P$ is **perpendicular** to the direction vector $v$ of the line $L$.

---

## Step 5: Geometric Interpretation of Why $Q$ Minimizes Distance

1. **Pythagorean proof of optimality:**
   Let $X$ be **any** point on the line $L$, so $\overrightarrow{OX} = t\,v$ for some $t \in \mathbb{R}$. Because $Q$ also lies on $L$, the displacement vector $\overrightarrow{XQ} = q - t\,v = \left(\frac{6}{5} - t\right)v$ is parallel to $v$. Writing $\overrightarrow{XP} = \overrightarrow{XQ} + \overrightarrow{QP}$ and using $\overrightarrow{QP} \perp v$ ($\overrightarrow{QP} \perp \overrightarrow{XQ}$), the Pythagorean theorem gives:

   $$
   \|\overrightarrow{XP}\|^2 = \|\overrightarrow{XQ}\|^2 + \|\overrightarrow{QP}\|^2 \ge \|\overrightarrow{QP}\|^2.
   $$

   Since $\|\overrightarrow{XQ}\|^2 \ge 0$, every point $X \neq Q$ on the line is strictly farther from $P$ than $Q$ is. Equality holds **if and only if** $\|\overrightarrow{XQ}\| = 0$, i.e., $X = Q$.

2. **Right-triangle check at the origin:**
   The vectors $q = \overrightarrow{OQ}$, $\overrightarrow{QP}$, and $p = \overrightarrow{OP}$ form a right triangle with hypotenuse $p$:

   $$
   \|q\|^2 + \|\overrightarrow{QP}\|^2 = \left(\frac{36}{25} + \frac{144}{25}\right) + \left(\frac{196}{25} + \frac{49}{25}\right) = \frac{180}{25} + \frac{245}{25} = \frac{425}{25} = 17 = 4^2 + 1^2 = \|p\|^2. \quad \checkmark
   $$

---

## Summary Table

| Quantity / Check | Formula / Operation | Calculation | Result |
|---|---|---|---|
| Position vector $q = \overrightarrow{OQ}$ | $\frac{p \cdot v}{v \cdot v}\,v$ | $\frac{6}{5}(1, 2)$ | $\left(\frac{6}{5},\ \frac{12}{5}\right)$ (closest point $Q$) |
| Residual vector $\overrightarrow{QP}$ | $p - q$ | $(4, 1) - \left(\frac{6}{5}, \frac{12}{5}\right)$ | $\left(\frac{14}{5},\ -\frac{7}{5}\right)$ |
| Distance $d(P, L)$ | $\lVert \overrightarrow{QP} \rVert$ | $\sqrt{\frac{196}{25} + \frac{49}{25}} = \sqrt{\frac{245}{25}}$ | $\frac{7\sqrt{5}}{5}$ |
| Orthogonality check | $\overrightarrow{QP} \cdot v$ | $\frac{14}{5}(1) + \left(-\frac{7}{5}\right)(2)$ | $0$ ($\overrightarrow{QP} \perp v$) ✓ |

---

## Final Answer

$$
\boxed{
Q = \left(\frac{6}{5},\ \frac{12}{5}\right), \qquad
d(P, L) = \frac{7\sqrt{5}}{5}, \qquad
\overrightarrow{QP} \cdot v = 0
}
$$

The orthogonal projection of $P = (4, 1)$ onto the line $L$ locates the unique closest point $Q = \left(\frac{6}{5},\ \frac{12}{5}\right)$, at a shortest distance of $\frac{7\sqrt{5}}{5}$, with $\overrightarrow{QP} = \left(\frac{14}{5},\ -\frac{7}{5}\right)$ perpendicular to $v = (1, 2)$.