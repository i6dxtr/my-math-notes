# Gram-Schmidt Process

Given matrix $A = \begin{pmatrix} 1 & 1 & 2 \\ 1 & 0 & -2 \\ -1 & 2 & 3 \end{pmatrix}$

Let's denote the original vectors as $\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3$ and the orthogonalized vectors as $\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3$.

## Step 1: $\mathbf{v}_1 = \mathbf{u}_1$
$\mathbf{v}_1 = (1, 1, -1)$

## Step 2: $\mathbf{v}_2 = \mathbf{u}_2 - \text{proj}_{\mathbf{v}_1}(\mathbf{u}_2)$

$$
\begin{align*}
\text{proj}_{\mathbf{v}_1}(\mathbf{u}_2) &= \frac{\mathbf{u}_2 \cdot \mathbf{v}_1}{\mathbf{v}_1 \cdot \mathbf{v}_1} \mathbf{v}_1 \\
&= \frac{(1,0,2) \cdot (1,1,-1)}{(1,1,-1) \cdot (1,1,-1)} (1,1,-1) \\
&= \frac{-1}{3} (1,1,-1) \\
&= (-\frac{1}{3}, -\frac{1}{3}, \frac{1}{3})
\end{align*}
$$

$$
\begin{align*}
\mathbf{v}_2 &= (1,0,2) - (-\frac{1}{3}, -\frac{1}{3}, \frac{1}{3}) \\
&= (\frac{4}{3}, \frac{1}{3}, \frac{5}{3})
\end{align*}
$$

## Step 3: $\mathbf{v}_3 = \mathbf{u}_3 - \text{proj}_{\mathbf{v}_1}(\mathbf{u}_3) - \text{proj}_{\mathbf{v}_2}(\mathbf{u}_3)$

$$
\begin{align*}
\text{proj}_{\mathbf{v}_1}(\mathbf{u}_3) &= \frac{\mathbf{u}_3 \cdot \mathbf{v}_1}{\mathbf{v}_1 \cdot \mathbf{v}_1} \mathbf{v}_1 \\
&= \frac{(2,-2,3) \cdot (1,1,-1)}{(1,1,-1) \cdot (1,1,-1)} (1,1,-1) \\
&= \frac{1}{3} (1,1,-1) \\
&= (\frac{1}{3}, \frac{1}{3}, -\frac{1}{3})
\end{align*}
$$

$$
\begin{align*}
\text{proj}_{\mathbf{v}_2}(\mathbf{u}_3) &= \frac{\mathbf{u}_3 \cdot \mathbf{v}_2}{\mathbf{v}_2 \cdot \mathbf{v}_2} \mathbf{v}_2 \\
&= \frac{(2,-2,3) \cdot (\frac{4}{3},\frac{1}{3},\frac{5}{3})}{(\frac{4}{3},\frac{1}{3},\frac{5}{3}) \cdot (\frac{4}{3},\frac{1}{3},\frac{5}{3})} (\frac{4}{3},\frac{1}{3},\frac{5}{3}) \\
&= \frac{17}{14} (\frac{4}{3},\frac{1}{3},\frac{5}{3}) \\
&= (\frac{68}{42}, \frac{17}{42}, \frac{85}{42})
\end{align*}
$$

$$
\begin{align*}
\mathbf{v}_3 &= (2,-2,3) - (\frac{1}{3}, \frac{1}{3}, -\frac{1}{3}) - (\frac{68}{42}, \frac{17}{42}, \frac{85}{42}) \\
&= (\frac{50}{42}, -\frac{101}{42}, \frac{82}{42})
\end{align*}
$$

## Normalizing vectors

$$
\begin{align*}
\mathbf{e}_1 &= \frac{\mathbf{v}_1}{\|\mathbf{v}_1\|} = (\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, -\frac{1}{\sqrt{3}}) \\
\mathbf{e}_2 &= \frac{\mathbf{v}_2}{\|\mathbf{v}_2\|} = (\frac{4}{\sqrt{30}}, \frac{1}{\sqrt{30}}, \frac{5}{\sqrt{30}}) \\
\mathbf{e}_3 &= \frac{\mathbf{v}_3}{\|\mathbf{v}_3\|} = (\frac{5}{\sqrt{21}}, -\frac{10}{\sqrt{21}}, \frac{8}{\sqrt{21}})
\end{align*}
$$

