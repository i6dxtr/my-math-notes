#ch8 
- all [[permutations]] can be decomposed into simple parts called [[cycles]]
- for example, take $f$ below and observe how it moves the elements in its domain
$$
f=
\begin{pmatrix}
1&2&3&4&5&6&7&8&9\\ 3&1&6&9&8&2&4&5&7
\end{pmatrix}
$$
![[Pasted image 20241008121146.png]]

- observe the 3 separate subsets, which are the cycles
	- when the cycles share no common elements, they are [[disjoint cycles|disjoint]]
- all permutations are either [[even & odd permutations|even or odd]]

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