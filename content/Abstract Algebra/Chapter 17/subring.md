#ch17 

> [!definition]
> $B$ is a **subring** of $A$ means:
> 1. $B$ is a subset of $A$
> 1. $B$ is a [[Subgroups|subgroup]] of $( A,+ )$
> 	1. $B$ is closed under $+$
> 	2. $0\in B$
> 	3. $B$ is closed under negatives
> 2. $B$ is closed under $\cdot$

> [!remark]
> Equivalently, $B$ is a subring of $A$ *if and only if* $B$ is closed with respect to subtraction and multiplication

- moreover, $B$ is a subset of $A$, being a ring under the same operations.
	- so we don't have to prove $B\subset A$

> [!example]
> ##### The set of dyadic rationals $D=\left\{ \frac{a}{2^{b}}\ |\ a,b\in \mathbb{Z} \right\}$ is a subring of $\mathbb{Q}$.
> 1. Let $\frac{a}{2^{b}},\frac{c}{2^{d}}\in D$ where $a,b,c,d\in \mathbb{Z}$.
> 2. $D$ is closed under $+$: $$\frac{a}{2^{b}}+\frac{c}{2^{d}}=\frac{a2^{d}+2^{b}c}{2^{b+d}}\in  D$$... since $a2^{d}+2^{b}c$ where $b+d\in \mathbb{Z}$
> 3. $D$ contains $0$: $$0=\frac{0}{2^{0}}\in D.$$
> 4. $D$ is closed under negatives: 
> 	1. Let $\frac{a}{2^{b}}\in D$. 
> 	2. Then $-\frac{a}{2^{b}}=\frac{-a}{2^{b}}\in D$.
> 5. $D$ is closed under $\cdot$
> 1. Let $\frac{a}{2^{b}}, \frac{c}{2^{d}}\in D$. Then: $$\frac{a}{2^{b}}\cdot\frac{c}{2^{d}}=\frac{ac}{2^{b+d}}\in  D$$... since $ac,b+d\in \mathbb{Z}$

### Subrings with unity

> [!remark]
> Every *subring with unity*, $B$, of an [[integral domain]], $A$, is an integral domain. In other words, if $A$ has no [[zero divisors]] then $B$ has no zero divisors.

> [!remark]
> It is *not* true that every subring with unity is a [[Fields|field]].

> [!example]
> - $\mathbb{Q}$ is a field
> 	- $D$ is a subring of $\mathbb{Q}$
> 	- $D$ is *not* a field (closure under inverses)
> 		- $\frac{3}{2}\in D$ but $\left(  \frac{3}{2}  \right)^{-1}=\frac{2}{3}\not\in D$

### Field of Fractions

> [!remark]
> Let $B$ be a commutative ring with [[unity]]. If $B$ is a [[subring]] of some [[field]], then $B$ *is an [[integral domain]]*. Alternatively, every field is an integral domain *and* every subring with unity of an integral domain is an integral domain.
>
> Conversely, if $B$ is an integral domain, *then* it is a subring of some field, called its **field of fractions**.
>
> This fact generalizes this prototypical example:

> [!corollary] Fact.
> $\mathbb{Z}$ is an integral domain, and $\mathbb{Z}$ is a subring of the field $\mathbb{Q}$.

