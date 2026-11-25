# Exercise 13. Do Four Points Lie in One Plane?

## Given

Consider the four points in $\mathbb{R}^3$:

$$
A = (0, 0, 0), \qquad B = (1, 2, 0), \qquad C = (0, 1, 1), \qquad D = (2, 5, 1).
$$

## Problem statement

For the given points $A = (0, 0, 0)$, $B = (1, 2, 0)$, $C = (0, 1, 1)$, and $D = (2, 5, 1)$:

1. Construct the displacement vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ starting at $A$.
2. Compute the normal vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$ to the plane determined by $A$, $B$, and $C$.
3. Construct the displacement vector $\overrightarrow{AD}$ and check whether $\overrightarrow{AD} \cdot n = 0$.
4. Based on this result, decide whether $D$ lies in the plane determined by $A$, $B$, and $C$, justify the geometric criterion used, and verify the conclusion independently.

---

## Step 1: Mechanism — Coplanarity Criterion via Cross and Dot Products

To test whether four points $A, B, C, D \in \mathbb{R}^3$ lie in a single plane (assuming $A, B, C$ are not collinear), we combine the cross product and dot product in three steps:

1. **Spanning vectors of the plane:** Anchor two displacement vectors at $A$:
   $$
   \overrightarrow{AB} = B - A, \qquad \overrightarrow{AC} = C - A.
   $$
   Because $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are non-collinear, they span the unique plane $\Pi$ passing through $A$, $B$, and $C$.
2. **Normal direction via the cross product:** Their cross product
   $$
   n = \overrightarrow{AB} \times \overrightarrow{AC}
   $$
   is a nonzero vector perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$, and therefore perpendicular to every vector lying in the plane $\Pi$.
3. **Orthogonality test via the dot product:** Construct $\overrightarrow{AD} = D - A$ and compute $\overrightarrow{AD} \cdot n$:
   - If $\overrightarrow{AD} \cdot n = 0$, then $\overrightarrow{AD}$ is perpendicular to the normal vector $n$, which means $\overrightarrow{AD}$ lies in $\Pi$ and therefore $D \in \Pi$.
   - If $\overrightarrow{AD} \cdot n \neq 0$, then $\overrightarrow{AD}$ has a nonzero component along $n$ (outside $\Pi$), so $D$ does not lie in $\Pi$.

---

## Step 2: Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$

Subtract the coordinates of the initial point $A = (0, 0, 0)$ from $B = (1, 2, 0)$ and $C = (0, 1, 1)$:

$$
\begin{aligned}
\overrightarrow{AB} &= B - A = (1 - 0,\ 2 - 0,\ 0 - 0) = (1, 2, 0),\\[4pt]
\overrightarrow{AC} &= C - A = (0 - 0,\ 1 - 0,\ 1 - 0) = (0, 1, 1).
\end{aligned}
$$

**Check that $A, B, C$ determine a unique plane:**
The vectors $\overrightarrow{AB} = (1, 2, 0)$ and $\overrightarrow{AC} = (0, 1, 1)$ are not scalar multiples of each other (the first component of $\overrightarrow{AC}$ is $0$ while that of $\overrightarrow{AB}$ is $1$, and the third component of $\overrightarrow{AB}$ is $0$ while that of $\overrightarrow{AC}$ is $1$). Therefore, $A$, $B$, and $C$ are non-collinear and uniquely define a plane $\Pi$.

Therefore:

$$
\boxed{\overrightarrow{AB} = (1, 2, 0), \qquad \overrightarrow{AC} = (0, 1, 1)}
$$

---

## Step 3: Find $n = \overrightarrow{AB} \times \overrightarrow{AC}$

Compute the cross product using the $3 \times 3$ determinant expansion with $\overrightarrow{AB} = (1, 2, 0)$ in the second row and $\overrightarrow{AC} = (0, 1, 1)$ in the third row:

$$
\begin{aligned}
n = \overrightarrow{AB} \times \overrightarrow{AC} &=
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}\\
1 & 2 & 0\\
0 & 1 & 1
\end{vmatrix}\\[6pt]
&=
\begin{vmatrix} 2 & 0 \\ 1 & 1 \end{vmatrix}\mathbf{i}
-
\begin{vmatrix} 1 & 0 \\ 0 & 1 \end{vmatrix}\mathbf{j}
+
\begin{vmatrix} 1 & 2 \\ 0 & 1 \end{vmatrix}\mathbf{k}\\[6pt]
&= (2 \cdot 1 - 0 \cdot 1)\mathbf{i} - (1 \cdot 1 - 0 \cdot 0)\mathbf{j} + (1 \cdot 1 - 2 \cdot 0)\mathbf{k}\\[6pt]
&= 2\mathbf{i} - 1\mathbf{j} + 1\mathbf{k}\\[6pt]
&= (2, -1, 1).
\end{aligned}
$$

**Quick verification of $n$:**
- Length: $\|n\| = \sqrt{2^2 + (-1)^2 + 1^2} = \sqrt{4 + 1 + 1} = \sqrt{6} \neq 0$.
- Orthogonality to $\overrightarrow{AB}$ and $\overrightarrow{AC}$:
  $$
  n \cdot \overrightarrow{AB} = 2(1) + (-1)(2) + 1(0) = 0, \qquad
  n \cdot \overrightarrow{AC} = 2(0) + (-1)(1) + 1(1) = 0. \quad \checkmark
  $$

