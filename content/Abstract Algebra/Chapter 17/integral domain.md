#ch17 

> [!definition]
> An **integral domain** is a nontrivial [[operation commutativity|commutative]] [[Rings|ring]] with [[unity]] and the [[cancellation property]].
> Equivalently, we can say there are no [[zero divisors]]. 

> [!theorem]
> Every [[Fields|field]] is an integral domain.

> [!proof]
> 1. Suppose $A$ is a field.
> 2. WTS cancellation.
> 	1. Let $a,b,c\in A$
> 	2. Suppose $ab=ac$ *and* $a\ne 0$
> 	3. Then $a^{-1}$ exists since $A$ is a field
> 	4. So $a^{-1}ab=a^{-1}ac$
> 	5. So $1b=1c$
> 	6. So $b=c$.

- The converse is not true:

> [!remark]
> Not every integral domain is a field
> - *e.g.* $\mathbb{Z}$ is an integral domain, but not a field
> 	- let $a,b,c\in \mathbb{Z}$ with $a\neq 0$
> 		- so $ab=ac$
> 		- so $a^{-1}ab=a^{-1}ac$
> 		- so $1b=1c$
> 		- so $b=c$
> 	- Observe: $a^{-1}$ might not exist in $\mathbb{Z}$, ex. if $a=\mathbb{Z}$. But it does exist in $\mathbb{Q}$ such that we can still use it to cancel.'

> [!example]
> ##### Prove that $a,b\in A$ where $A$ is an integral domain & $a^{2}=b^{2}$, then $a=b$ or $a=-b$.
> 1. $a^{2}=b^{2}$
> 2. $a^{2}-b^{2}=0$
> 3. $( a+b )( a-b )=0$
> 4. Since $A$ has no zero divisors, $a+b=0$ or $a-b=0$
> 	1. so $a\ne 0\ \wedge b\ne0\longrightarrow ab\ne 0$ is equivalent to $ab=0\longrightarrow a=0\ \vee\  b=0$, aka no 0-divisors
> 5. Take $a+b=0$
> 	1. then $a=-b$
> 6. Take $a-b=0$
> 	1. then $a=b$

> [!remark]
> If $A$ is not an integral domain, this *can fail.*

> [!example]
> ##### In $\mathbb{Z}_{8}$
> 1. $1^{2}=1$
> 2. $2^{2}=4$
> 3. $3^{2}=1$
> 4. ...
> 5. So $1^{2}=3^{2}$
> 	1. but $1\ne \pm 3$
> 		1. $( -3=5\ne1 )$

> [!remark]
> If $A$ is an [[integral domain]], the only idempotent elements are $0$ and $1$.

> [!proof]
> Suppose $a^{2}=a$. So $a\cdot a=a\cdot1$. If $a$ is nonzero then, by cancellation, $a=1$.

### Chapter 20
#### Relation of [[characteristic]] to the integral domains

> [!theorem]
> Every finite [[integral domain]] is a [[Fields|field]].
> - *i.e. $\mathbb{Z}$ is an infinite integral domain that's not a field*.

> [!proof]
> 1. Let $A$ be a finite integral domain
> 2. Let $a\in A$ be nonzero
> 3. We'll show $a$ has an inverse...      ... *i.e. $\exists b\in A$ such that $ab=1$...         ... this also implies $ba=1$ by commutativity, so $b=a^{-1}$*.
> 	1. Let $A=\left\{ b_{1},b_{2},...,b_{n} \right\}$
> 	2. Observe: $ab_{1}, ab_{2},...,ab_{n}$
> 	3. We'll show one of these is equal to 1:
> 	4. These are different:
> 		1. If $ab_{i}=ab_{j}$, then since $a\ne 0$, $b_{i}=b_{j}$, by cancellation.
> 		2. So $i=j$
> 	5. Suppose a contradiction: there exists no $ab_{i}=1$.
> 		1. Then $ab_{1},ab_{2},...,ab_{n}$ are $n$ different elements of the $( n-1 )$-element set $A-\left\{ 1 \right\}$.
> 		2. *Contradiction:* the pigeonhole principal
> 			1. *i.e.* $f:A\rightarrow A-\left\{ 1 \right\}$ defined by $f( b )=ab$ is injective, a contradiction.

> [!remark]
> - What goes wrong when $A=\mathbb{Z}$ and $a\in \mathbb{Z}$?
> 	- $f:\mathbb{Z}\rightarrow\mathbb{Z-\left\{ 1 \right\}}$ given by $f( b )=2b$ is injective
> 	- Not a contradiction, since an *infinite* set can have an injection to a proper subset.

> [!theorem]
> Let $ab\in A$. If $A$ is an integral domain of [[characteristic]] $p$, then $( a+b )^{p}=a^{p}+b^{p}$
> - *Assumption: $p\ne 0$, therefore prime.*

> [!proof]
> 1. In any commutative ring:
> 	1. $( a+b )^{2}=a^{2}+2ab+b^{2}$
> 		1. $=a^{2}+b^{2}$ since $2ab=( 1+1 )ab=0ab=0$
> 		2. if $\text{char}=2$
> 	2. $( a+b )^{3}=a^{3}+3a^{2}b+3ab^{2}+b^{3}$
> 		1. $=a^{3}+b^{3}$ since $3a^{2}b$ and $3ab^{2}$ are $0$
> 		2. if $\text{char}=3$
> 	3. $( a+b )^{4}=a^{4}+4a^{3}+6a^{2}b^{2}+4ab^{3}+b^{4}$
> 		1. ...
> 	4. $( a+b )^{5}=a^{5}+5a^{4}b+10a^{3}b^{2}+10a^{2}b^{3}+5ab^{4}+b^{5}$
> 		1. $=a^{5}+b^{5}$ since $10a^{3}b^{2}=( 1+1+1+1+1 )2a^{2}b^{2}$
> 		2. if $\text{char}=5$

> [!remark]
> - Let $A$ be an integral domain of $\text{char}$ $p$ and $a\in A$.
> - Then $pa=a+a+\cdots+a\ ( p\text{-times} )=0$

> [!remark]
> Since $( ab )^{p}=a^{p}b^{p}$ is also true (by commutativity), then the function $f:A\rightarrow A$ where $f( x )=x^{p}$ is a homomorphism.

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

link [[characteristic]] [[zero divisors]] [[cancellation property]] [[Fields]] [[unity]] [[operation commutativity]]