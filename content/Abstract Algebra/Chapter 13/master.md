
> [!definition]
> Let $G$ be a group, and $H$ a subgroup of $G$. For any element $a\in G$, the symbol $$aH$$... denotes the set of all products $ah$, as $a$ remains fixed and $h$ ranges over $H$. $aH$ is called a **left coset** of $H$ in $G$.
> Similarly, $$Ha$$... denotes the set of all products $ha$, as $a$ remains fixed and $h$ ranges over $H$. $Ha$ is called a **right coset** of $H$ in $G$.

- when to use each doesn't matter as much as being consistent when using each
- every coset in group $G$ is a subset of $G$
- proving $Ha=Hb$ means proving they're equal sets ($\forall x\in Ha$ in $Hb$, likewise for converse)$$a\in  Hb\longrightarrow Ha=Hb$$

> [!theorem]
> The family of all the cosets $Ha$, as $a$ ranges over $G$, is a partition of $G$.

> [!proof]
> 1. Show $Ha, Hb$ are either disjoint or equal
> 	1. if disjoint -- end proof
> 	2. if not: let $x\in Ha\cap Hb$
> 		1. $x\in Ha$ so $x=h_{1}a$, $\exists h_{1}\in H$
> 		2. $x\in Hb$ so $x=h_{2}b$, $\exists h_{2} \in H$
> 		3. therefore $h_{1}a = h_{2} b$
> 		4. solving for $a$ gives $a=(h_{1}^{-1} h_{2} )b$
> 		5. thus, $a\in Hb$, so $Ha = Hb$.
> 2. Show $\forall c\in G$ in one of the cosets of $H$
> 	1. clearly $c=ec$ and $e\in H$
> 	2. therefore $c=ec\in Hc$
> 	3. thus, the family of all the cosets of $H$ is a partition of $G$. **Q.E.D.**

- any coset can be rewritten in another way
	- $a\in Hb\longrightarrow Hb=Ha$
- where $H\subset G$, all cosets of $H$ have the same number of elements
	- leads to theorem

> [!theorem]
> If $Ha$ is any coset of $H$, there is a one-to-one correspondence from $H\rightarrow Ha$

> [!proof]
> - we should find obvious $f:H\rightarrow Ha$ s.t. $\forall h\in H$ matches $h$ with $ha$
> 1. define $f:H\rightarrow Ha$ as $f(h)=ha$
> 	1. $a$ remains fixed, $h$ varies
> 	2. check $f$ bijectivity:
> 		1. *$f$ is injective:* $f(h_{1})=f(h_{2})\longrightarrow h_{1}a=h_{2}a$, therefore $h_{1}=h_{2}$
> 		2. *$f$ is surjective:* $\forall a \in Ha$, $a$ in the form $ha$ for some $h\in H$, $ha=f(h)$
> 2. thus, $f$ one-to-one from $H$ to $Ha$. **Q.E.D.**

- any coset $Ha$ has same # of elements as $H$
	- so all cosets have same # elements too ![[Pasted image 20241023225015.png]]

> [!theorem] Theorem: Lagrange's Theorem
> Let $G$ be a finite group, and let $H$ be any subgroup of $G$. The order of $G$ is a multiple of the order of $H$.

- order of any subgroup of a group $G$ is a divisor of the order of $G$.
	- *e.g.* $G$ w/ 15 elements.
		- proper subgroups $3-5$ elements
		- $G$ w/ 7 elements $\longrightarrow$ no proper subgroups
			- no factors not 1 or 7, aka prime

> [!theorem]
> If $G$ is a group with a prime number $p$ of elements, then $G$ is a cyclic group. Furthermore, any element $a\neq e$ in $G$ is a generator of $G$.

> [!proof]
>    Let $G$ be a group with a *prime* number $p$ of elements. 
> 1. If $a\in G$ where $a\neq e$, then $\text{ord}(a)=m\neq 1$. 
> 	1. ... but then $\left\langle a \right\rangle$ has $m$ elements
> 2. By Lagrange's, $m$ must be a factor of $p$.
> 	1. ... but $p$ is prime
> 3. ... therefore $m=p$
> 4. Thus, $\left\langle a \right\rangle$ has $p$ elements, thus is all of $G$.

- just a consequence of Lagrange's theorem
- its claim:
	- there is, up to isomorphism, only one group of any given prime order $p$
		- *e.g.* only group $\text{ord}=7$ is $\mathbb{Z}_{7}$, where $\text{ord}=11$ is $\mathbb{Z}_{11}$, etc.
- if $a$ any element of $G$, $\text{ord } a=\text{ord}\left( \left\langle a \right\rangle \right)$, a divisor of $\text{ord }G$
	- leads to theorem

> [!theorem]
> The order of any element of a finite group divides the order of the group.

- the *index* of $H$ in $G$ is the number of cosets of $H$ in $G$.
	- denoted $\left( G:H \right)$
	- can be expressed in terms of orders of $G, H$ $$\left( G:H \right)=\frac{\text{ord}(G)}{\text{ord(H)}}$$
	- 