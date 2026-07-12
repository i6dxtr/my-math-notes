
> [!definition]
> If $G$ and $H$ are groups, a **homomorphism** from $G$ to $H$ is a function $f:G\rightarrow H$ such that for any two elements $a$ and $b$ in $G$, $$f(ab)=f(a)f(b)$$

- $H$ homomorphic image of $G$ $\rightarrow$ $f$  transforms $G$ into $H$
	- def $f:G\rightarrow H$
	- $f$ transform table $G$ to table $H$; therefore must have following property: $$f(a)=a'\ \wedge\ f(b)=b' \longrightarrow f(ab)=a'b'$$
	- If there exists a homomorphism from $G$ onto $H$, we say that $H$ is a **homomorphic image** of $G$

> [!theorem]
> Let $G$ and $H$ be groups, and $f:G\rightarrow H$ a homomorphism. Then:
> 1. $f(e)=e$
> 2. $f(a^{-1})=[ f(a)]^{-1}$ for every element $a\in G$.
> 3. $f(a^{n})=f(a)^{n}$
> 4. $\text{ord}(f(a))=\text{ord}(a)$

> [!definition]
> Let $H$ be a subgroup of a group $G$. $H$ is called a **normal subgroup** of $G$ if it is closed with respect to conjugates, that is, if: $$\forall a\in H\ \wedge\ \forall x\in G\ xax^{-1}\in H$$

> [!corollary]
> If $G_{1}\cong G_{2}$ and $\exists a\in G_{1}$ such that $\text{ord}(a)=n$, then $\exists b\in G_{2}$ such that $\text{ord}(b)=n$

> [!proof] Proof: $\mathbb{R}^{*}\not\cong \mathbb{R}$.
> - Assume $\mathbb{R}^{*}$ is closed under multiplication and $\mathbb{R}$ is closed under addition.
> 1. $\mathbb{R}^{*}$ has element $-1$ where $\text{ord}(-1)=2$
> 2. ... but $\mathbb{R}$ doesn't
> 	1. Every non-identity $a\in \mathbb{R}$ has $\text{ord}(a)=\infty$:
> 	2. $\left\langle a \right\rangle=\left\{ ...,2a, -a, 0, a, 2a, ... \right\}$

> [!proof] Proof: $A_{4}\not\cong D_{6}$
> - Observe how neither $A_{4}$ nor $D_{6}$ are abelian or cyclic.
> - Recall: $A_{4}=\left\{ \sigma\in S_{4}\ |\ \sigma\text{ is even} \right\}$ is the group of rotational symmetries of a regular tetrahedron: $\left\{ e, (1\ 2\ 3), (1\ 3\ 2), ..., (1\ 2)(3\ 4), ... \right\}$
> - Every element of $A_{4}$ has order $1,2,3$.
> - But $D_{6}$ has an element of order $6$
> 	- *e.g.* $(1\ 2\ 3\ 4\ 5\ 6)$

