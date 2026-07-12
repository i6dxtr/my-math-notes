#ch5

> [!definition]
> A **subgroup** of $(G, *)$ is a subset $H$ of $G$ s.t. :
> - $\forall x,y \in H\ x*y\in H$ ($H$ is closed under the operation)
> 	- exact same criteria as normal group def.
> - $e$ is in $H$ ($H$ contains the identity element)
> - For every element $x$ of $H$, its inverse $x^{-1}\in H$ ($H$ is closed under inverses)
> - $*$ is associative (implied)

> [!theorem]
> If $(G,*)$ is a group and $H$ is a *finite* subset of $G$ such that:
> 1. $\forall x,y\in H,\ x*y\in H$
> 2. $e_{G}\in H$
> ... then $H$ is a subgroup of $(G, *)$

> [!proof]
> WTS $\forall x\in H,\ x^{-1}\in H$. 
> - Let $H=\left\{ a_{1},a_{2},...,a_{n} \right\}$. We show $a_{n}^{-1} \in H$ for each element $a_i \in H$. Note $a_{n}\cdot a_{1}, a_{n}\cdot a_{2}, ..., a_{n}\cdot a_{n}$ are all different (by cancellation) and all elements are in $H$ (by 1). So $H=\left\{ a_{n}a_1, a_na_2, ..., a_na_n \right\}$. By 2, $e_{g}=a_na_j$ for some $j$. So $a_{n}^{-1}=a_j \in H$. 

- we can define the *smallest* subgroup of, e.g. $G$, by taking some element $a\in G$ where $a$ is the only thing being operated on
	- we call this a [[Cyclic Subgroup]], which is [[generators|generated]] by $a$

> [!example]
> - $\left\{ e \right\}$ is a subgroup of $G$ (trivial subgroup). $G$ is a subgroup of $G$
>
> - $SL_{n}(\mathbb{R})$ is a subgroup of $GL_{n}(\mathbb{R})$ (matrices w/ $\text{det }1$)
> 	~~~ad-proof
> 	i. Let $A,B\in SL_{n}(\mathbb{R})$. Then $\text{det}(AB)=\text{det}(A)\text{det}(B)=1\cdot1=1$
> 	ii. $I\in SL_{n}(\mathbb{R})$ since $\text{det}(I)=1$
> 	iii. Let $A\in SL_{n}(\mathbb{R})$. Then $\text{det}(a^{-1})=\frac{1}{\text{det}(A)}=\frac{1}{1}=1$. So $A^{-1}\in SL_{n}(\mathbb{R})$
> 	~~~
> 	- $H=\left\{ xy, x, e, x^{-1}, y, ... \right\}$ where $H \subset G$
> 	~~~ad-remark
> 	These aren't subgroups:
> 	- $H=\left\{ x,y,... \right\},\ G=\left\{ H, xy, ... \right\}$
> 	- $H=\left\{ \emptyset \right\},\ G=\left\{H, xy, ... \right\}$
> 	- $H=\left\{ x, ... \right\},\ G=\left\{ H, x^{-1}, ... \right\}$

> [!example]
> $\mathbb{Z}$ and $\mathbb{Q}$ are subgroups of $(\mathbb{R}, +)$
> 1. $\forall x,y\in \mathbb{Z},\ x+y\in\mathbb{Z}$
> 2. $0\in\mathbb{Z}$
> 3. $\forall x\in \mathbb{Z},\ -x\in\mathbb{Z}$
> - $SL_{n}(\mathbb{R})$ is a subgroup of $GL_{n}(\mathbb{R})$
> - $\left\{ 0,3,6,9 \right\}$ is a subgroup of $(\mathbb{Z}_{12}, +_{12})$

> [!remark]
> $\mathbb{Z}_{n}$ is *not* a subgroup of $\mathbb{Z}$.

> [!example]
> Let $n\in \mathbb{Z}^+$ and $\overline{x}\in\mathbb{R}^{n}$ *($n-$dimensional vector)*. Let $G_{\overline{x}}=\left\{ A\in GL_{n}\mathbb{R} |A\overline{x}=\overline{x} \right\}$. Then $G_{\overline{x}}$ is a subgroup of $GL_{n}(\mathbb{R})$ *(stabilizer subgroup)*.
> 1. (closure) Let $A,B\in G_{\overline{x}}$. We show $AB\in G_{\overline{x}}$. $\rightarrow$ $(AB)\overline{x}=A(B\overline{x})=A\overline{x}=\overline{x}$. So $AB\in G_{\overline{x}}$
> 2. (identity) We show $I\in G_{\overline{x}}$. This is given by definition of identity matrix.
> 3. (inverses) Let $A\in G_{\overline{x}}$. We show $A^{-1}\in G_{\overline{x}}$.
> 	$$
> 	\begin{align}
> 	A\overline{x}=\overline{x}&\Longrightarrow A^{-1}A\overline{x}=A^{-1}x \\
> 	&\Longrightarrow\overline{x}=A^{-1}\overline{x} \\
> 	&\Longrightarrow A^{-1}\overline{x} \\
> 	&=x.
> 	\end{align}
>
> 	$$
> - So $A^{-1}\in G_{\overline{x}}$
