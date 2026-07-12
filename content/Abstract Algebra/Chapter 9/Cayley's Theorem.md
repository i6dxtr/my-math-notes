#ch9 

> [!theorem]
> Every group is [[Isomorphism|isomorphic]] to a group of [[permutations]] (*i.e.*, to a subgroup of $S_{a}$, the [[symmetric group]], for some $A$).

> [!proof] Proof: $G$ is isomorphic to a subgroup of $S_{G}$.
> - $\forall a\in G$, define $\Pi _{a}\in G$ by: $$\Pi _{a}(x)=ax$$... where $\Pi _{a}(x)$ is left-multiplication by $a$.
>
> ##### Proof: $\Pi _{a}$ is actually in $S_{G}$
> 1. $\Pi _{a}$ is a function from $G\rightarrow G$
> 2. Since $\forall x\in G$, $ax\in G$, $\Pi _{a}$ is a bijection, since has an inverse function $\Pi _{a^{-1}}$:
> 	$$
> 	\begin{align} \Pi _{a} (\Pi _{a^{-1}}(x))&=\Pi _{a}(a^{-1}x)=aa^{-1}x=x \\ \Pi _{a^{-1}}\left( \Pi _{a}(x) \right)&=\Pi _{a^{-1}}(ax)=a^{-1}ax=x \end{align}
> 	$$
> 	... recall how if there exists a two-sided inverse function on $f$, then $f$ must be both injective and surjective.
> 4. Thus $\Pi_a$ is a permutation of $G$.
>
> ##### Proof: $f$ is a homomorphism
> - Define $f:G\rightarrow S_{G}$ by $f(a)=\Pi _{a}$
> 1. Let $a,b\in G$. We show $f(ab)=f(a)\circ f(b)$ (meaning $\Pi _{ab}=\Pi_{a}\circ \Pi_{b}$)
> 2. $\forall x\in G$, $\Pi _{ab}(x)=abx$, so: $$\left( \Pi _{a}\circ \Pi _{b} \right)(x)=\Pi _{a}\left( \Pi _{b} (x)\right)=\Pi _{a} (bx)=abx.$$
>
> ##### Proof: $f$ is injective
> 1. Suppose $f(a)=f(b)$. 
> 2. We show $a=b$
> 	1. $\Pi _{a} = \Pi _{b}$
> 	2. So $\Pi _{a} (e)=\Pi _{b}(e)$
> 	3. Therefore $ae=be\longrightarrow a=b$
> 3. Define $H=\left\{ \Pi _{a}\ |\ a\in G \right\}=\text{range}(f)=\text{image}(f)$
> 4. Since $f$ is a homomorphsim, its range $H$ is a subgroup of $S_{G}$
> 5. Thus, $f$ is an injective and surjective homomorphsim onto $H$
> 	1. *i.e.* an isomorphism $G\rightarrow H$
> 	2. then $H$ is a group of permutations

> [!corollary] Lemma: Isomorphic properites of cyclic group $G$.
> ##### Proof: $\text{ord}(G)=n\longrightarrow G\cong \mathbb{Z}_{n}$
> 1. Let $a$ be a generator of $G$,
> 2. So $\text{ord}(a)=n$ and $G=\left\{ e,a,a^{2},..., a^{n-1} \right\}$
> 3. Define $f:\mathbb{Z}_{n}\rightarrow G$ by $f(k)=a^{k}$, a bijection.
> 4. We show $f$ is a homomorphism:
> 	1. $f(i+_{n} j)=a^{i+j\text{ mod }n}=a^{i+j}$
> 	2. Since $\text{ord}(a)=n=a^{i}a^{j}=f(i)f(j)$
> ##### Fact: $\text{ord}(G)=\infty\longrightarrow G\cong \mathbb{Z}$

link [[Isomorphism]] [[permutations]] [[Groups]] [[symmetric group]]