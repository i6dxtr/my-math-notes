#ch8
- a collection of [[Cycles|cycles]] are considered *disjoint* if they have no elements in common
	- e.g. $(132)$ and $(465)$
- disjoint cycles are [[operation commutativity|commutative]], meaning: $$(a_{1}\cdots a_{r})(b_{1}\cdots b_{s})=(b_{1}\cdots b_{s})(a_{1}\cdots a_{r})$$... note the composition operation is implied

> [!theorem]
> Every element in the [[symmetric group]] can be written as a product of some number of pair-wise disjoint cycles.

> [!remark]
>       Allow the trivial cases:
>
> 1. The product of $1$ cycle $(a_{1}a_{2}\cdots a_{k})$ is itself, $\left( a_{1} a_{2} \cdots a_{k} \right)$
> 2. The product of $0$ cycles (empty product) is $e$.

> [!example]
> Write $\begin{pmatrix} 1&2&3&4&5&6&7&8&9\\ 7&2&6&1&8&3&4&9&8\end{pmatrix}$ as a product of disjoint cycles.
> 1. $\rightarrow1\rightarrow7\rightarrow4\rightarrow:(1\ 7\ 4)$
> 2. $\rightarrow2\rightarrow:(2)$
> 3. $\rightarrow3 \rightarrow6 \rightarrow:(3\ 6)$
> 4. $\rightarrow5\rightarrow8\rightarrow9\rightarrow: (5\ 8\ 9)$
> 5. $=(1\ 7\ 4)(3\ 6)(5\ 8\ 9)$

- Consider any single-element cycle as being *fixed*, such that it is omitted in the product of disjoint cycles
	- makes then unique
- Conventionally, cycles written with the *smallest number first*.

> [!example]
> Write every element of $D_{4}$ as a product of some number of disjoint cycles
> where 1,2 on right side of square:
> - $0^{\circ}\text{ rot}$: $e$
> - $90^{\circ}\text{ rot}$: $(1\ 2\ 3\ 4)$
> - $180^{\circ}\text{ rot}$: $(1\ 3)(2\ 4)$
> - $270^{\circ}\text{ rot}$: $(1\ 4\ 3\ 2)$
> - reflection across $y$: $(1\ 4)(2\ 3)$
> - reflection across $x=y$: $(2\ 4)$
> - reflection across $x$: $(1\ 2)(3\ 4)$
> - reflection across $-x=y$: $(1\ 3)$

