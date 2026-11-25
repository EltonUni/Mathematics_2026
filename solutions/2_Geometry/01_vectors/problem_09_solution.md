# Exercise 9. Cross Product as a Perpendicular Direction

## Given

Consider the two vectors in $\mathbb{R}^3$:

$$
u = (1, 2, 0), \qquad v = (0, 1, 3).
$$

## Problem statement

For the given vectors $u = (1, 2, 0)$ and $v = (0, 1, 3)$:

1. Compute the cross product $u \times v$.
2. Use dot products to verify that $u \times v$ is perpendicular to both $u$ and $v$.
3. Compute the reversed cross product $v \times u$ directly.
4. Compare $u \times v$ and $v \times u$ both algebraically and geometrically (including their lengths, supporting line, and orientations).

---

## Step 1: Mechanism — The Cross Product in $\mathbb{R}^3$

For any two vectors $a = (a_1, a_2, a_3)$ and $b = (b_1, b_2, b_3)$ in $\mathbb{R}^3$, the **cross product** $a \times b$ is a vector in $\mathbb{R}^3$ defined via the formal $3 \times 3$ determinant expansion along the standard unit basis vectors $\mathbf{i} = (1, 0, 0)$, $\mathbf{j} = (0, 1, 0)$, and $\mathbf{k} = (0, 0, 1)$:

$$
a \times b =
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}\\
a_1 & a_2 & a_3\\
b_1 & b_2 & b_3
\end{vmatrix}
=
\begin{vmatrix} a_2 & a_3 \\ b_2 & b_3 \end{vmatrix}\mathbf{i}
-
\begin{vmatrix} a_1 & a_3 \\ b_1 & b_3 \end{vmatrix}\mathbf{j}
+
\begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix}\mathbf{k},
$$

which expands in component form to:

$$
a \times b = (a_2 b_3 - a_3 b_2,\ -(a_1 b_3 - a_3 b_1),\ a_1 b_2 - a_2 b_1).
$$

**Key geometric properties:**
- **Orthogonality:** Whenever $a$ and $b$ are not collinear, $a \times b$ is a nonzero vector perpendicular to both $a$ and $b$ (and thus normal to the plane spanned by $a$ and $b$).
- **Orientation (Right-Hand Rule):** Pointing the fingers of your right hand along $a$ and curling them toward $b$ through the smaller angle causes your thumb to point in the direction of $a \times b$.
- **Anticommutativity:** Swapping the order of the two arguments swaps two rows of the determinant, which reverses the sign: $b \times a = -(a \times b)$.

---

## Step 2: Compute $u \times v$

Substitute $u = (1, 2, 0)$ into the second row and $v = (0, 1, 3)$ into the third row of the determinant:

$$
\begin{aligned}
u \times v &=
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}\\
1 & 2 & 0\\
0 & 1 & 3
\end{vmatrix}\\[6pt]
&=
\begin{vmatrix} 2 & 0 \\ 1 & 3 \end{vmatrix}\mathbf{i}
-
\begin{vmatrix} 1 & 0 \\ 0 & 3 \end{vmatrix}\mathbf{j}
+
\begin{vmatrix} 1 & 2 \\ 0 & 1 \end{vmatrix}\mathbf{k}\\[6pt]
&= (2 \cdot 3 - 0 \cdot 1)\mathbf{i} - (1 \cdot 3 - 0 \cdot 0)\mathbf{j} + (1 \cdot 1 - 2 \cdot 0)\mathbf{k}\\[6pt]
&= 6\mathbf{i} - 3\mathbf{j} + 1\mathbf{k}\\[6pt]
&= (6, -3, 1).
\end{aligned}
$$

Therefore:

$$
\boxed{u \times v = (6, -3, 1)}
$$

---

## Step 3: Verify Perpendicularity Using Dot Products

First confirm that $u \times v = (6, -3, 1)$ is a nonzero vector by computing its length:

$$
\|u \times v\| = \sqrt{6^2 + (-3)^2 + 1^2} = \sqrt{36 + 9 + 1} = \sqrt{46} \neq 0.
$$

Now apply the orthogonality criterion ($x \perp y \iff x \cdot y = 0$) to test $u \times v$ against both $u$ and $v$:

1. **Dot product with $u = (1, 2, 0)$:**

   $$
   \begin{aligned}
   (u \times v) \cdot u &= (6, -3, 1) \cdot (1, 2, 0)\\
   &= 6 \cdot 1 + (-3) \cdot 2 + 1 \cdot 0\\
   &= 6 - 6 + 0\\
   &= 0. \quad \checkmark
   \end{aligned}
   $$

