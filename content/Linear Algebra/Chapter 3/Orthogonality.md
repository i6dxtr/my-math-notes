#ch3
- essentially, the mathematical formalization of the [[geometric rep. of inner products|geometrical properties of perpendicularity]]

> [!definition]
> Two elements $\mathbf{v}, \mathbf{w}\in V$ of an inner product space $V$ are called **orthogonal** if their inner product vanishes: $\left\langle \mathbf{v}, \mathbf{w} \right\rangle=0$

- this condition is equivalent to saying that vectors $\mathbf{v}, \mathbf{w}$ are *perpendicular*:

> [!definition]
> If $V\subset\mathbb{R}^{n}$ such that $V$ is a subspace, the **perpendicular** is defined as $$V^{\perp}=\left\{ x\in  \mathbb{R}^{n}\ |\ x\cdot v=0\ \ \forall \mathbf{v}\in  V \right\}$$

### Properties of Orthogonality

> [!theorem]
> Let $\mathbf{v}_{1},..., \mathbf{v}_{k}\in V$ be nonzero, mutually orthogonal elements, so $$\mathbf{v}_{i}\neq 0\text{ and}\left\langle \mathbf{v}_{i}, \mathbf{v}_{j} \right\rangle=0\ \ \forall i\neq j$$ Then the set $\{\mathbf{v}_{1}, ..., \mathbf{v}_{k}\}$ is [[linear independence|linearly independent]].

- we can define their [[orthogonal bases]] accordingly
- meet at right angles: $\vartheta=\frac{1}{2}\pi$ or $\frac{3}{2}\pi$ with $\cos \vartheta=0$
- zero element is orthogonal to all other vectors: $\left\langle \mathbf{0}, \mathbf{v} \right\rangle=0\  \forall\mathbf{v}\in V$. 
![[vector_direction_relationship.png]]$$\mathbf{a}\cdot\mathbf{b}=\lvert \lvert \mathbf{a} \rvert  \rvert \ \lvert \lvert \mathbf{b} \rvert  \rvert \cos \vartheta=\mathbf{0}$$
- we can also derive the [[triangle inequality]] as a result

> [!remark] Remark: Importance of the Inner Product on Orthogonality
> The vectors $\mathbf{v}=(1,2)^{T}$ and $\mathbf{w}=(6, -3)^{T}$ are orthogonal with respect to the Euclidean dot product in $\mathbb{R}^{2}$, since $\mathbf{v}\cdot \mathbf{w}=1\cdot 6+2\cdot (-3)=0$. Therefore, they meet at a right angle. However, they aren't orthogonal w/ respect to the weighted inner product:
> $$
> \left\langle \mathbf{v}, \mathbf{w} \right\rangle=\left\langle
> \begin{pmatrix}
> 1\\2
> \end{pmatrix},
> \begin{pmatrix}
> 6\\-3
> \end{pmatrix}\right\rangle=2\cdot1\cdot6+5\cdot2\cdot(-3)=-18\neq 0
> $$
> ... thus, the property of orthogonality (like angles in general) depend upon which inner product is being used

> [!theorem] Theorem: Orthogonal Basis
> Suppose $\mathbf{v}_{1}, ..., \mathbf{v}_{n}\in V$ are nonzero, mutually orthogonal elements of an inner product space $V$. Then $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ form an *orthogonal basis* for their span $W=\text{span }\left\{ \mathbf{v}_{1}, ..., \mathbf{v}_{n} \right\}\subset V$, which is therefore a subspace of dimension $n=\text{dim }W$. In particular, if $\text{dim}\ {V}=n$ then $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ form an orthogonal basis for $V$.

> [!remark]
> Observe vector space $V$. $V^{\perp}$ is the set of vectors perpendicular to all vectors in $V$.
> It has the following properties:
> 1. $V\cap V^{\perp}=\mathbf{0}$, which means they're completely orthogonal
> 2. $\text{span}\left\{ V, V^{\perp} \right\}=\mathbb{R}^{n}$, meaning their span is defined
> 3. $\text{dim}(V)+\text{dim}(V^{\perp})=n$

*Claim.* Given $A$, the null space of $A^{T}$ is equal to the transpose of the column space of $A$. $$\text{null}(A^{\perp})=\text{col}(A)^{\perp}$$
   *Proof.* Let $\mathbf{x}\in \text{null}(A^{T})$
1. then $A^{T}\mathbf{x}=\mathbf{0}$
2. $\longrightarrow A^{T}\mathbf{x}\cdot\mathbf{y}=0$
3. $\longrightarrow \mathbf{x}\cdot A\mathbf{y}=0$
4. ... meaning, $\mathbf{x}$ is orthogonal to every vector in $\text{col}(A)^{\perp}$
5. $\rightarrow \mathbf{x}\in \text{col}(A)^{\perp}$

link: [[linear independence]]