Therefore:

$$
\boxed{n = (2, -1, 1)}
$$

---

## Step 4: Construct $\overrightarrow{AD}$ and Check Whether $\overrightarrow{AD} \cdot n = 0$

### 1. Construct $\overrightarrow{AD}$
Subtract $A = (0, 0, 0)$ from $D = (2, 5, 1)$:

$$
\overrightarrow{AD} = D - A = (2 - 0,\ 5 - 0,\ 1 - 0) = (2, 5, 1).
$$

### 2. Compute the dot product $\overrightarrow{AD} \cdot n$
Take the dot product of $\overrightarrow{AD} = (2, 5, 1)$ with the normal vector $n = (2, -1, 1)$:

$$
\begin{aligned}
\overrightarrow{AD} \cdot n &= (2, 5, 1) \cdot (2, -1, 1)\\[4pt]
&= 2 \cdot 2 + 5 \cdot (-1) + 1 \cdot 1\\[4pt]
&= 4 - 5 + 1\\[4pt]
&= 0. \quad \checkmark
\end{aligned}
$$

Thus, $\overrightarrow{AD} \cdot n = 0$ holds.

Therefore:

$$
\boxed{\overrightarrow{AD} = (2, 5, 1), \qquad \overrightarrow{AD} \cdot n = 0}
$$

---

## Step 5: Decision, Justification, and Independent Verification

### 1. Decision
**Yes**, the point $D = (2, 5, 1)$ **lies in the plane** determined by $A$, $B$, and $C$. All four points $A, B, C, D$ are coplanar.

### 2. Justification of the geometric criterion
- Because $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are non-collinear, the plane $\Pi$ through $A, B, C$ consists precisely of all points $P \in \mathbb{R}^3$ whose displacement vector $\overrightarrow{AP}$ is perpendicular to the normal vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$ (since $n \neq \mathbf{0}$ defines the unique direction perpendicular to $\Pi$).
- Geometrically, the scalar projection of $\overrightarrow{AD}$ onto the normal vector $n$ is $\frac{\overrightarrow{AD} \cdot n}{\|n\|}$, which measures the signed perpendicular distance from $D$ to the plane $\Pi$.
- Finding $\overrightarrow{AD} \cdot n = 0$ proves that this perpendicular distance is $0$ (equivalently, the parallelepiped spanned by $\overrightarrow{AB}$, $\overrightarrow{AC}$, and $\overrightarrow{AD}$ has signed volume $(\overrightarrow{AB} \times \overrightarrow{AC}) \cdot \overrightarrow{AD} = 0$ and is completely flat). Hence $D$ lies directly on the plane $\Pi$.

### 3. Independent verifications
- **Plane equation check:** Using normal vector $n = (2, -1, 1)$ and base point $A = (0, 0, 0)$, the scalar equation of $\Pi$ is $2x - y + z = 0$. Substituting $D = (2, 5, 1)$ gives:
  $$
  2(2) - 5 + 1 = 4 - 5 + 1 = 0. \quad \checkmark
  $$
- **In-plane linear combination check:** Since $D \in \Pi$, $\overrightarrow{AD}$ must be expressible as a linear combination of $\overrightarrow{AB}$ and $\overrightarrow{AC}$:
  $$
  2\overrightarrow{AB} + 1\overrightarrow{AC} = 2(1, 2, 0) + 1(0, 1, 1) = (2, 4, 0) + (0, 1, 1) = (2, 5, 1) = \overrightarrow{AD}. \quad \checkmark
  $$

---

## Summary Table

| Step / Quantity | Formula / Operation | Calculation | Result |
|---|---|---|---|
| Edge vector $\overrightarrow{AB}$ | $B - A$ | $(1 - 0,\ 2 - 0,\ 0 - 0)$ | $(1, 2, 0)$ |
| Edge vector $\overrightarrow{AC}$ | $C - A$ | $(0 - 0,\ 1 - 0,\ 1 - 0)$ | $(0, 1, 1)$ |
| Normal vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$ | $3 \times 3$ determinant | $(2 - 0,\ -(1 - 0),\ 1 - 0)$ | $(2, -1, 1)$ ($\lVert n \rVert = \sqrt{6} \neq 0$) |
| Test vector $\overrightarrow{AD}$ | $D - A$ | $(2 - 0,\ 5 - 0,\ 1 - 0)$ | $(2, 5, 1)$ |
| Coplanarity test $\overrightarrow{AD} \cdot n$ | $(2, 5, 1) \cdot (2, -1, 1)$ | $2(2) + 5(-1) + 1(1)$ | $0$ ($\overrightarrow{AD} \perp n \implies D \in \Pi$) ✓ |

---

## Final Answer

$$
\boxed{
\overrightarrow{AB} = (1, 2, 0), \qquad
\overrightarrow{AC} = (0, 1, 1), \qquad
n = (2, -1, 1), \qquad
\overrightarrow{AD} = (2, 5, 1), \qquad
\overrightarrow{AD} \cdot n = 0
}
$$

Since $n = (2, -1, 1) \neq \mathbf{0}$ is perpendicular to the plane through $A, B, C$ and $\overrightarrow{AD} \cdot n = 0$, the vector $\overrightarrow{AD}$ is orthogonal to the plane's normal vector, proving that **$D$ lies in the plane determined by $A, B, C$**.