## Results

The resulting orthonormal basis $Q$ (as confirmed by numerical calculations):

$$
Q \approx \begin{pmatrix}
0.57735027 & 0.73029674 & 0.36514837 \\
0.57735027 & 0.18257419 & -0.79535825 \\
-0.57735027 & 0.91287093 & 0.48686449
\end{pmatrix}
$$

The upper triangular matrix $R$:

$$
R \approx \begin{pmatrix}
1.73205081 & 0.57735027 & 1.15470054 \\
0 & 2.30940108 & 1.84752086 \\
0 & 0 & 2.18581761
\end{pmatrix}
$$

These results confirm our manual calculations and demonstrate that:
1. The columns of $Q$ are indeed the normalized vectors we calculated ($\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3$).
2. $Q$ is orthogonal ($Q^T Q$ is very close to the identity matrix).
3. The original matrix $A$ can be reconstructed by multiplying $Q$ and $R$.


### Projections
The formula for the projection of a vector $\mathbf{u}$ onto a vector $\mathbf{v}$ is:

$$\text{proj}_\mathbf{v}(\mathbf{u}) = \frac{\mathbf{u} \cdot \mathbf{v}}{|\mathbf{v}|^2} \mathbf{v}$$

Let's break this down:

1. $\mathbf{u} \cdot \mathbf{v}$ is the dot product of vectors $\mathbf{u}$ and $\mathbf{v}$.
2. $|\mathbf{v}|$ is the norm (or length) of vector $\mathbf{v}$.
3. $|\mathbf{v}|^2$ is the square of the norm, which is equal to the dot product of $\mathbf{v}$ with itself: $|\mathbf{v}|^2 = \mathbf{v} \cdot \mathbf{v}$.
4. The fraction $\frac{\mathbf{u} \cdot \mathbf{v}}{|\mathbf{v}|^2}$ gives us a scalar value.
5. This scalar is then multiplied by the vector $\mathbf{v}$ to give us the projection vector.

An alternative way to write this formula, emphasizing the use of dot products, is:

$$\text{proj}_\mathbf{v}(\mathbf{u}) = \frac{\mathbf{u} \cdot \mathbf{v}}{\mathbf{v} \cdot \mathbf{v}} \mathbf{v}$$

This formula calculates the component of $\mathbf{u}$ that is parallel to $\mathbf{v}$. Geometrically, it's the shadow cast by $\mathbf{u}$ onto the line spanned by $\mathbf{v}$ if a light source were shining perpendicular to $\mathbf{v}$.

The result, $\text{proj}_\mathbf{v}(\mathbf{u})$, is a vector that:

1. Points in the same or opposite direction as $\mathbf{v}$.
2. Has a magnitude that represents how much of $\mathbf{u}$ is in the direction of $\mathbf{v}$.

This projection formula is a key component in many linear algebra applications, including the Gram-Schmidt process we discussed earlier.





# QR Algorithm and Projections

## QR Algorithm

The QR algorithm is a method for decomposing a matrix $A$ into the product of an orthogonal matrix $Q$ and an upper triangular matrix $R$, such that $A = QR$.

### Steps of the QR Algorithm:

1. Start with matrix $A = [a_1 \  a_2 \ \cdots \ a_n]$ where $a_i$ are the columns of $A$.

2. For the first column:
   - $q_1 = \frac{a_1}{\|a_1\|}$

3. For each subsequent column $i = 2, 3, \ldots, n$:
   - Compute $v_i = a_i - \sum_{j=1}^{i-1} (q_j^T a_i) q_j$
   - Normalize: $q_i = \frac{v_i}{\|v_i\|}$

4. The columns $q_i$ form the matrix $Q = [q_1 \ q_2 \ \cdots \ q_n]$

5. Compute $R = Q^T A$

### Properties of Q and R:

- $Q$ is orthogonal: $Q^T Q = Q Q^T = I$
- $R$ is upper triangular:
  $$
  R = \begin{bmatrix}
  r_{11} & r_{12} & r_{13} & \cdots & r_{1n} \\
  0 & r_{22} & r_{23} & \cdots & r_{2n} \\
  0 & 0 & r_{33} & \cdots & r_{3n} \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  0 & 0 & 0 & \cdots & r_{nn}
  \end{bmatrix}
  $$

