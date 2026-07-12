 #ch2

> [!definition]
> A **vector space** is a set $V$ equipped with two operations:
> - *Addition*: adding any pair of vectors $\overline{v}, \overline{w}\in V$ produces another vector $\overline{v}+\overline{w}\in V$
> - *Scalar multiplication*: multiplying a vector $\overline{v}\in V$ by a scalar $c\in \mathbb{R}$ produces a vector $c\overline{v}\in V$

> [!corollary]
> The following axioms hold for all $\overline{v}\in V$:
> - Commutativity of Addition
> - Associativity of Addition
> - Additive Identity
> 	- There is a zero element $\overline{0}\in V$ satisfying $\overline{v}+\overline{0}=\overline{v}=0+\overline{v}$
> - Additive Inverse
> 	- $\forall \overline{v}\in V\ \exists-v\in V$ s.t.  $\overline{v}+(-\overline{v})=0=(-\overline{v})+\overline{v}$
> - Distributivity
> - Associativity of Scalar Multiplication
> - Unit for Scalar Multiplication
> 	- the scalar $1\in \mathbb{R}$ satisfies $1\overline{v}=\overline{v}$
>
> The following identities are elementary consequences of the vector space axioms:
> 1. $0\mathbf{v}=\mathbf{0}$
> 2. $(-1)\mathbf{v}=-\mathbf{v}$
> 3. $c\mathbf{0}=-\mathbf{0}$
> 4. If $c\mathbf{v}=\mathbf{0}$, then either $c=0$ or $\mathbf{v}=0$

- related to the [[kernel space]] of a [[Matrix|matrix]]
- a [[Subspaces|subspace]] of a vector space is a vector space wholly contained within another
- a [[basis]] can be found for a vector space (and subsequently, a [[Subspaces|subspace]]) if:
	- it spans
	- is [[linear independence|linearly independent]]

> [!example]
> - The Euclidian space $\mathbb{R}^{n}$
> 	- all $n-$tuple of reals ( $\mathbf{v}=(v_{1}, v_{2}, ..., v_{n})^{T}$ ) written as column vectors.
> 	- usual definition of $\mathbf{v}+ \mathbf{w}$ and $c\mathbf{v}$
> - $M_{m \times n}$, all real matrices w/ given size
> 	- vector space under matrix addition and scalar multiplication
> 	- zero element is the zero matrix
> - $\mathcal{P}^{(n)}=\left\{ p(x)=a_{n}x^{n}+a^{n-1}a^{n-1}+...+a_{1}x+a_{0} \right\}$
> 	- all real polynomials of degree $\leq n$.
> 	- addition of polynomials defined in usual manner
> 		- note, sum of polys deg. $\leq n$ holds true for the polys themselves too
> 	- scalar multiplication defined in usual manner
> 	- zero element $\in\mathcal{P}^{(n)}$

