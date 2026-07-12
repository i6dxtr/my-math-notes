#ch9

> [!definition]
> Let $G_{1}$ and $G_{2}$ be groups. A [[bijective]] function $f:G_{1}\rightarrow G_{2}$ with the property that for any two elements $a,b\in G_{1}$: $$f(ab)=f(a)f(b)$$ ... is called an **isomorphism** from $G_{1}$ to $G_{2}$. If there exists an isomorphism from $G_{1}$ to $G_{2}$, we say that $G_{1}$ is **isomorphic** to $G_{2}$, or: $$G_{1}\cong G_{2}$$

- meaning, "same structure" in an abstract sense, e.g. palindromes
- there is a sequential process of [[determining isomorphism]] between two groups

> [!example] Example: Flow Networks
> - set of points w/ arrows joining them together
> - represents channels of communication, electric circuits, etc. ![[Pasted image 20241014134439.png]]
> - creating a superposition of the points in $(A)$ to points in $(B)$ shows the two are *isomorphic*:
> 	$$
> 	\begin{pmatrix}
> 	1&2&3&4 \\ 6&5&8&7
> 	\end{pmatrix}
> 	$$
> 	... which retains the direction of flow between points.
> - we call this an **isomorphism** from network $(A)$ to $(B)$
> Consider the following groups:
> ![[Pasted image 20241014135012.png]]
> - $G_{1}, G_{2}$ clearly different, but they are still isomorphic, since replacing elements in $G_{1}$ with those in $G_{2}$, we can see that $G_{1}$ *coincides* with $G_{2}$ forming a one-to-one correspondence in the following fashion:
> 	$$
> 	\begin{pmatrix}
> 	0&1&2 \\ e&a&b
> 	\end{pmatrix}
> 	$$
> 	... essentially transforming $G_{1}$ to $G_{2}$
> Generally speaking, if there exists an isomorphism between two [[Groups|groups]], there is a one-to-one correspondence between them. Formally: $$f(a)=a'\wedge f(b)=b' \longrightarrow f(ab)=a'b'$$![[Pasted image 20241014140110.png]]... from which we derive the definition, in more concise terms:

> [!theorem]
> Every group of [[order]] 4 is *isomorphic* to either $\mathbb{Z}_{4}$ or $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$. In the latter case, the group is called a *Klein* group.

> [!proof]
>    Let $G=\left\{ e,a,b,c \right\}$.
> 1. **Case**: $G$ is cyclic.
> 	1. Then $G\cong \mathbb{Z}_{4}$
> 2. **Case**: $G$ is not cyclic. We show $G\cong \mathbb{Z}_{2} \times \mathbb{Z}_{2}$
> 	1. ==Theorem.== If $G$ is a group and $a\in G$, then $\text{ord}(G)=k\cdot \text{ord}(a)\ \ \exists k\in \mathbb{Z}$.
> 	2. Observe: $\text{ord}(G)$ is divisible by $\text{ord}(a)$
> 	3. Thus, it is necessary that $1\in G$ or $2\in G$.
> 		1. Not $4$, since $G$ is *not* cyclic.
> 	4. So $a^{2}=e, b^{2}=e$, and $c^{2}=e$
> 		1. Construct table and observe $ab=c$

> [!corollary]
> If $G_{1}\cong G_{2}$ and there exists an $a\in G_{1}$ such that the order of $a$ is equal to $n$, then there exists a $b\in G_{2}$ such that the order of $b$ is also equal to $n$. $$\left( G_{1}\cong G_{2}  \right)\wedge \left( \exists a\in  G_{1} \text{ s.t. }\text{ord}(a)=n \right)\longrightarrow\left( \exists b\in G_{2}\text{ s.t. ord}(b)=n \right)$$

> [!example] Example: Proving $\mathbb{R}^{*}\not\cong \mathbb{R}$.
> 1. Assume $\mathbb{R}^{*}$ is closed under multiplication and $\mathbb{R}$ is closed under addition.
> 2. $\mathbb{R}^{*}$ has element $-1$ where $\text{ord}(-1)=2$
> 3. ==But==, $\mathbb{R}$ does *not*:
> 	1. Every non-identity element of $\mathbb{R}$ has $\text{ord}=\infty$ $$\left\langle a \right\rangle=\left\{ ...,2a,-a,0,a,2a,... \right\}$$

> [!example] Example: Proving $A_{4}\not\cong D_{6}$
> - Observe: $A_{4}, D_{6}$ neither abelian nor cyclic
> - Recall: $A_{4}=\left\{ \sigma\ |\ \sigma\text{ is even} \right\}$ is the group of [[symmetric group|rotational symmetries]] of a regular tetrahedron: $$A_{4}=\left\{ e,(1\ 2\ 3), (1\ 3\ 2), ..., (1\ 2)(3\ 4),... \right\}$$
> - Every element in $A_{4}$ has order $1,2,3$.
> - ==But==, $D_{6}$ has an element of order $6$
> 	- *e.g.* $(1\ 2\ 3\ 4\ 5\ 6)$

link: [[Groups]] [[bijective]] [[Functions]]