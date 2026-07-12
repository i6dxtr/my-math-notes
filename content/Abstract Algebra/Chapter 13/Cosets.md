#ch13

> [!definition]
> Let $G$ be a [[group]], and $H$ a [[subgroup]] of $G$. For any element $a\in G$, the symbol $$aH$$... denotes the set of all products $ah$, as $a$ remains fixed and $h$ ranges over $H$. $aH$ is called a **left coset** of $H$ in $G$.
> Similarly, $$Ha$$... denotes the set of all products $ha$, as $a$ remains fixed and $h$ ranges over $H$. $Ha$ is called a **right coset** of $H$ in $G$.

> [!example]
> *e.g.* $G=S_{3}$, $H=\left\langle 1,2 \right\rangle=\left\{ e, (12) \right\}$, $a=(1\ 2\ 3)$, so $aH$ is a right coset and $Ha$ is a left coset.
>    $Ha=\left\{ e(1\ 2\ 3), (12)(123) \right\}=\left\{ (1\ 2\ 3), (2\ 3) \right\}$
>    $aH=\left\{ (1\ 2\ 3)e, (1\ 2\ 3)(1\ 2) \right\}=\left\{ (1\ 2\ 3),(1\ 3) \right\}$
> *e.g.* $G=\mathbb{Z}_{6}$, $H=\left\langle 3 \right\rangle=\left\{ 0, 3 \right\}$
>    $H+0=\left\{ 0+0, 3+0 \right\}=\left\{ 0, 3 \right\}$
>    $H+1=\left\{ 0+1, 3+1 \right\}=\left\{ 1, 4 \right\}$
>    $H+2=\left\{ \cdots \right\}=\left\{ 2,5 \right\}$
>    $H+3=\left\{ \cdots \right\}=\left\{ 3,0 \right\}=H+0$
>    $H+4=\left\{ \cdots \right\}=\left\{ 4,1 \right\}=H+1$
>    $H+5=\left\{ \cdots \right\}=\left\{ 5,2 \right\}=H+2$
> Note there are only 3 different cosets, and they form a partition of $G$.

- when to use each doesn't matter as much as being consistent when using each
- every coset in group $G$ is a subset of $G$
- proving $Ha=Hb$ means proving they're equal sets ($\forall x\in Ha$ in $Hb$, likewise for converse)$$a\in  Hb\longrightarrow Ha=Hb$$

> [!corollary] Lemma 1.
> The right cosets of $H$ form a [[partition]] of $G$ such that: 
> 1. They are pairwise disjoint: $$Ha\neq Hb\longrightarrow Ha\cap Hb=\emptyset$$
> 2. Their union is all of $G$: 
>          $\rightarrow$ Every element of $G$ is in some right coset $Ha$

> [!proof]
> ##### If $Ha\cap Hb\neq \emptyset$ then $Ha=Hb$.
> 1. Suppose $\exists c\in Ha\cap Hb$.
> 2. So $c=xa,\exists x\in H$ and $c=yb,\exists y\in H$.
> 3. So $xa=yb$ and $a=x^{-1}yb$.
> 1. *Claim.* $Ha=Hb$
> 	1. *Claim.* $Ha\subset Hb$
> 		1. Let $d\in Ha$
> 		2. so $d=za=zx^{-1}yb$
> 		3. therefore $zx^{-1}yb\in H$
> 	2. *Claim.* $Hb\subset Ha$
> 		1. Let $d\in Hb$
> 		2. so $d=zb=zy^{-1}xa\in Ha$ 
> 		3. therefore $zy^{-1}xa\in H$
> ##### The union of all right cosets is $G$.
> $$
> \begin{align}
> \cup_{a\in G}Ha=G \begin{cases} \subset\text{ since }Ha\text{ is a subset of }G \\ \subset : \text{Let }b\in  G.\\ \ \ \ \ \  \text{Then }b=eb\in  Hb\\ \ \ \ \ \ \  \text{so }b\in  LHS. \end{cases}
> \end{align}
> $$

> [!theorem]
> ##### All cosets have the same number of elements.
> 1. Let $a\in G$.
> 2. *Claim*. $\lvert H \rvert=\lvert Ha \rvert$.
> 	1. Consider $f:H\rightarrow Ha$ defined by $f(x)=x$.
> 	2. $f$ is surjective by definition of $Ha$.
> 	3. *Claim.* $f$ is injective:
> 		1. Suppose $f(x_{1})=f(x_{2})$
> 		2. Then $x_{1}a=x_{2}a$
> 		3. $\rightarrow x_{1}aa^{-1}=x_{2}aa^{-1}$ 
> 		4. so $x_{1}=x_{2}$ ... log cancellation
> 	4. So $f$ is bijective.
> 3. 
> Thus, $\lvert H \rvert=\lvert Ha \rvert$. **Q.E.D**

$$\int_{a}^{b}f(x)$$

link [[Groups]]