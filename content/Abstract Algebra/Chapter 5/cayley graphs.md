#ch5 
- remember how [[groups]] can be defined by their *relations*:
	*e.g.* $G=\left\{ e,a,a^{2}, b, ab, a^{2}b \right\}$ where $a^{3}=e b^{2}=e, ba=a^{2}b$
- any finite group can be represented by the relations visually with arrows

> [!definition]
> A **Cayley graph**, or Cayley diagram, is a visual representation of the relations in a group $G$:
> 1. There is one point for every element in the group called the vertices, or points, of $G$
> 2. Arrows from elements represent the result of multiplying by a generator
> 3. Edges describe what happens when multiplying by several generators 
> 	1. *e.g.* $(a,b)$ is an edge with 2 arrows

> [!remark]
> ![[Pasted image 20241026221403.png]]
> - multiplying by $b$: $x\rightarrow xb$
> - multiplying by $b^{-1}$: $b\longleftarrow xb^{-1}$

- if 2 different paths (starting at $x$) lead to the same destination, then corresponding path (starting at $y$) lead to the *same destination as each other*
- any path leading to itself can be represented simply as the product of the elements along the path to itself
	- $a\rightarrow a^{2} \rightarrow \cdots \rightarrow a^{n}\rightarrow a$, so $a^{2}\cdots a^{n}=a$ 
	- the product of arrows that lead an element to the identity is it's inverse
#### building process
1. Build [[group table]]
2. Pick vertex $e$
3. Pick points with names of other elements in terms of which element generates it