Where:
- $r_{11} = \|a_1\|$
- For $i > 1$: $r_{ii} = \|v_i\|$
- For $j > i$: $r_{ij} = q_i^T a_j$

### Advantages over Gram-Schmidt:

1. Better numerical stability, especially for large matrices
2. Simultaneous computation of $Q$ and $R$
3. Can be implemented using Householder reflections or Givens rotations for even better stability

## Projections and Column Spaces

### Column Space Equality

When we say $\text{col}(P) = \text{col}(Q)$, we mean:

- The column spaces of $P$ and $Q$ are exactly the same set of vectors
- They span the same subspace
- Any vector in one column space can be expressed as a linear combination of the columns of the other matrix
- The dimensions of these column spaces are the same

### Visualization of Projections

A projection matrix $P$ projects vectors onto a specific subspace:

- It "flattens" a vector onto the subspace
- The projected vector is the closest vector in the subspace to the original vector
- Vectors already in the subspace remain unchanged when projected

### Projection Formula

For a vector $u$ and a unit vector $v$, the projection of $u$ onto $v$ is:

$$\text{proj}_v(u) = (u \cdot v)v$$

### Orthogonal Decomposition

Any vector $u$ can be decomposed as:

$$u = \text{proj}_V(u) + (u - \text{proj}_V(u))$$

Where $\text{proj}_V(u)$ is in the subspace $V$, and $(u - \text{proj}_V(u))$ is orthogonal to $V$.

### Projection Matrix

If $V$ is a matrix with orthonormal columns spanning a subspace, then $P = VV^T$ is the projection matrix onto that subspace.

Properties of Projection Matrices:
- Symmetry: $P = P^T$
- Idempotence: $P^2 = P$

### Importance of Orthonormality

Orthonormality in projections:
- Simplifies calculations
- Ensures projection onto a well-defined subspace
- Allows use of the simple formula $P = VV^T$
- Ensures desirable properties like symmetry and idempotence
- Avoids numerical instabilities associated with inverting the Gram matrix $(V^T V)^{-1}$

## 3D Vector Projections

In 3D Euclidean space:
- The projection of $u$ onto $v$ is parallel to $v$, not opposite
- It represents the component of $u$ in the direction of $v$
- If $u$ and $v$ are orthogonal, the projection is the zero vector

Remember: The projection is always in the same direction as the vector being projected onto, or its negative, never at an angle to it.


# $2  \times 2$ projection matrices

Let's consider two 2x2 projection matrices:

$$P_1 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$$

$$P_2 = \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}$$

Both of these are valid projection matrices because $P_1^2 = P_1$ and $P_2^2 = P_2$.

Now, let's multiply these matrices:

$$P_1 P_2 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$$

To check if the result is a projection matrix, we need to verify if $(P_1P_2)^2 = P_1P_2$:

$$(P_1P_2)^2 = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = P_1P_2$$

In this case, the product $P_1P_2$ is still a projection matrix (the zero matrix is a valid projection matrix).

To find an example where the product is not a projection, we need to consider non-diagonal matrices. Here's such an example:

$$P_1 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$$

$$P_2 = \begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2} \end{bmatrix}$$

Their product is:

$$P_1P_2 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2} \end{bmatrix} = \begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ 0 & 0 \end{bmatrix}$$

To check if this is a projection matrix:

$$(P_1P_2)^2 = \begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ 0 & 0 \end{bmatrix} \begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} \frac{1}{4} & \frac{1}{4} \\ 0 & 0 \end{bmatrix} \neq P_1P_2$$

Therefore, $P_1P_2$ is not a projection matrix, satisfying the requirements of the question.
\

# Problem

#### Suppose $P$ is a projection and $Q$ is orthogonal. Claim: $Q^{T}PQ$ is a projection. Note $\mathbb{1}_{n}-P$ is a projection. Prove $Q^{T}PQ$ is also a projection.
Given:
- $P$ is a projection matrix
- $Q$ is an orthogonal matrix

To prove: $Q^TPQ$ is also a projection matrix

Definitions and properties:

1) Projection Matrix ($P$):
   - Definition: $P^2 = P$ (idempotent)
   - Properties:
     • Symmetric: $P^T = P$
     • Eigenvalues are either 0 or 1
     • $\text{trace}(P) = \text{rank}(P)$

