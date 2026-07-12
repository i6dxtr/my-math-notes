#ch4 
- [[projection|projections]] can be found for both individual vectors as well as subspaces
- the *[[orthogonality|orthogonal]] projection* onto a subspace is especially important for least-squares minimization & data fitting

> [!definition]
> A vector $z\in V$ is said to be **orthogonal** to the subspace $W \subset V$ if it is orthogonal to every vector in $W$, so $\left\langle \mathbf{z}, \mathbf{w} \right\rangle=0$ for all $\mathbf{w}\in W$.
>
> The **orthogonal projection** of $\mathbf{v}$ onto the subspace $W$ is the element $\mathbf{w}\in W$ that makes the difference $\mathbf{z}=\mathbf{v}-\mathbf{w}$ orthogonal to $W$.

- where $W\subset V$ is a finite-dimensional subspace of a real inner product space
	- $V$ allowed to be infinite-dimensional, but just view $V=(\mathbb{R}^{m},\ \cdot)$
- $\mathbf{z}$ is orthogonal to $W$ if: 
	- $\mathbf{z}$ is orthogonal to every basis vector, which follows naturally from the fact that:
	- some scalar multiple of $\left\langle \mathbf{v}, \mathbf{w}_{i} \right\rangle$ is orthogonal to all vectors in $W$
		- since all $w\in\mathbf{w}$ are scalar multiples of the basis vectors ![[Pasted image 20241021105709.png| Orthogonal Projection of a Vector onto a Subspace]]
- $\mathbf{v}=\mathbf{w}+\mathbf{z}$ is the sum of its orthogonal projection $\mathbf{w}\in V$ and perp vector $\mathbf{z}\perp W$.
- orthogonal projection can be simplified by taking orthonormal basis of the subspace
	- apply [[Gram-Schmidt Process]]

> [!theorem]
> Let $\mathbf{u}_{1}, ..., \mathbf{u}_{n}$ be an orthonormal basis for the subspace $W\subset V$. Then the orthogonal projection of $\mathbf{v}\in V$ onto $\mathbf{w}\in W$ is given by:
> $$
> \begin{align}
> \mathbf{w}=c_{1}\mathbf{u}_{1}+\cdots+c_{n}\mathbf{u}_{n}&&\text{ where }&&c_{i}=\left\langle \mathbf{u},\mathbf{u}_{i} \right\rangle,\ \ i=1,...,n
> \end{align}
> $$

> [!proof]
> $\mathbf{u}_{1},...,\mathbf{u}_{n}$ form basis, so the orthogonal projection is some linear combination of it: $\mathbf{w}=c_{1}\mathbf{u}_{1}+\cdots+c_{n}\mathbf{u}_{n}$. We know $\mathbf{z}=\mathbf{v}-\mathbf{w}$ orthogonal to $W$, so it suffices to check orthogonality to the basis vectors:
> $$
> \begin{align}
> 0=\left\langle \mathbf{z}, \mathbf{u}_{i} \right\rangle&=\left\langle \mathbf{v}-\mathbf{w}, \mathbf{u}_{i} \right\rangle = \left\langle \mathbf{v}-c_{1}\mathbf{u}_{1}-\cdots-c_{n}\mathbf{u}_{n}, \mathbf{u}_{i} \right\rangle \\ &=\left\langle \mathbf{v}, \mathbf{u}_{i} \right\rangle-c_{1} \left\langle \mathbf{u}_{1},\mathbf{u}_{i}  \right\rangle-\cdots-c_{n}\left\langle \mathbf{u}_{n}, \mathbf{u}_{i} \right\rangle=\left\langle \mathbf{v}, \mathbf{u}_{i} \right\rangle-c_{i}
> \end{align}
> $$
> ... coefficients $c_{i}=\left\langle \mathbf{v}, \mathbf{u}_{i} \right\rangle$ of orth. proj $\mathbf{w}$ are uniquely given by orthogonality requirement, preserving uniqueness.

> [!remark]
> - employing orthogonal basis $\mathbf{v}_{1},...,\mathbf{v}_{n}$ for subspace $W$ derives a similar argument showing $\text{proj}_{W}(\mathbf{v})$ is given by:
> 	$$
> 	\begin{align}
> 	\mathbf{w}=a_{1}\mathbf{v}_{1}+\cdots+a_{n}\mathbf{v}_{n}&&\text{ where }&&a_{i}=\frac{\left\langle \mathbf{v}, \mathbf{v}_{i} \right\rangle }{\lvert \lvert \mathbf{v}_{i} \rvert  \rvert ^{2} },\ \ i=1,...,n
> 	\end{align}
> 	$$
> - we can derive a useful geometric interpretation of the Gram-Schmidt process as well: $$W_{k}=\text{span}\left\{ \mathbf{w}_{1}, ..., \mathbf{w}_{k} \right\}=\text{span}\left\{ \mathbf{v}_{1}, ..., \mathbf{v}_{k} \right\}=\text{span}\left\{ \mathbf{u}_{1}, ..., \mathbf{u}_{k} \right\}$$

