#ch20 

> [!definition]
> The **binomial expansion theorem** and formula is given by the following: $$ \small{( a+b )^{p}=\begin{pmatrix} p\\0 \end{pmatrix}a^{p}+\begin{pmatrix} p\\1 \end{pmatrix}a^{p-1}b+\begin{pmatrix} p\\2 \end{pmatrix}a^{p-2}b^{2}+\cdots+\begin{pmatrix} p\\p \end{pmatrix}b^{p}=\sum_{i=0}^{p}\begin{pmatrix} p\\i \end{pmatrix}a^{p-i}b^{i}}$$... which holds for any commutative [[ring]].

- When [[characteristic]] $\text{char}=p$, the inner terms (between the first and last) disappear, since they are multiples of $p$.
- ==Recall==: $$\begin{pmatrix} p\\i \end{pmatrix}=\frac{p!}{i!( p-i )!}=\frac{p( p-1 )( p-2 )\cdots( p-i+1 )( p-i )!}{i( i-1 )( i-2 )\cdots1( p-i )!}$$... if $p$ is prime, then $\begin{pmatrix} p\\i \end{pmatrix}$ is a multiple of $p$.

- ==Recall==: Any [[subring]] with [[unity]] of a [[Fields|field]] is an [[integral domain]].
- What field?
	- It can be given by the [[field of fractions]] construction, generalizing the definition/construction of $\mathbb{Q}$ from $\mathbb{Z}$.
		- Think of $\mathbb{Z}$ as the prototypical integral domain
- For example, we can define any $a\in \mathbb{Q}$ by an equivalence relation:
	- $a=\frac{q}{r}=\frac{q'}{r'}$
	- so $( a,b )\sim( a',b' )$ essentially means $ab'=ba'$
		- *i.e.* $\frac{a}{b}=\frac{a'}{b'}$, but written without fractions or division.
	- This is an equivalence relation.
	- Technically, it can be thought of as the equivalence class of $( 3,5 ): \frac{3}{5}=\left[ ( 3,5 ) \right]=\left\{ ( 3,5 ),( 6,10 ),( 9,15 ),( -3,-5 ),... \right\}$
	- This construction works with any integral domain
		- (observe that, in above, obviously $\mathbb{Z}$ is an integral domain)
		1. Define $\sim$ on the set of all pairs $( a,b )$ such that $a,b\in A$ and $b\ne0$
		2. By definition: $( a,b )\sim( a',b' )$ means $ab'=ba'$
		3. Define $\frac{a}{b}$ as the equivalence class of $( a,b )$
		4. Define $F=\left\{ \frac{a}{b}\ |\ a,b\in A \large\wedge b\ne0 \right\}$
		5. We show $F$ is a field:
			1. Define operations:
				1. $\frac{a}{b}+\frac{a'}{b'}=\frac{ab'+ba'}{bb'}$
				2. $\frac{a}{b}\cdot\frac{a'}{b'}=\frac{aa'}{bb'}$
				3. This is well defined only when $b,b'$ are not zero divisors,
			2. Fact: Rings are integral domains
			3. So $A$ is an integral domain. (assuming field axioms, not proven.)