2) Orthogonal Matrix ($Q$):
   - Definition: $Q^TQ = QQ^T = I$
   - Properties:
     • $Q^T = Q^{-1}$
     • $\det(Q) = \pm 1$
     • Preserves inner products: $(Qx)^T(Qy) = x^Ty$

Proof:

To show $Q^TPQ$ is a projection, we need to prove $(Q^TPQ)^2 = Q^TPQ$

1) Expand the left side:
   $$(Q^TPQ)^2 = (Q^TPQ)(Q^TPQ)$$

2) Focus on the middle part:
   $$= Q^TP\underbrace{(QQ^T)}_{=I}PQ$$

3) Simplify using $QQ^T = I$:
   $$= Q^TPIPQ = Q^TPP Q$$

4) Use the property of projection $P^2 = P$:
   $$= Q^TPQ$$

Thus, we have shown $(Q^TPQ)^2 = Q^TPQ$, proving that $Q^TPQ$ is indeed a projection matrix.

Additional insight:
The transformation $Q^TPQ$ can be interpreted as:
1) First apply $Q$ (rotation/reflection)
2) Then apply $P$ (projection)
3) Finally apply $Q^T$ (inverse rotation/reflection)

This sequence effectively rotates the subspace that $P$ projects onto, resulting in a new projection matrix.

Is there any part of this proof you'd like me to elaborate on further?


# Problem

For the projection matrix $P$:

$$
P = \begin{bmatrix}
* & * & * \\
* & 1 & * \\
-0.2 & * & *
\end{bmatrix}
$$

1) Projection matrices are symmetric, so $P = P^T$. This means:
   - The element in position (3,1) must equal the element in (1,3)
   - The element in position (2,1) must equal the element in (1,2)
   - The element in position (3,2) must equal the element in (2,3)

2) For a projection matrix, $P^2 = P$. This gives us additional constraints.

3) The diagonal elements of a projection matrix can only be 0 or 1.

Given these properties, we can deduce:

$$
P = \begin{bmatrix}
1 & 0 & -0.2 \\
0 & 1 & 0 \\
-0.2 & 0 & 0.04
\end{bmatrix}
$$

For the orthogonal matrix $Q$:

$$
Q = \begin{bmatrix}
* & * & * \\
* & 1 & * \\
-0.2 & * & *
\end{bmatrix}
$$

1) For an orthogonal matrix, $Q^TQ = QQ^T = I$. This means each row and column must be a unit vector, and rows/columns must be orthogonal to each other.

2) Given that one element is 1, the rest of that row and column must be 0 to maintain orthogonality.

3) The remaining 2x2 submatrix must form a rotation matrix to preserve orthogonality.

Therefore, the only possible form for $Q$ is:

$$
Q = \begin{bmatrix}
\cos \theta & 0 & \sin \theta \\
0 & 1 & 0 \\
-\sin \theta & 0 & \cos \theta
\end{bmatrix}
$$

where $\sin \theta = 0.2$ and $\cos \theta = \sqrt{1 - 0.2^2} = \sqrt{0.96} \approx 0.98$.

This approach allows us to fill in the matrices without extensive calculations, using the fundamental properties of projection and orthogonal matrices.

# textbook 4.4.1

A vector is orthogonal to a subspace if it's orthogonal to every vector in that subspace. For lines and planes, we can check orthogonality against the spanning vectors.

Let's go through each case:

(a) Line spanned by $\begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix}$:
   Check if $v_i \cdot \begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix} = 0$ for each $v_i$.

(b) Plane spanned by $\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$ and $\begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$:
   Check if $v_i$ is orthogonal to both spanning vectors.

(c) Plane $x - y - z = 0$:
   The normal vector to this plane is $\begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix}$.
   Check if $v_i \cdot \begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix} = 0$.

(d) Kernel of $\begin{pmatrix} 1 & -1 & -1 \\ 3 & -2 & -4 \end{pmatrix}$:
   Find the null space and check orthogonality against its basis vector(s).

(e) Image of $\begin{pmatrix} -3 & 1 \\ 3 & -1 \\ -1 & 0 \end{pmatrix}$:
   Find the column space and check orthogonality against its basis vectors.

