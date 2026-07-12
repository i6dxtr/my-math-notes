#ch14 

> [!definition]
> Let $H$ be a [[Subgroups|subgroup]] of a group $G$. $H$ is called a **normal subgroup** of $G$ if it is closed with respect to [[conjugate|conjugates]], that is, if: $$\forall a\in  H\ \wedge \forall x\in  G\ \ xax^{-1}\in  H$$

> [!example] Examples of normal subgroups
> ##### $SL_{n}(\mathbb{R})$ is a normal subgroup of $GL_{n}(\mathbb{R})$ 
> 1. Its the kernel of the determinant homomorphism, which we can check directly:
> 	1. Let$A\in SL_{n}(\mathbb{R})$ and $x\in GL_{n}(\mathbb{R})$. 
> 	2. WTS $XAX^{-1}\in SL_{n}(\mathbb{R}):$
> 		1. $\text{det}(XAX^{-1})=\text{det}(X)\text{det}(A)\text{det}(X)^{-1}$
> 			1. $=\text{det}(X)\cdot1\cdot \text{det}(X)^{-1}$
> 			2. $=1.$
>
> ##### If $G$ is abelian, then every subgroup $H$ of $G$ is normal
> 1. Let $a\in H$ and $x\in G$. 
> 2. $xax^{-1}=xx^{-1}a=ea=a\in H$
>
> ##### $A_{n}=\left\{ \sigma\in S_{n}\ |\ \sigma\text{ is even} \right\}$ is a normal subgroup of $S_{n}$:
> 1. Let $a\in A_{n}$ and $x\in S_{n}$.
> 2. WTS $xax^{-1}\in A_{n}$
> 	1. $a=\tau_{1}\cdots\tau_{k}$ where $k$ is even
> 	2. $x=\tau_{1}'\cdots\tau_{n}'$ where $n\geq 0$
> 	3. $x^{-1}=\tau_{n}'\cdots\tau_{1}'^{-1}=\tau_{n}'\cdots\tau_{1}'$
> 	4. So $xax^{-1}=\tau_{1}'\cdots\tau_{n}'\tau_{1}\cdots\tau_{k}\tau_{n}'\cdots\tau_{1}'$
> 3. Thus, the product of $2n+k$ transpositions is also even (since $k$ is even)

> [!example] Examples of non-normal subgroups
> ##### $H=\left\langle (1,2) \right\rangle=\left\{ e,(1,2) \right\}$ is not a normal subgroup
> - $(1\ 2)\in H$
> 	- *but*, $(1\ 2\ 3)(1\ 2)(1\ 2\ 3)^{-1}$
> 	- $=(1\ 2\ 3)(1\ 2)(3\ 2\ 1)$
> 	- $=(2\ 3)\not\in H$.

> [!remark]
>  Another way to show $A_{n}$ is normal in $S_{n}$ is to show it is the [[kernel]] of $f: S_{n}\rightarrow\mathbb{Z}_{2}$ where $$f(\sigma)=\begin{cases} 0&&\text{if }\sigma\text{ is even} \\ 1&&\text{if }\sigma\text{ is odd}\end{cases}$$... and show $f$ is a homomorphism.

link [[kernel]] [[Subgroups]] [[conjugate]]