#ch8 
- any given [[permutations of finite sets|permutation]] is even or odd:
	- *even* if it is a product of an even number of transpositions
	- *odd* if it is a product of an odd number of transpositions
- seems trivial, but important for several theorems 

> [!theorem]
> No matter how $\epsilon$ is written as a product of transpositions, the number of transpositions is even.

> [!proof]
> Let $t_{1}, t_{2},...,t_{m}$ be $m$ transpositions, and suppose that
> $$\epsilon=t_{1}t_{2}\cdots t_{m}$$ $\epsilon$ can be rewritten as a product of $m-2$ transpositions:
> Let $x$ be any numeral appearing in one of the transpositions $t_{1}, ...,t_{m}$. Let $t_{k}=(xa)$, and suppose $t_{k}$ is the last transposition in which $x$ appears: $$\epsilon=t_{1}t_{2}\cdots t_{k-1}\ t_{k}\ t_{k+1}\cdots t_{m}$$ ... where $t_{k}=(xa)$, and $x$ does not appear in $t_{k+1}\cdots t_{m}$.
> Now, $t_{k-1}$ is a transposition which is either equal to $(xa)$, or else one or both of its components are different from $x$ and $a$.
> **Case 1**: $t_{k-1}=(xa)$
> - $t_{k-1}=(xa)(xa)$ ... the identity permutation.
> **Case 2**: $t_{k-1}=(xb),\ b\neq x, a$
> - Then $t_{k-1}=t_{k}=(xb)(xa)$
> **Case 3**: $t_{k-1}=(ca),\ c\neq x, a$
> ##### ... finish proof later.

> [!theorem]
> If $\pi \in S_{n}$, then $\pi$ cannot be both an odd permutation and an even permutation

> [!proof]
> s.p $\pi$ is product of even number of transpositions & differently as product of an odd number. Contradiction: should be same for $\pi^{-1}$, but $\epsilon=\pi\circ\pi^{-1}$.

- the set of all even permutations in $S_{n}$ is a subgroup of $S_{n}$, the [[symmetric group]]. It's denoted $A_{n}$ and is called the **alternating group** on $\left\{ 1,2,...,n \right\}$
