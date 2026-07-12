#ch2

> [!definition]
> A group is a set $G$ with an [[Binary Operations|operation]] $*$ on $G$ such that:
> 1. $*$ is [[operation associativity|associative]]
> 2. there is an [[Identity Element|identity element]] $e\in G$ for $*$, and
> 3. Every element $x\in G$ has an [[inverse elements|inverse]] $x^{-1}\in G$.
> - these are called the *group axioms*
> - technically, a group is $(G, *)$, but we can call it $G$ when $*$ is clear from context

- there are several different types of [[Binary Operations|operations]] on groups
	- see example 2 below
- [[abelian|Abelian groups]], a special type of group, are uniquely *commutative*
- [[Cyclic Subgroup|Cyclic subgroups]] are [[subgroups]] containing only one element of its superset group
	- and such element is called a [[generators|generator]] of its subgroup

> [!example]
> **Is $(\mathbb{Z}, +)$ a group?**
> *Solution*: Yes,
> 1. $\forall x,y \in \mathbb{Z}, x+y\in \mathbb{Z}$ (so $+$ is an operation on $\mathbb{Z}$)
> 1. $+$ is associative: $(x+y)+z=x+(y+z)$
> 2. $0\in \mathbb{Z}$ is an identity element: $0+x=x$ and $x+0=x$
> 3. Every $x\in \mathbb{Z}$ has an inverse $-x\in \mathbb{Z}$: $(-x)+x=0$ and $x+(-x)=0$
>
> **Is $(\mathbb{R}, \cdot)$ a group?**
> *Solution*: No,
> - It has an identity element $1\in \mathbb{R}$
> - $0\in\mathbb{R}$ has no inverse in $\mathbb{R}$: $0\cdot x\neq 1$
> But, $\mathbb{R}^{*}$ *is* a group. (all nonzero real numbers)
>
> **Is $(\mathbb{Z}^{*})$ a group?**
> *Solution*: No, 
> - $Z\in\mathbb{Z}^{*}$, but its inverse would have to be $\frac{1}{2}\notin \mathbb{Z}^{*}$
> 	- More precisely, $Z\cdot x=1$ (w/ $1$ being identity) would imply $x=\frac{1}{2}\not\in \mathbb{Z}^{*}$

Note:
- $(\mathbb{Z}, +)$, $(\mathbb{Q}, +)$,  $(\mathbb{R}, +)$, $(\mathbb{R}^*, \cdot)$, $(\mathbb{R}^+, \cdot)$, $(\mathbb{Q}^{*}, \cdot)$, $(\mathbb{Q}^{+}, \cdot)$ are all groups

> [!example]
> The group of integers modulo $n$:
> - defined as $\mathbb{Z}_{n}=\{ 0,1,2,...,n-1 \}$, $+_{n}$ is addition $\text{mod }n$
> - eg. for $n=10$: 
> 	$4+_{10}9 =4+9\text{ mod }10$
> 	 $=13\text{ mod }10$
> 	 $=3$.
> 	- think of a clock
>
> Note: $\mathbb{Z}_{n}$ is an example of a *finite* group, so we can make an operation table
> - eg. for $n=5$
> $$
> \begin{array}{c|cccc}
> \underline{t_{5}}  &  \underline{0} & \underline{1} & \underline{2} & \underline{3} & \underline{4} \\
> 0  & 0 & 1 & 2 & 3 & 4  & \\
> 1 & 1 & 2 & 3 & 4  & \underline{0}  & \text{: since }1+4\text{ mod }5=0\\
> 2 & 2 & 3 & 4 & 0 & 1 &  \\
> 3 & 3 & 4 & 0 & 1 & 2 &  \\
> 4 & 4 & 0 & 1 & 2 & \underline{3} & \text{: since }4+4\text{ mod }5=3
> \end{array}
> $$

> [!example]
> $SL_{n}(\mathbb{R})$= the set of all $n \times n$ matrices whose determinant is $1$.
> Proof that this is a group under matrix multiplication:
> 1. Let $A,b\in SL_{n}(\mathbb{R})$. WTS $AB\in SL_{n}(\mathbb{R})$
> 	$\text{det}(AB)=\text{det}(A)\text{det}(B)=1\cdot1=1$
> 2. Matrix multiplication is associative in general
> 3. There is an identity element $I_{n}$
> 	$I_{n}\in SL_{n}(\mathbb{R})$ since $\text{det}(I_{n})=1$
> 4. Let $A\in SL_{n}(\mathbb{R})$. WTS $\underline{A}^{-1}\in SL_{n}(\mathbb{R})$ (ud: exists since $\text{det}(A)\neq0$)
> 	$\text{det}(A^{-1})=\frac{1}{\text{det}(A)}=\frac{1}{1}=1$

- there are 2 different [[linear groups]]: $SL_{n}(\mathbb{R})$ and $GL_{n}(\mathbb{R})$

link: [[Binary Operations]] [[inverse elements]] [[Identity Element]] [[operation associativity]]