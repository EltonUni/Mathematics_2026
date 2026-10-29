# Exercise 14: Rotation Matrices

**Problem Statement:**
Let $R(\theta)$ denote the $2 \times 2$ rotation matrix by an angle $\theta$:
$$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$$
1. Prove algebraically that $R(\alpha)R(\beta) = R(\alpha+\beta)$ for any angles $\alpha$ and $\beta$.
2. Provide a geometric explanation for this identity.

**Step-by-Step Explanation:**
1. **Setting up the Multiplication:**
   We multiply two rotation matrices, $R(\alpha)$ and $R(\beta)$:
   $$ R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix} $$

2. **Computing the Matrix Product:**
   We perform standard row-by-column multiplication:
   * Top-left entry: $(\cos\alpha)(\cos\beta) + (-\sin\alpha)(\sin\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
   * Top-right entry: $(\cos\alpha)(-\sin\beta) + (-\sin\alpha)(\cos\beta) = -(\sin\alpha\cos\beta + \cos\alpha\sin\beta)$
   * Bottom-left entry: $(\sin\alpha)(\cos\beta) + (\cos\alpha)(\sin\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$
   * Bottom-right entry: $(\sin\alpha)(-\sin\beta) + (\cos\alpha)(\cos\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
   
   The resulting matrix is:
   $$ \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \end{pmatrix} $$

3. **Applying Trigonometric Identities:**
   We use the standard angle-sum formulas for sine and cosine:
   * $\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
   * $\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$
   
   Substituting these identities into our matrix yields:
   $$ \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} $$
   This matches the exact definition of $R(\alpha+\beta)$.

**Final Result:**
- $R(\alpha)R(\beta) = R(\alpha+\beta)$
- **Geometrical Explanation:** Matrix multiplication corresponds to the composition of linear transformations. Rotating a vector by an angle $\beta$ first, and then rotating the result by an angle $\alpha$, is physically equivalent to applying a single rotation by the total combined angle $\alpha + \beta$.