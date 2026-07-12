#ch18 

> [!theorem]
> Let $A$ be a ring and $I$ be an [[ideal]] of $A$.
> $I$ is *prime* means $\forall x,y\in A$, if $xy\in I$ then $x\in I$ or $y\in I$.

> [!remark]
> - Let $n\ge 2\in \mathbb{Z}^{+}$ and $I=\left\langle n \right\rangle=\left\{ ...,-2n,-n,0,n,2n,... \right\}$. 
> - $I$ is prime *if and only if* $n$ is a prime number.
> - If $n$ is composite, then $I$ is not prime
> 	- $ab=n\in I$ but $a\notin I$ and $b\notin I$.
> - If $n$ is prime, WTS $I$ is prime
> 	- Let $x,y\in \mathbb{Z}$
> 	- Suppose $xy\in I$
> 		- So $n |xy$ i.e. $xy$ is a multiple of $n$
> 		- Since $n$ is prime, by Euclid's lemma, $n|x$ or $n|y$, so $x\in I$ or $y\in I$

> [!theorem]
> Let $A$ be a ring and $I$ an ideal of $A$. $I$ is *semiprime* if the following holds:  $$\forall a\in A, \forall n\in \mathbb{Z}^{+}: \  a^{n}\in I \longrightarrow a\in A.$$

---

> [!corollary] Euclid's Lemma
> If $p$ is prime and $p|ab$, then $p|a$ or $p|b$.

> [!remark]
> Let $A$ be a commutative ring with unity. The trivial ideal, $\left\{ 0 \right\}$, is prime *if and only if* $A$ is an [[integral domain]].

> [!proof]
> - $\left\{ 0 \right\}$ is prime means:
> 	- $\forall x,y\in A$, if $xy\in \left\{ 0 \right\}$ then $x\in \left\{ 0 \right\}$ or $y\in \left\{ 0 \right\}$
> 		- *i.e.* if $xy=0$ then $x=0$ or $y=0$
> 	- this is equivalent to stating $A$ has no zero divisors.

link [[ideal]]