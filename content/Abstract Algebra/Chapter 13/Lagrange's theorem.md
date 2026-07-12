#ch13

> [!definition]
> If $G$ is a [[Groups|group]] and $H$ is a [[Subgroups|subgroup]] of $G$, then the [[order]] of $H$ is a multiple of the order of $G$

> [!example]
> *e.g.* $S_{4}$ has order $24$
>    $D_{4}$ has order $8$, a multiple of $24$
>    $A_{4}$ has order $12$, a multiple of $24$
> *e.g.* $\mathbb{Z}_{6}$ has order $6$
>    $\left\{ 0,2,4 \right\}=\left\langle 2 \right\rangle$
>    $\left\{ 0,3 \right\}=\left\langle 3 \right\rangle$

> [!corollary] Corollaries of Lagrange's Theorem
> ##### 1. If $G$ is a group and $a\in G$, then the order of $a$ divides the order of $G$. ($\text{ord}(a)=\text{ord}(\left\langle a \right\rangle)$)
> ##### 2. Every group of prime order is cyclic
> 1. Suppose the order of $G$ is a prime $p$. $\exists a\in G, a\neq e$ s.t.
> 	1. $\left\langle a \right\rangle$ is a subgroup of $G$ 
> 	2. $\lvert \left\langle a \right\rangle \rvert>1$ and order dividing $p$
> 	3. so $\lvert \left\langle a \right\rangle \rvert=p$
> 	4. so $\left\langle a \right\rangle=G$
> ##### 3. Every group of prime order is abelian.
> ##### 4. Fermat's Little Theorem:
> $\Longrightarrow$ Let $p$ be prime and $0<a<p$
> $\Longrightarrow$ Then $a^{p-1}\text{ mod }p=1$.
> 1. Let $a\in\mathbb{Z}_{p}^{*}$, the group of nonzero elements of $\mathbb{Z}_{p}$ under multiplication $\text{mod }p$.
> 2. Let $k=\text{ord}(a)$. 
> 3. 2. By Lagrange's theorem, $k$ divides $p-1$, so let $p-1=nk$.
> 3. So $a^{p-1}=(a^{k})^{n}=e^{n}=e=1$ in $\mathbb{Z}_{p}^{*}$
> 4. So $a^{p-1}\text{ mod }p=1$.

link [[Subgroups]] [[Chapter 5/order|order]] [[Groups]]