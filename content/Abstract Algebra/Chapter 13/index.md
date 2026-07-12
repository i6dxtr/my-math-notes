#ch13 

> [!definition]
> The **index** of $H$ in $G$ is $(G:H)$, which is equal to the number of right [[cosets]] of $H$ in $G$. Meaning,
> 1. $\lvert H \rvert\cdot(G:H)=\lvert G \rvert$
> 2. $(G:H)=\frac{\lvert G \rvert}{\lvert H \rvert}$, if $G,H$ are finite sets.
> *e.g.* The index of $\left\langle 3 \right\rangle\in \mathbb{Z}$
> 	$\left\langle 3 \right\rangle+0=\left\{ -3,0,3,6,... \right\}$
> 	$\left\langle 3 \right\rangle+1=\left\{ ...-2,1,4,7,... \right\}$
> 	$\left\langle 3 \right\rangle+2=\left\{ ...,-1,2,5,8,... \right\}$
> 	... forming a [[partitions|partition]] of $G$.

> [!example]
> ##### $G=\mathbb{Z}, H=\left\langle 3 \right\rangle$
> So $( \mathbb{Z}:\left\langle 3 \right\rangle )=3$, since it can be rewritten $\mathbb{Z}+0, \mathbb{Z}+1, \mathbb{Z}+2$
> ##### $G=\mathbb{Q}, H\in \mathbb{Z}$
> 1. $( \mathbb{Q}:\mathbb{Z} )\rightarrow \infty$
> 	1. $\mathbb{Z}+0=\left\{ ...,-2,-1,0,1,2,... \right\}$
> 	2. $\mathbb{Z}+\frac{1}{2}=\left\{ ..,-\frac{3}{2},-\frac{1}{2}, \frac{1}{2},\frac{3}{2},\frac{5}{2},... \right\}$
> 	3. $\mathbb{Z}+\frac{1}3{}=\left\{ ...,-\frac{5}{3},-\frac{2}{3},\frac{1}{3},\frac{4}{3},\frac{7}{3},... \right\}$\
> 	4. $\mathbb{Z}+\frac{1}{4}$, etc....
> 	5. $\mathbb{Z}+\frac{1}{n}$, $n\in \mathbb{Z}^{+}$ are all different cosets

> [!remark]
> $( G:H )=$ the number of distinct left cosets of $H$ in $G$
> ... b/c $f( Ha )=a^{-1}H$ is a well-defined bijection from $\left\{ Hx\ |\ x\in G \right\}$ to $\left\{ xH\ |\ x\in G \right\}$

link [[partitions]] [[Cosets]] 