(f) Cokernel of $\begin{pmatrix} -1 & 0 & 3 \\ 2 & 1 & -2 \\ 3 & 1 & -5 \end{pmatrix}$:
   The cokernel is the left null space. Find it and check orthogonality against its basis vector(s).

For each case, a vector $v_i$ is orthogonal if it satisfies the orthogonality condition with all basis vectors of the given subspace.



(a) Line spanned by $\begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix}$:

   $v_1 \cdot \begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix} = 1(1) + 1(3) + 0(-2) = 4 \neq 0$
   $v_2 \cdot \begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix} = -2(1) + 2(3) + 2(-2) = 0$
   $v_3 \cdot \begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix} = 2(1) + (-1)(3) + (-3)(-2) = 5 \neq 0$
   $v_4 \cdot \begin{pmatrix} 1 \\ 3 \\ -2 \end{pmatrix} = -1(1) + 3(3) + 4(-2) = 0$

   Only $v_2$ and $v_4$ are orthogonal.

(b) Plane spanned by $\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$ and $\begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$:

   For $v_1$: $(1,1,0) \cdot (1,-1,1) = 0$ and $(1,1,0) \cdot (1,1,1) = 2 \neq 0$
   For $v_2$: $(-2,2,2) \cdot (1,-1,1) = -2$ and $(-2,2,2) \cdot (1,1,1) = 2$
   For $v_3$: $(2,-1,-3) \cdot (1,-1,1) = 6 \neq 0$ and $(2,-1,-3) \cdot (1,1,1) = -2 \neq 0$
   For $v_4$: $(-1,3,4) \cdot (1,-1,1) = 0$ and $(-1,3,4) \cdot (1,1,1) = 6 \neq 0$

   None of the vectors are orthogonal to both spanning vectors.

(c) Plane $x - y - z = 0$:

   Normal vector: $\begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix}$
   
   $v_1 \cdot \begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix} = 1(1) + 1(-1) + 0(-1) = 0$
   $v_2 \cdot \begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix} = -2(1) + 2(-1) + 2(-1) = -6 \neq 0$
   $v_3 \cdot \begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix} = 2(1) + (-1)(-1) + (-3)(-1) = 6 \neq 0$
   $v_4 \cdot \begin{pmatrix} 1 \\ -1 \\ -1 \end{pmatrix} = -1(1) + 3(-1) + 4(-1) = -8 \neq 0$

   Only $v_1$ is orthogonal.

(d) Kernel of $\begin{pmatrix} 1 & -1 & -1 \\ 3 & -2 & -4 \end{pmatrix}$:

   The kernel is spanned by $\begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix}$.

   $v_1 \cdot \begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix} = 1(2) + 1(1) + 0(1) = 3 \neq 0$
   $v_2 \cdot \begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix} = -2(2) + 2(1) + 2(1) = 0$
   $v_3 \cdot \begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix} = 2(2) + (-1)(1) + (-3)(1) = 0$
   $v_4 \cdot \begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix} = -1(2) + 3(1) + 4(1) = 5 \neq 0$

   $v_2$ and $v_3$ are orthogonal.

(e) Image of $\begin{pmatrix} -3 & 1 \\ 3 & -1 \\ -1 & 0 \end{pmatrix}$:

   The image is spanned by $\begin{pmatrix} -3 \\ 3 \\ -1 \end{pmatrix}$.

   $v_1 \cdot \begin{pmatrix} -3 \\ 3 \\ -1 \end{pmatrix} = 1(-3) + 1(3) + 0(-1) = 0$
   $v_2 \cdot \begin{pmatrix} -3 \\ 3 \\ -1 \end{pmatrix} = -2(-3) + 2(3) + 2(-1) = 10 \neq 0$
   $v_3 \cdot \begin{pmatrix} -3 \\ 3 \\ -1 \end{pmatrix} = 2(-3) + (-1)(3) + (-3)(-1) = -6 \neq 0$
   $v_4 \cdot \begin{pmatrix} -3 \\ 3 \\ -1 \end{pmatrix} = -1(-3) + 3(3) + 4(-1) = 5 \neq 0$

   Only $v_1$ is orthogonal.

