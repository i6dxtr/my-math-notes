#ch15

> [!definition]
> If $H$ is a [[normal subgroup]] of $G$, we define an operation on $G / H$ by: $$( Ha )( Hb )=H( ab ).$$... which is a [[Groups|group]] under **coset multiplication**.

> [!proof] Proof of being well-defined
> Define $$G / H=\left\{  Ha\ |\ a\in  G \right\}$$... as the set of all right [[cosets]].
> 1. Suppose $Ha=Ha'$ and $Hb=Hb'$.
> 2. *By contradiction*:
> 3. *Claim.* $H( ab )=H( a'b' )$
> 	1. *Claim.* $H( ab )\subset H( a'b' )$
> 		1. Let $h_{1}ab\in Hab_{1}$, since $h_{1}a\in Ha=Ha'$
> 		2. So $h_{1}a=h_{2}a'$
> 		3. So $h_{1}ab=h_{2}a'=a'h_{3}b$ where $h_{3}\in H$
> 	2. Since $h_{3}b\in Hb=Hb'$, observe that $h_{3}b=h_{4}'$
> 	3. $h_{4}b'=b'h_{5}$ where $h_{4}, h_{5}\in H$
> 	4. Thus,
> 		1. $h_{1}ab$
> 		2. $=a'h_{3}b$
> 		3. $=a'h_{4}b'$
> 		4. $=h_{5}a'b'\in Ha'b'$
> 		5. ... where $h_{5}\in H$.

> [!corollary]
> If $H$ is normal, $h\in H$, and $c\in G$, then $hc=ch'$ for some $h'\in H$ (since $Hc=cH$)

> [!example]
> ##### Let $G=\left( \left\{ 1,3,7,9,11,13,17,19 \right\}, \cdot_{20} \right)$ and $H=\left\{ 1,9 \right\}$. Make a table for $G / H$.
> - $H1=\left\{ 1,9 \right\}$
> - $H3=\left\{ 3,7 \right\}$
> - $H11=\left\{ 11,19 \right\}$
> - $H13=\left\{ 13,17 \right\}$
> - Table: $$\left(\begin{array}{c|cccc} G / H&\underline{H1}&\underline{H3}&\underline{H11}&\underline{H13} \\ \underline{H1}&H1&H3&H11&H13 \\ \underline{H3}&H3&H1&H13&H11 \\ \underline{H11}&H11&H13&H1&H3 \\ \underline{H13} &H13&H11&H13&H1  \end{array}\right)$$

> [!example]
> ##### $*$ on $\mathbb{Q}$ by $\frac{a}{b}*\frac{c}{d}=\frac{a+c}{b+d}$
> 1. $\frac{1}{2}*\frac{1}{3}=\frac{1+1}{2+3}=\frac{2}{5}$
> 2. $\frac{2}{4}*\frac{3}{9}=\frac{2+3}{4+9}=\frac{5}{13}$

#### [[abelian|Abelian]]-ness

> [!corollary]
> $$G / H\text{ abelian}\Longleftrightarrow \forall a,b\in  G,\ aba^{-1}b^{-1}\in H$$
> - $axa^{-1}b^{-1}$ called a *commutation*
> 	- equals $e$ iff $ab=ba$

> [!proof]
>    Suppose $H$ contains all commutators $aba^{-1}b^{-1}$.
>    We show $G / H$ is abelian:
> 1. Let $Ha, Hb\in G / H$
> 	1. $HaHb=Hab$
> 	2. $HbHa=Hba$
> 2. We show 1 and 2 are equal
> 	1. recall $Hc=Hd \Longleftrightarrow c\in Hd$
> 	2. $ab = (aba^{-1}b^{-1})ba\in Hb$, assuming commutator in $H$
> 	3. Therefore $Hab=Hba$
> 	4. Therefore $HaHb=HbHa$
> 3. Thus, $G / H$ is abelian.

> [!theorem] Theorem: $G$ abelian $\longrightarrow$ $G / H$ abelian.
>    Let $Ha, Hb\in G / H$ where $a,b\in G$.
> - $HaHb=Hab=Hba=HbHa$

> [!remark] Remark: The converse may not be true.
>    *ex. Let $G=D_{4}$*
> 1. Let $H=\left\langle (1\ 2\ 3\ 4) \right\rangle=\left\{ \sigma\in D_{4}\ |\ \sigma \text{ is a rotation} \right\}$
> 2. So $He=\left\{ e,(1\ 2\ 3\ 4), \left( 1\ 3 \right)\left( 2\ 4 \right), \left( 1\ 4\ 3\ 2 \right) \right\}$
> 	1. $H(13)=\left\{ (1\ 3), (1\ 4)(2\ 3), (2\ 4) \right\}$
> 3. Now observe the table for $G / H$: $$\left(\begin{array}{c|cc} \underline{G / H}&\underline{He}&\underline{H(1\ 3)} \\ He&He&H(1\ 3) \\ H(1\ 3)&H(1\ 3)&He  \end{array}\right)$$... abelian

