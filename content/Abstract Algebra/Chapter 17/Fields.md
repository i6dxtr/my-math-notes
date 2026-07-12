#ch17 

> [!definition]
> A **field** is a *nontrivial* [[operation commutativity|commutative]] (under multiplicaton) [[Rings|ring]] with [[unity]], in which every nonzero element has an inverse, i.e., a multiplicative [[inverse elements|inverse]].

> [!example]
> 1. $\mathbb{Z}$?
> 	1. $2\in \mathbb{Z}$ doesn't have multiplicative inverse
> 2. $\mathbb{Q}$?
> 	1. yup
> 3. $\mathbb{R}$
> 	1. yup

> [!theorem]
> Every field is an [[integral domain]].

> [!proof]
> 1. Suppose $A$ is a field.
> 2. WTS cancellation.
> 	1. Let $a,b,c\in A$
> 	2. Suppose $ab=ac$ *and* $a\ne 0$
> 	3. Then $a^{-1}$ exists since $A$ is a field
> 	4. So $a^{-1}ab=a^{-1}ac$
> 	5. So $1b=1c$
> 	6. So $b=c$.

### Zero Inverse

> [!remark]
> $0$ can't have an inverse:

> [!proof]
> Suppose it has inverse $x$. then $0x=1$. But $0=0$. So $1=0$. Then $\forall a\in A$, multiply by $a$: $1a=0n$ ... $a=0$. So $a=\left\{ 0 \right\}$ is trivial, contradiction.

### Operation Properties

> [!remark]
> If $A$ is a field (with $+$ and $\cdot$), then:
> 1. $( A,+ )$ is an [[abelian]] group
> 2. $( A^{*}, \cdot )$ is an abelian group where $A^{*}=A-\left\{ 0 \right\}$ AND...
> 3. $\cdot$ distributes over $+$
> 	1. assuming $A$ is a set with operations $+$ and $\cdot$, 1 and 3 give an alternative definition of field.

### Direct Products

> [!remark]
> The [[direct product]] of [[Fields|fields]] is *not* a field. Moreover, the direct product of [[integral domain|integral domains]] is *not* an integral domain.

## Chapter 20
- random fact

> [!theorem]
> Any [[subring]] with [[unity]] of a [[Fields|field]] is an [[integral domain]].

> [!remark]
> - What field?
> 	- It can be given by the [[field of fractions]] construction, generalizing the definition/construction of $\mathbb{Q}$ from $\mathbb{Z}$.
> 		- Think of $\mathbb{Z}$ as the prototypical integral domain
> - For example, we can define any $a\in \mathbb{Q}$ by an equivalence relation:
> 	- $a=\frac{q}{r}=\frac{q'}{r'}$
> 	- so $( a,b )\sim( a',b' )$ essentially means $ab'=ba'$
> 		- *i.e.* $\frac{a}{b}=\frac{a'}{b'}$, but written without fractions or division.
> 	- This is an equivalence relation.
> 	- Technically, it can be thought of as the equivalence class of $( 3,5 ): \frac{3}{5}=\left[ ( 3,5 ) \right]=\left\{ ( 3,5 ),( 6,10 ),( 9,15 ),( -3,-5 ),... \right\}$
> 	- This construction works with any integral domain
> 		- (observe that, in above, obviously $\mathbb{Z}$ is an integral domain)
> 		1. Define $\sim$ on the set of all pairs $( a,b )$ such that $a,b\in A$ and $b\ne0$
> 		2. By definition: $( a,b )\sim( a',b' )$ means $ab'=ba'$
> 		3. Define $\frac{a}{b}$ as the equivalence class of $( a,b )$
> 		4. Define $F=\left\{ \frac{a}{b}\ |\ a,b\in A \large\wedge b\ne0 \right\}$
> 		5. We show $F$ is a field:
> 			1. Define operations:
> 				1. $\frac{a}{b}+\frac{a'}{b'}=\frac{ab'+ba'}{bb'}$
> 				2. $\frac{a}{b}\cdot\frac{a'}{b'}=\frac{aa'}{bb'}$
> 				3. This is well defined only when $b,b'$ are not zero divisors,
> 			2. Fact: Rings are integral domains
> 			3. So $A$ is an integral domain. (assuming field axioms, not proven.)

link [[unity]] [[Rings]] [[operation commutativity]]