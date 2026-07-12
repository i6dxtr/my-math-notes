#ch4 
- conceptually, [[Orthogonality|orthogonality]] can be applied from individual elements to entire subspaces of an inner product space $V$:

> [!definition]
> Two subspaces $W,Z\subset V$ are called *orthogonal* if every vector in $W$ is orthogonal to every vector in $Z$.

- only really need to check orthogonality of the basis elements (more generally, spanning sets)

> [!corollary] Lemma.
> If $\mathbf{w}_{1}, ..., \mathbf{w}_{k}$ span $W$ and $\mathbf{z}_{1}, ..., \mathbf{z}_{l}$ span $Z$, then $W,Z$ are orthogonal subspaces *if and only if* $\left\langle \mathbf{w}_{i} , \mathbf{z}_{j} \right\rangle\ \ \forall i=1, ..., k \wedge j=1, ..., l$. 
> Equivalently, $$W,Z\text{ are orthogonal subspaces}\Longleftrightarrow\left\langle \mathbf{w}, \mathbf{z} \right\rangle=0\ \forall \mathbf{w}\in W \wedge \forall \mathbf{z}\in Z$$

> [!example]
> Where $V=\mathbb{R}^{3}$, take plane $W\subset\mathbb{R}^{3}$ defined by equation $2x-y+3z=0$ is orthogonal to the line $Z$ spanned by normal vector $\mathbf{n}=(2,-1,3)^{T}$. Then every $\mathbf{w}=(x,y,z)^{T}\in W$ satisfies orthogonality condition $\mathbf{w}\cdot\mathbf{n}=2x-y+3z=0$, simply the equation for the plane.

> [!definition]
> The **orthogonal complement** of a subspace $W\subset V$, denoted $W^{\perp}$, is defined as the set of all vectors that are orthogonal to $W$: $$W^{\perp}=\left\{ \mathbf{v}\in  V\ |\ \left\langle \mathbf{v}, \mathbf{w} \right\rangle=0\ \ \forall \mathbf{w}\in  W\right\}.$$

- note that $W\cap W^{\perp}$

> [!example]
> Let $W=\left\{ \left( t,2t,3t \right)^{T}\ |\ t\in \mathbb{R} \right\}$ be a line in direction $\mathbf{w}_{1}=\left( 1,2,3 \right)^{T}\in \mathbb{R}^{3}$. 
> - Under dot product, orthogonal complement $W^{\perp}=\mathbf{w}_{1}^{\perp}$ is the plane passing through origin having normal vector $\mathbf{w}_{1}$
> - i.e. $\mathbf{z}=\left( x,y,z \right)^{T}\in W^{\perp}$ if and only if $\mathbf{z}\cdot\mathbf{w}_{1}=x+2y+3z=0$.
> - Thus, $W^{\perp}$ is characterized as solution space of homogeneous linear equation shown above. 
> 	- solve as you would for finding $A\mathbf{x}=\mathbf{0}$
> - General solution where $y,z$ are free variables: $$\mathbf{v}=\begin{pmatrix} -2y-3z\\y\\z \end{pmatrix}=y\begin{pmatrix} -2\\1\\0 \end{pmatrix}+z\begin{pmatrix} -3\\0\\1 \end{pmatrix}=y\mathbf{z}_{1}+z\mathbf{z}_{2}$$

> [!corollary] Propositions.
> *Proposition 1.* Suppose that $W \subset V$ is a finite-dimensional subspace of an inner product space. Then every vector $\mathbf{v}\in V$ can be uniquely decomposed into $\mathbf{v}=\mathbf{w}+\mathbf{z}$ where $\mathbf{w}\in W$ and $\mathbf{z}\in W^{\perp}$
>
> *Proposition 2.* If $W\subset V$ is a subspace with $\text{dim }W=n$ and $\text{dim }V=m$, then $\text{dim }W^{\perp}=m-n$.

> [!example]
> Decompose $\mathbf{v}=\left( 1,0,0 \right)^{T}\in \mathbb{R}^{3}$ into sum $\mathbf{v}=\mathbf{w}+\mathbf{z}$ of $\mathbf{w}$ lying on $W$ & $\mathbf{z}$ on orthogonal plane $W^{\perp}$.
> - we only need to compute either $\mathbf{v}$ or $\mathbf{w}$ since we can get the other by subtracting first from $\mathbf{v}$
> - where $\mathbf{w}_{1}=\left( 1,2,3 \right)^{T}$, we compute: $$\text{proj}_{\mathbf{w}_{1}}(\mathbf{v})=\frac{\left\langle \mathbf{v}, \mathbf{w}_{1} \right\rangle }{\lvert \mathbf{w}_{1} \rvert ^{2}}\cdot \mathbf{w}_{1}=\left( \frac{1}{14}, \frac{2}{14}, \frac{3}{14} \right)^{T}$$
> - then we obtain component in $W^{\perp}$: $$\mathbf{z}=\mathbf{v}-\mathbf{w}=\left( \frac{13}{14}, - \frac{2}{14}, -\frac{3}{14} \right)^{T}$$
> - this can also be obtained thru orthogonal projection onto $W^{\perp}$
> 	- must make sure basis is orthogonal first
>
>