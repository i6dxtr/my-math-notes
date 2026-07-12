#ch2 
- serves to generalize geometrically the idea of two vectors spanning a plane in $\mathbb{R}^{3}$:

> [!definition]
> Let $\mathbf{v}_{1}, ..., \mathbf{v}_{k}$ be elements of a [[vector space]] $V$. A sum of the form $$c_{1}\mathbf{v}_{1}+c_{2}\mathbf{v}_{2}+...+c_{k}\mathbf{v}_{k}=\sum_{i=1}^{k}c_{i}\mathbf{v}_{i}$$ ... where the coefficients $c_{1}, c_{2},...,c_{k}$ are any scalars, is known as a *linear combination* of the elements $\mathbf{v}_{1}, ..., \mathbf{v}_{k}$. Their **span** is the subset $W=\text{span}\left\{ \mathbf{v}_{1}, ..., \mathbf{v}_{k} \right\}\subset V$ consisting of all possible linear combinations with scalars $c_{1}, ..., c_{k}\in\mathbb{R}$.

> [!corollary]
> The span $W=\text{span}\left\{ \mathbf{v}_{1}, ..., \mathbf{v}_{k} \right\}$ of any finite collection of vector space elements $\mathbf{v}_{1}, ..., \mathbf{v}_{k}\in V$ is a subspace of the underlying vector space $V$ *(p. 88)*.

- basically, the span always forms a [[Subspaces|subspace]] of a [[Vector Space|vector space]]

> [!corollary]
> A collection of $k$ vectors span $\mathbb{R}^{n}$ *if and only if* their $n \times k$ matrix has rank $n$, requiring $k\geq n$

> [!example]
> - If $\mathbf{v}_{1}\neq \mathbf{0}$ is any non-zero vector in $\mathbb{R}^{3}$, then its span is the line $\left\{ c\mathbf{v}_{1}\ |\ c\in\mathbb{R} \right\}$ consisting of all vectors parallel to $\mathbf{v}_{1}$. If $\mathbf{v}_{1}=\mathbf{0}$, then its span just contains the origin.
> - If we are given three non-coplanar vectors $\mathbf{v}_{1}, \mathbf{v}_{2}, \mathbf{v}_{3}$, then their span is all of $\mathbb{R}^{3}$. If they all lie in a plane, then their span is the plane, unless they're parallel; then, their span is a line. Or $\mathbf{0}$, if a single point.
> 	- we know which case is which when we observe the matrix of the vectors in [[Row Echelon Form]]