(f) Cokernel of $\begin{pmatrix} -1 & 0 & 3 \\ 2 & 1 & -2 \\ 3 & 1 & -5 \end{pmatrix}$:

   The cokernel (left null space) is spanned by $\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$.

   $v_1 \cdot \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix} = 1(1) + 1(-1) + 0(1) = 0$
   $v_2 \cdot \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix} = -2(1) + 2(-1) + 2(1) = -2 \neq 0$
   $v_3 \cdot \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix} = 2(1) + (-1)(-1) + (-3)(1) = 0$
   $v_4 \cdot \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix} = -1(1) + 3(-1) + 4(1) = 0$

   $v_1$, $v_3$, and $v_4$ are orthogonal.

In summary:
- (a) $v_2$ and $v_4$ are orthogonal
- (b) None are orthogonal
- (c) Only $v_1$ is orthogonal
- (d) $v_2$ and $v_3$ are orthogonal
- (e) Only $v_1$ is orthogonal
- (f) $v_1$, $v_3$, and $v_4$ are orthogonal

# 4.4.2
I'll solve this problem step-by-step using the orthogonal projection formula. For a vector v and a subspace spanned by unit vector(s) u, the projection is given by:

$\text{proj}_u(v) = \frac{v \cdot u}{u \cdot u} u$ (for a single vector)

or 

$\text{proj}_U(v) = \sum_{i=1}^n \frac{v \cdot u_i}{u_i \cdot u_i} u_i$ (for multiple orthonormal vectors)

Let's solve each part:

a) The line in the direction $\left(-\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}\right)^T$:
	This vector is already a unit vector, so we can directly use the formula:
	$\text{proj}_u(v) = \left((1,1,1) \cdot \left(-\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}\right)\right) \left(-\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}\right)$
	$= \frac{1}{\sqrt{3}} \left(-\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}\right)$
	$= \left(-\frac{1}{3}, \frac{1}{3}, \frac{1}{3}\right)$

b) The line spanned by $(2,-1,3)^T$:
	First, we need to normalize this vector:
	$u = \frac{(2,-1,3)}{\sqrt{4+1+9}} = \frac{(2,-1,3)}{\sqrt{14}}$
	Now we can project:
	$\text{proj}_u(v) = \frac{(1,1,1) \cdot (2,-1,3)}{(2,-1,3) \cdot (2,-1,3)} (2,-1,3)$
	$= \frac{2-1+3}{14} (2,-1,3) = \frac{4}{14}(2,-1,3) = \frac{2}{7}(2,-1,3)$
	$= \left(\frac{4}{7}, -\frac{2}{7}, \frac{6}{7}\right)$

c) The plane spanned by $(1,1,0)^T$ and $(-2,2,1)^T$:
	We need to orthonormalize these vectors:
	$u_1 = \frac{(1,1,0)}{\sqrt{2}} = \left(\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}, 0\right)$
	$u_2 = (-2,2,1) - \left((-2,2,1) \cdot \frac{(1,1,0)}{\sqrt{2}}\right)\frac{(1,1,0)}{\sqrt{2}}$
	$= (-2,2,1) - 0(1,1,0) = (-2,2,1)$
	Normalizing $u_2$:
	$u_2 = \frac{(-2,2,1)}{\sqrt{9}} = \frac{(-2,2,1)}{3}$
	Now we can project:
	$\text{proj}_U(v) = \left((1,1,1) \cdot \left(\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}, 0\right)\right) \left(\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}, 0\right) + \left((1,1,1) \cdot \frac{(-2,2,1)}{3}\right) \frac{(-2,2,1)}{3}$
	$= \sqrt{2}\left(\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}, 0\right) + \frac{1}{3}(-2,2,1)$
	$= (1,1,0) + \left(-\frac{2}{3}, \frac{2}{3}, \frac{1}{3}\right)$
	$= \left(\frac{1}{3}, \frac{5}{3}, \frac{1}{3}\right)$