2. **Dot product with $v = (0, 1, 3)$:**

   $$
   \begin{aligned}
   (u \times v) \cdot v &= (6, -3, 1) \cdot (0, 1, 3)\\
   &= 6 \cdot 0 + (-3) \cdot 1 + 1 \cdot 3\\
   &= 0 - 3 + 3\\
   &= 0. \quad \checkmark
   \end{aligned}
   $$

Since both dot products equal $0$ and all three vectors are nonzero, $u \times v$ is confirmed to be perpendicular to both $u$ and $v$.

---

## Step 4: Compute $v \times u$

Place $v = (0, 1, 3)$ in the second row and $u = (1, 2, 0)$ in the third row of the determinant:

$$
\begin{aligned}
v \times u &=
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}\\
0 & 1 & 3\\
1 & 2 & 0
\end{vmatrix}\\[6pt]
&=
\begin{vmatrix} 1 & 3 \\ 2 & 0 \end{vmatrix}\mathbf{i}
-
\begin{vmatrix} 0 & 3 \\ 1 & 0 \end{vmatrix}\mathbf{j}
+
\begin{vmatrix} 0 & 1 \\ 1 & 2 \end{vmatrix}\mathbf{k}\\[6pt]
&= (1 \cdot 0 - 3 \cdot 2)\mathbf{i} - (0 \cdot 0 - 3 \cdot 1)\mathbf{j} + (0 \cdot 2 - 1 \cdot 1)\mathbf{k}\\[6pt]
&= -6\mathbf{i} + 3\mathbf{j} - 1\mathbf{k}\\[6pt]
&= (-6, 3, -1).
\end{aligned}
$$

Therefore:

$$
\boxed{v \times u = (-6, 3, -1)}
$$

---

## Step 5: Comparison of $u \times v$ and $v \times u$

1. **Algebraic relation (anticommutativity):**
   Comparing components directly shows that $v \times u$ is the exact additive inverse of $u \times v$:

   $$
   v \times u = (-6, 3, -1) = -1 \cdot (6, -3, 1) = -(u \times v).
   $$

   This reflects the determinant property that interchanging two rows multiplies the determinant by $-1$.

2. **Equal lengths (magnitudes):**
   Both vectors have the exact same Euclidean length:

   $$
   \|v \times u\| = \sqrt{(-6)^2 + 3^2 + (-1)^2} = \sqrt{36 + 9 + 1} = \sqrt{46} = \|u \times v\|.
   $$

   Geometrically, this shared length $\sqrt{46}$ equals the area of the parallelogram spanned by $u$ and $v$, which does not depend on the order of the two vectors.

3. **Same supporting normal line, opposite orientations:**
   Because $v \times u = -(u \times v)$, both vectors lie along the **exact same line** through the origin perpendicular to the plane spanned by $u$ and $v$ (indeed, $(v \times u) \cdot u = 0$ and $(v \times u) \cdot v = 0$ as well). However, swapping the order reverses the orientation by $180^\circ$ in accordance with the **right-hand rule**: curling fingers from $u$ to $v$ points the thumb in the direction $(6, -3, 1)$, whereas curling fingers from $v$ to $u$ points the thumb in the opposite direction $(-6, 3, -1)$.

---

## Summary Table

| Quantity | Calculation | Result | Geometric Meaning |
|---|---|---|---|
| $u \times v$ | $(2\cdot 3 - 0\cdot 1,\ -(1\cdot 3 - 0\cdot 0),\ 1\cdot 1 - 2\cdot 0)$ | $(6, -3, 1)$ | Normal vector via right-hand rule ($u \to v$) |
| $(u \times v) \cdot u$ | $6(1) + (-3)(2) + 1(0)$ | $0$ ✓ | $u \times v \perp u$ |
| $(u \times v) \cdot v$ | $6(0) + (-3)(1) + 1(3)$ | $0$ ✓ | $u \times v \perp v$ |
| $v \times u$ | $(1\cdot 0 - 3\cdot 2,\ -(0\cdot 0 - 3\cdot 1),\ 0\cdot 2 - 1\cdot 1)$ | $(-6, 3, -1)$ | Normal vector via right-hand rule ($v \to u$) |
| Comparison | $v \times u = -(u \times v)$, $\lVert v \times u \rVert = \lVert u \times v \rVert = \sqrt{46}$ | Opposite vectors | Same normal line & length, opposite orientation |

---

## Final Answer

$$
\boxed{
u \times v = (6, -3, 1), \qquad
v \times u = (-6, 3, -1) = -(u \times v)
}
$$

Both dot products $(u \times v) \cdot u = 0$ and $(u \times v) \cdot v = 0$ confirm perpendicularity. Reversing the order of the arguments preserves the vector's length ($\sqrt{46}$) and supporting normal line, but reverses its orientation ($v \times u = -(u \times v)$) by the right-hand rule.