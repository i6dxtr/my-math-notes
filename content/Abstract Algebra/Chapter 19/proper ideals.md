#ch19 
- As we've seen, there are several types of [[ideal|ideals]]
- An ideal with several properties of these types can be defined as a proper ideal:

> [!definition]
> A **proper ideal** $I$ of a [[ring]] $A$ is... 
> 1. [[(semi)prime ideals|semiprime]],
> 	1. $\forall a\in A$ $\forall n\in \mathbb{Z}^{+}$, if $a^{n}\in I$ then $a\in A$;
> 2. [[(semi)prime ideals|prime]], 
> 	1. $a,b\in A$, if $ab\in I$ then $a\in A$ or $b\in I$;
> 3. [[maximal ideal|maximal]], 
> 	1. There is no ideal $J$ of $A$ such that $I\subseteq J\subseteq A$ then $J=I$ or $J=A$.

> [!example]
> ##### Given $A=\mathbb{Z}$: Is $\left\langle 6 \right\rangle$ semiprime?
> 1. $\left\langle 6 \right\rangle=\left\{ 6i\ |\ i\in \mathbb{Z} \right\}$, the set of all multiples of 6 (definition)
> 2. Let $a\in \mathbb{Z}$ and $n\in \mathbb{Z}^{+}$
> 3. Does it follow that $a\in \left\langle 6 \right\rangle$; i.e. is $6$ divisible by $a$?
> 	1. $6|a^{n}$, so $2|a^{n}$ and $3|a^{n}$
> 	2. so $3|a^{n}$
> 	3. ...

> [!remark]
> Alternatively,
> 1. If $m=p_{1}p_{2}\cdots p_{k}$ for *distinct* primes $p_{1}, p_{2}, \cdots, p_{k}$, then $\left\langle m \right\rangle$ is *semiprime*
> 2. Otherwise, if the prime factorization of $m$ is $p_{1}^{e_{1}}p_{2}^{e_{2}}\cdots p_{k}^{e_{k}}$

> [!example]
> $\left\langle 12 \right\rangle$ is not semiprime:
> 1. $12=2^{2}\cdot3$
> 2. $6^{2}=2^{2}3^{2}$ is in $\left\langle 12 \right\rangle$ since $36=12 \cdot 3$
> 	1. ... but $6=2\cdot3$ is not in $\left\langle 12 \right\rangle$

> [!corollary]
> An integer is called *square free* if it is not divisible by $n^{2}$ for any $n>1$.
> $\left\langle m \right\rangle$ is [[(semi)prime ideals|semiprime]] if and only if it is square free.

> [!theorem]
> Let $A$ be a (nontrivial) commutative ring with unity and let $I$ be a *proper ideal* of $A$.
> 1. $I$ is *semiprime* if and only if $A / I$ has no nonzero [[nilpotent]] elements
> 2. $I$ is *prime* if and only if $A / I$ is an [[integral domain]]
> 3. $I$ is *maximal* if and only if $A / I$ is a [[Fields|field]].

