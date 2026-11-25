# Exercise 1. Vector Operations and Their Meaning

## Given

Consider the two vectors in $\mathbb{R}^3$:

$$
u = (2, -1, 3), \qquad v = (-1, 4, 2).
$$

## Problem statement

Using the given vectors $u = (2, -1, 3)$ and $v = (-1, 4, 2)$:

1. Compute the vector sum $u + v$, the vector difference $u - v$, and the linear combination $3u - 2v$, showing the componentwise operations explicitly.
2. Verify by direct calculation that $(u + v) - v = u$, and state the algebraic property this illustrates.
3. Explain geometrically what adding two vectors means (using both the tip-to-tail rule and the parallelogram rule).

---

## Step 1: Mechanism — Componentwise Vector Operations

In $\mathbb{R}^3$, vector addition, subtraction, and scalar multiplication are defined **component by component**. For any vectors $a = (a_1, a_2, a_3)$ and $b = (b_1, b_2, b_3)$ and any scalar $c \in \mathbb{R}$:

$$
a + b = (a_1 + b_1,\ a_2 + b_2,\ a_3 + b_3),
$$

$$
a - b = (a_1 - b_1,\ a_2 - b_2,\ a_3 - b_3),
$$

$$
c\,a = (c\,a_1,\ c\,a_2,\ c\,a_3).
$$

---

## Step 2: Compute $u + v$

Add the corresponding components of $u = (2, -1, 3)$ and $v = (-1, 4, 2)$:

$$
\begin{aligned}
u + v &= (2 + (-1),\ -1 + 4,\ 3 + 2)\\
&= (2 - 1,\ -1 + 4,\ 3 + 2)\\
&= (1,\ 3,\ 5).
\end{aligned}
$$

Therefore:

$$
\boxed{u + v = (1, 3, 5)}
$$

---

## Step 3: Compute $u - v$

Subtract each component of $v = (-1, 4, 2)$ from the corresponding component of $u = (2, -1, 3)$:

$$
\begin{aligned}
u - v &= (2 - (-1),\ -1 - 4,\ 3 - 2)\\
&= (2 + 1,\ -1 - 4,\ 3 - 2)\\
&= (3,\ -5,\ 1).
\end{aligned}
$$

Therefore:

$$
\boxed{u - v = (3, -5, 1)}
$$

---

## Step 4: Compute $3u - 2v$

First, apply scalar multiplication to each vector separately:

$$
3u = 3(2, -1, 3) = (3\cdot 2,\ 3\cdot(-1),\ 3\cdot 3) = (6, -3, 9),
$$

$$
2v = 2(-1, 4, 2) = (2\cdot(-1),\ 2\cdot 4,\ 2\cdot 2) = (-2, 8, 4).
$$

Now subtract the resulting vectors component by component:

$$
\begin{aligned}
3u - 2v &= (6 - (-2),\ -3 - 8,\ 9 - 4)\\
&= (6 + 2,\ -3 - 8,\ 9 - 4)\\
&= (8,\ -11,\ 5).
\end{aligned}
$$

Therefore:

$$
\boxed{3u - 2v = (8, -11, 5)}
$$

---

## Step 5: Verify that $(u + v) - v = u$

Substitute the result $u + v = (1, 3, 5)$ from Step 2 and subtract $v = (-1, 4, 2)$:

$$
\begin{aligned}
(u + v) - v &= (1, 3, 5) - (-1, 4, 2)\\
&= (1 - (-1),\ 3 - 4,\ 5 - 2)\\
&= (1 + 1,\ 3 - 4,\ 5 - 2)\\
&= (2, -1, 3) = u. \quad \checkmark
\end{aligned}
$$

**Algebraic explanation:** Vector addition in $\mathbb{R}^3$ is associative, and $-v$ is the additive inverse of $v$ ($v + (-v) = \mathbf{0}$). Hence:

$$
(u + v) - v = u + (v - v) = u + \mathbf{0} = u.
$$

Subtracting $v$ exactly undoes the addition of $v$.

---

## Step 6: Geometric Meaning of Vector Addition

Geometrically, a vector represents a **displacement** (a shift with a specific direction and length). Adding two vectors $u$ and $v$ means combining two successive displacements into a single net displacement:

1. **Tip-to-tail (triangle) rule:** Place the tail (initial point) of $v$ at the tip (terminal point) of $u$. The sum $u + v$ is the directed segment starting at the tail of $u$ and ending at the tip of $v$. Moving along $u$ and then along $v$ brings you to the exact same position as moving directly along $u + v$.
2. **Parallelogram rule:** Place both $u$ and $v$ so that their tails start at the same point (such as the origin). Since $u$ and $v$ are not parallel, they span a parallelogram, and $u + v$ is the **main diagonal** starting from their common tail.
3. **Geometric meaning of $(u + v) - v = u$:** Since $-v$ has the same length as $v$ but points in the exact opposite direction, adding $-v$ to $u + v$ moves backward along the second side of the triangle, returning from the tip of $u + v$ directly back to the tip of $u$.

---

## Summary Table

| Operation | Componentwise Calculation | Result |
|---|---|---|
| $u + v$ | $(2 - 1,\ -1 + 4,\ 3 + 2)$ | $(1, 3, 5)$ |
| $u - v$ | $(2 + 1,\ -1 - 4,\ 3 - 2)$ | $(3, -5, 1)$ |
| $3u - 2v$ | $(6 + 2,\ -3 - 8,\ 9 - 4)$ | $(8, -11, 5)$ |
| $(u + v) - v$ | $(1 + 1,\ 3 - 4,\ 5 - 2)$ | $(2, -1, 3) = u$ ✓ |

---

## Final Answer

$$
\boxed{
u + v = (1, 3, 5), \qquad
u - v = (3, -5, 1), \qquad
3u - 2v = (8, -11, 5)
}
$$

Verification holds: $(u + v) - v = (2, -1, 3) = u$. Geometrically, $u + v$ represents the combined displacement obtained by placing $v$ tip-to-tail after $u$ (or taking the main diagonal of the parallelogram spanned by $u$ and $v$).