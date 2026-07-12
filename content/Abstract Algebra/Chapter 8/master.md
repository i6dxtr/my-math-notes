### Permutations of finite sets
- every permutation can be decomposed into simple parts called *cycles*
- for example, take $f$ below and observe how it moves the elements in its domain
$$
f=
\begin{pmatrix}
1&2&3&4&5&6&7&8&9\\ 3&1&6&9&8&2&4&5&7
\end{pmatrix}
$$
![[Pasted image 20241008121146.png]]

- 3 separate subsets
- these are the *cycles*
formal definition of cycle:

> [!definition]
> Let $a_{1}, a_{2},...,a_{s}$ be distinct elements of the set $\left\{ 1,2,...,n \right\}$. The **cycle** $(a_{1}a_{2}\cdots a_{s})$ is the permutation $a_{1}\rightarrow a_{2}\rightarrow a_{3}\rightarrow\cdots\rightarrow a_{s-1}\rightarrow a_s$ of $\left\{ 1,2,...,n \right\}$ with remaining elements of $\left\{ 1,2,...,n \right\}$ remaining fixed.

> [!example]
> In $S_{5}$, the cycle $(254)$ is the permutation $$\begin{pmatrix} 1&2&3&4&5 \\ 1&5&3&2&4 \end{pmatrix}$$

- notice how in the example above, $2$ maps to $5$, and $4$ maps to $2$, such that $\cdots \rightarrow 2\rightarrow 5\rightarrow 4\rightarrow2\rightarrow\cdots$

- A [[composition]] of 2 cycles can be formed as you'd expect
	- typically called the *product* of two cycles

> [!example]
> $$
> > \begin{align}
> (245)(124)&=
> \begin{pmatrix}
> 1&2&3&4&5 \\ 1&4&3&5&2
> \end{pmatrix}\circ
> \begin{pmatrix}
> 1&2&3&4&5 \\ 2&4&3&1&5
> \end{pmatrix}\\ &=
> \begin{pmatrix}
> 1&2&3&4&5 \\ 4&5&3&1&2
> \end{pmatrix}
> \end{align}
>
> $$
>
> Let $\alpha=(245)$ and $\beta=(124)$:
> - $\beta$ performs $1\rightarrow2$; $\alpha$ performs $2\rightarrow4$
> 	- $\alpha\beta$ performs $1\rightarrow4$
> - $\beta$ performs $2\rightarrow4$; $\alpha$ performs $4\rightarrow5$
> 	- $\alpha\beta$ performs $2\rightarrow5$
> - $\beta, \alpha$ leaves $3$ fixed; composite does the same
> 	- $\alpha\beta$ leaves $3$ static
> - $\beta$ leaves $5$ fixed; $\alpha$ performs $5\rightarrow2$
> 	- $\alpha\beta$ performs $5\rightarrow2$

- If $(a_{1}a_{2}\cdots a_{s})$ is a cycle, the integer $s$ is called its *length*
	- a cycle of length $=2$ is called a *transposition*
		- every cycle can be written as product of 1+ transposes
- If two cycles have no elements in common, they are considered [[disjoint cycles]]
- disjoint cycles are [[operation commutativity|commutative]], meaning: $$(a_{1}\cdots a_{r})(b_{1}\cdots b_{s})=(b_{1}\cdots b_{s})(a_{1}\cdots a_{r})$$
	- remember this is the operation of composition

> [!theorem]
> Every permutation is either the identity, a single cycle, or a product of disjoint cycles.

> [!example]
> Let $f=\begin{pmatrix} 1&2&3&4&5&6 \\ 3&4&5&2&1&6 \end{pmatrix}$. Writing $f$ as a product of disjoint cycles, we get: $$1\longrightarrow^{f}3\longrightarrow^{f}5\longrightarrow^{f}1$$ ... so the first cycle is $(135)$. Similarly, starting from $2$ we get $(24)$. Since only $6$ is left, we leave it fixed. Thus, $$f=(135)(24)$$

- the proof for *any* permutation follows the same pattern

> [!theorem] Formula for Products of Transpositions
> $$(a_{1}a_{2}\cdots a_{r})=(a_{r}a_{r-1})(a_{r}a_{r-2})\cdots(a_{r}a_{3})(a_{r}a_{2})(a_{r}a_{1})$$

> [!example] Expressing cycles as products of transpositions:
> $$
> > \begin{align}
> (12345)&=(54)(53)(52)(51) \\
> &=(15)(14)(13)(12) \\
> &=(54)(52)(51)(14)(32)(41)
> \end{align}
>
> $$

- expressions derived from this formula are *not* unique, nor are the number of transpositions involved.
- we define permutation even/odd-ness:
	- *even* if it is a product of an even number of transpositions
	- *odd* if it is a product of an odd number of transpositions
	- trivial, but important for several theorems

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

- the set of all even permutations in $S_{n}$ is a subgroup of $S_{n}$. It's denoted $A_{n}$ and is called the **alternating group** on $\left\{ 1,2,...,n \right\}$