#### [[normal subgroup|Normality]]

> [!theorem]
> Let $H$ be a [[normal subgroup]] of $G$. If $Ha=Hc$ and $Hb=Hd$, then $H( ab )=H( cd )$.

> [!proof]
> 1. $Ha=Hc\longrightarrow a\in Hc$
> 	1. therefore $a=h_{1}c$ for some $h_{1}\in H$.
> 2. $Hb=Hd\longrightarrow b\in Hd$
> 	1. therefore $b=h_{2}d$ for some $h_{2}\in H$.
> 3. Therefore: $$ab=h_{1}ch_{2}d=h_{1}( ch_{2} )d$$
> 	1. But $ch_{2}\in cH=Hc$
> 	2. Thus, $ch_{2}=h_{3}c$ for some $h_{3}in H$
> 4. Observe $ab$:
> 	$$
> 	\begin{align}
> 	ab&=h_{1}( ch_{2} )d\\&=h_{1}( h_{3}c )d\\&=( h_{1}h_{3} )( cd )
> 	\end{align}
> 	$$
> 	... which is clearly in $H( cd )$.
> 5. Thus, $H( ab )=H( cd )$. **QED**

> [!corollary] Postulate: If $H$ is a subgroup of $G$ and $(G:H)=2$, then $H$ is normal.
> *e.g.* $G=D_{n}$, $H$ is equal to the rotations
>        $G=S_{n}$, $H=a_{n}$

> [!proof]
>    Recall that $H$ is normal if and only if $\forall a\in G,$  $Ha=aH$
> 1. **Case**: $a\in H$.
> 	1. Then $Ha=H=aH$
> 2. **Case**: $a\not\in H$.
> 	1. Then $Hb=G-H=bH$

#### [[Chapter 5/order|Order]]

> [!remark]
> In general, the [[order]] of $Ha$ in $G / H$ is the least $n\in \mathbb{Z}^{+}$ such that $a^{n}\in H$

> [!proof]
> $$
> \begin{align}
> (Ha)^{n}&=(HaHa\cdot Ha)\text{ $n$ times}\\ &=H((a\cdots a ),\text{ $n$ times})\\ &=Ha^{n}.
> \end{align}
> $$
> ###### In additive notation, 
> $$
> \begin{align}
> n(H+a)&=\left( H+a \right)+\left( H+a \right)+\cdots +\left( H+a \right) \\ &=H+\left( a+a+\cdots+a \right)\\ &=H+na.
> \end{align}
> $$

> [!remark]
> Some elements of $\mathbb{R} / \mathbb{Z}$ have infinite order. 
> Namely, $\mathbb{Z}+x$ where $x\in \mathbb{R}-\mathbb{Q}$ ($x$ is irrational).

> [!proof] Proof: by contraposition.
> If $\mathbb{Z}+x$ has finite order, then $x\in \mathbb{Q}$.
> 1. Suppose it has order $n$;
> 	1. Then $n(\mathbb{Z}+x)=\mathbb{Z}+0$
> 	2. so $\mathbb{Z}+nx=\mathbb{Z}+0$
> 	3. so $nx\in \mathbb{Z}$.
> 2. Let $a=nx\in \mathbb{Z}$
> 	1. thus $x=\frac{a}{n}\in \mathbb{Q}$
> 	**Q.E.D**

#### [[Homomorphism]]

> [!theorem]
> $G / H$ is a [[Homomorphism|homomorphic]] image of $G$.

> [!proof]
> 1. Take $f(x)=Hx$, carrying each element to its own coset
> 	1. Homomorphic: $f( xy )=Hxy=Hx\cdot Hy=f( x )f( y )$
> 	2. called the *natural homomorphism*

### Examples

> [!example]
>    *Let $G=\mathbb{Z}$ and $H=\left\langle 10 \right\rangle$. Find the order of $H+6$ in $G / H$*
> 1. $(H+6)+(H+6)=H+12\neq H+0$
> 	1. note $H+0$ is the identity
> 	2. since $12\notin H+0$
> 2. $(H+12)+(H+6)=H+18\neq H+0$
> 	1. since $18\notin H+0$
> 3. $(H+18)+\left( H+6 \right)=H+24\neq H+0$
> 	1. since $24\notin H+0$
> 4. $\left( H+24 \right)+\left( H+6 \right)=H+30=H+0$
> 	1. since $30\in H+0$

> [!example]
>    *Show that every element of $\mathbb{Q} / \mathbb{Z}$ has finite order*
> 1. Let $\mathbb{Z}+\frac{a}{b}\in \mathbb{Q}+\mathbb{Z}$.
> 2. Then $b\left( \mathbb{Z}+\frac{a}{b} \right)=\mathbb{Z}+b\frac{a}{b}=\mathbb{Z}+a=\mathbb{Z}=e$
> 3. So the order of $\mathbb{Z}+\frac{a}{b}\leq b$

link [[Cosets]] [[Groups]] [[normal subgroup]] [[abelian]]