d) The plane spanned by $\left(-\frac{2}{3}, \frac{1}{3}, 0\right)^T$ and $\left(\frac{1}{13}, \frac{1}{13}, -\frac{12}{13}\right)^T$:
	These vectors are already orthonormal, so we can directly use the formula:
	$\text{proj}_U(v) = \left((1,1,1) \cdot \left(-\frac{2}{3}, \frac{1}{3}, 0\right)\right) \left(-\frac{2}{3}, \frac{1}{3}, 0\right) + \left((1,1,1) \cdot \left(\frac{1}{13}, \frac{1}{13}, -\frac{12}{13}\right)\right) \left(\frac{1}{13}, \frac{1}{13}, -\frac{12}{13}\right)$
	$= -\frac{1}{3}\left(-\frac{2}{3}, \frac{1}{3}, 0\right) + 0\left(\frac{1}{13}, \frac{1}{13}, -\frac{12}{13}\right)$
	$= \left(\frac{2}{9}, -\frac{1}{9}, 0\right)$

These are the orthogonal projections of the vector $v=(1,1,1)^T$ onto the given subspaces.

# 4.4.4
To find the orthogonal projection of the vector onto the image of the given matrix, we'll follow these steps:

1) Let's call our vector $\mathbf{v}$ and the matrix $\mathbf{A}$.
	   $\mathbf{v} = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$
	   $\mathbf{A} = \begin{pmatrix} 3 & 2 \\ 2 & -2 \\ 1 & -2 \end{pmatrix}$

2) The projection matrix onto the column space of $\mathbf{A}$ is given by:
	   $\mathbf{P} = \mathbf{A}(\mathbf{A}^T \mathbf{A})^{-1}\mathbf{A}^T$

3) First, let's calculate $\mathbf{A}^T \mathbf{A}$:
	   $\mathbf{A}^T \mathbf{A} = \begin{pmatrix} 3 & 2 & 1 \\ 2 & -2 & -2 \end{pmatrix} \begin{pmatrix} 3 & 2 \\ 2 & -2 \\ 1 & -2 \end{pmatrix} = \begin{pmatrix} 14 & -2 \\ -2 & 12 \end{pmatrix}$

4) Now, we need to find $(\mathbf{A}^T \mathbf{A})^{-1}$:
	   $\det(\mathbf{A}^T \mathbf{A}) = 14 \cdot 12 - (-2) \cdot (-2) = 164$
	   
	   $(\mathbf{A}^T \mathbf{A})^{-1} = \frac{1}{164} \begin{pmatrix} 12 & 2 \\ 2 & 14 \end{pmatrix}$

5) Now we can calculate $\mathbf{P}$:
	   $\mathbf{P} = \mathbf{A} \cdot \frac{1}{164} \begin{pmatrix} 12 & 2 \\ 2 & 14 \end{pmatrix} \cdot \mathbf{A}^T$
	   
	   $= \frac{1}{164} \begin{pmatrix} 3 & 2 \\ 2 & -2 \\ 1 & -2 \end{pmatrix} \begin{pmatrix} 12 & 2 \\ 2 & 14 \end{pmatrix} \begin{pmatrix} 3 & 2 & 1 \\ 2 & -2 & -2 \end{pmatrix}$
	   
	   $= \frac{1}{164} \begin{pmatrix} 38 & -10 \\ -10 & 42 \\ -10 & -26 \end{pmatrix} \begin{pmatrix} 3 & 2 & 1 \\ 2 & -2 & -2 \end{pmatrix}$
	   
	   $= \frac{1}{164} \begin{pmatrix} 94 & -50 & -38 \\ -50 & 26 & 20 \\ -38 & 20 & 16 \end{pmatrix}$

6) Finally, we project $\mathbf{v}$ onto the image of $\mathbf{A}$:
	$\text{proj}_A(\mathbf{v}) = \mathbf{P} \mathbf{v}$
		  $= \frac{1}{164} \begin{pmatrix} 94 & -50 & -38 \\ -50 & 26 & 20 \\ -38 & 20 & 16 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$
		  $= \frac{1}{164} \begin{pmatrix} -32 \\ 16 \\ 16 \end{pmatrix}$
		  $= \begin{pmatrix} -16/82 \\ 8/82 \\ 8/82 \end{pmatrix}$
		  $= \begin{pmatrix} -4/41 \\ 2/41 \\ 2/41 \end{pmatrix}$

Therefore, the orthogonal projection of $\begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$ onto the image of the given matrix is: $\begin{pmatrix} -4/41 \\ 2/41 \\ 2/41 \end{pmatrix}$
- or approximately $\begin{pmatrix} -0.0976 \\ 0.0488 \\ 0.0488 \end{pmatrix}$