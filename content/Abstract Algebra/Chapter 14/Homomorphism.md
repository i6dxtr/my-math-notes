#ch14

> [!definition]
> If $G$ and $H$ are groups, a **homomorpism** from $G$ to $H$ is a [[Functions|function]] $f:G\rightarrow H$ such that for any two elements $a,b\in G$, $$f(ab)=f(a)f(b)$$... which is equivalent to the form $f(a)=a'\wedge f(b)=b'\longrightarrow f(ab)=a'b'$.

- when such an $f$ exists, $H$ called the *homomorphic image* of $G$
- a homomorphism crucially preserves *at least one* structural property of the set being transformed to its image
- observe $f\left( ab \right)=f\left( a \right)f\left( b \right)$
	- the product $ab$ has a mapping with $f$ to some element in the image
	- such element is also equivalent to the product to the individual elements in the homomorphic image
- a homomorphic function is [[Isomorphism|isomorphic]] when it is bijective

> [!theorem]
> Let $f:G\rightarrow H$ be a homomorphism.
> 1. The [[kernel]] of $f$ is a [[normal subgroup]] of $G$, and
> 2. The *range* of $f$ is a subgroup of $H$.

> [!proof]
> ##### $\text{ker}\left( f \right)$ is a normal subgroup of $G$
> 1. Let $K$ denote the kernel of $f$. 
> 2. If $a,b\in K$, then $f(a)=e$ and $f(b)=e$. 
> 3. Therefore $f(ab)=f(a)f(b)=ee=e$
> 4. hence $ab\in K$
> 5. If $a\in K$ and $x\in G$ then $f(axa^{-1})=f(x)f(a)f(x^{-1})=f(x)f(a)\left[ f(x) \right]^{-1}=e$
> 6. Ss $xax^{-1}\in K$
> 7. Thus, $K$ is a normal subgroup of $G$.
> ###### $\text{range}\left( f \right)$ is a subgroup of $H$
> 1. If $f(a), f(b)\in \text{range}\left( f \right)$, then $f(a)f(b)\in \text{range}\left( f \right)$
> 2. If $f(a)\in \text{range}\left( f \right)$ then $\left[ f(a) \right]^{-1}=f(a^{-1})\in \text{range}\left( f \right)$
> 3. Thus $\text{range}\left( f \right)$ is a subgroup of $H$.

> [!remark]
> This fails if $f$ is *not* a multiple of $m$
> - e.g. $n=5, m=2$ since $\left(\begin{array}{c|ccccc} &0&1&2&3&4\\0&0&1&2&3&4\\1&1&2&3&4&0\\3&3&4&0&1&2\\ 4&4&0&1&2&3\end{array}\right)\longrightarrow ^{\text{replace } a \text{ with }f(a) }\left(\begin{array}{c|ccccc} &0&1&0&1&0\\ 0&0&1&0&1&0\\ 1&1&0&1&0&0\\ 0&1&0&0&1&0 \\ 1&0&0&1&0&1  \end{array}\right)$

> [!theorem]
> Let $G$ and $H$ be groups, and $f:G\rightarrow H$ a homomorphism. Then the following hold: 
> 1. $f\left( e \right)=e$
> 2. $f\left( a^{-1} \right)=\left[ f\left( a \right) \right]^{-1}$ for all $a\in G$
> 3. $f\left( a^{n} \right)=f\left( a \right)^{n}$
> 4. $\text{ord}\left( f\left( a \right) \right)=\text{ord}\left( a \right)$

> [!corollary] Corollaries of homomorphisms.
> ##### If $n$ is a multiple of $m$, then $f:\mathbb{Z}_{n}\rightarrow\mathbb{Z}_{m}$ where $f(a)=a\text{ mod }m$ is a homomorphsim.
> 1. Suppose $n$ is a multiple of $m$.
> 2. Let $a,b\in \mathbb{Z}_{n}$.
> 3. We show $f(a+b\text{ mod }n)=f(a)+f( b )\text{ mod }m$
> 	1. $LHS=( a+b\text{ mod }n )\text{ mod m}=a+b\text{ mod }m$
> 		1. since $n$ is a multiple of $m$.
> 	2. $RHS = ( a\text{ mod }m )+( b\text{ mod }m )\text{ mod }m=a+m$
>
> ##### $f:\mathbb{Z}\rightarrow\mathbb{Z}_{m}$ *where* $f(a)=a\text{ mod }m$.
> 1. $\text{ker}( f )=\left\{ a\in \mathbb{Z}\ |\ f( a )=0 \right\}$
> 	1. $=\left\{ a\in \mathbb{Z}\ |\ a\text{ mod }m=0 \right\}$
> 	2. $=\left\{ a\in \mathbb{Z}\ |\ a\text{ is a multiple of }m \right\}$
> 	3. $=\left\langle m \right\rangle$
> 2. $\text{ran}( f )=\mathbb{Z}_{m}$

> [!example]
> $\text{det}:GL_{n}(\mathbb{R})\rightarrow\mathbb{R}^{*}$ is a homomorphism:
> 1. $\text{det}(AB)=\text{det}(A)\text{det}(B)$
> 2. $\text{ker}(\text{det})=\left\{ A\in GL_{n}(\mathbb{R})\ |\ \text{det}(A)=1 \right\}=SL_{n}(\mathbb{R})$

> [!example]
> *Let $G, H$ be groups such that $f:G \times H\rightarrow G$ and $f(a,b)=a$. Prove that $f$ is a homomorphism*.
> 1. $\forall(a,b), (a', b')\in G \times H$:
> 	1. $f\left( (a,b)(a', b') \right)=f((aa', bb'))=aa'$
> 	2. $f((a,b))f((a',b'))=aa'$ also works
> 	3. $\text{ker}(f)=\left\{ (a,b)\in G \times H\ |\ f((a,b))=e \right\}=\left\{ (e,b)\ |\ \left\{ e \right\} \times H \right\}$

link [[conjugate|conjugacy]] [[normal subgroup|normal subgroups]] [[kernel]] [[Functions]]