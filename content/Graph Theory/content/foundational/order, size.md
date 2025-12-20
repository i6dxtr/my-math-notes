#definition 
> [!definition]
> ### Definition: Order, Size
> Let $G$ be a graph.
> - The **order** of $G$ is $\lvert V(G) \rvert$, the number of vertices of $G$.
> - The **size** of $G$ is $\lvert E(G) \rvert$, the number of edges of $G$.
- If $G$ has $n$ vertices, the maximum value of $\lvert E(G) \rvert$ is
$$
\binom{n}{2} = \frac{n(n-1)}{2}.
$$


- Notation: $n(G) := \lvert V(G) \rvert$ and $e(G) := \lvert E(G) \rvert$.

#### Relations
- The **order** and **size** of a graph quantify its basic structure and relate directly to vertex degrees — see [[degree]] and the [[handshake lemma]] which connects degrees to edge count.
- The maximum size $\binom{n}{2}$ is attained by the complete graph; see [[graph]] and [[clique]] for complete graphs and cliques.
- Order and size are used when discussing graph complements ([[graph complement]]), connectivity ([[connectedness]]), and extremal results (see [[theorem - dirac (hamiltonian)]]).
- See also [[neighbor, adjacent]] and [[(induced) subgraphs]] for local and subgraph perspectives.
- Order and size are important parameters in matching and covering results (e.g., bounds on matching size, Tutte's condition uses vertex counts in odd components — see [[odd components]] and [[Tutte's theorem]]). 
- They also appear in algorithmic complexity discussions for BFS/DFS and matching algorithms where $n$ and $m$ denote input sizes ([[algorithm - breadth-first search (BFS)]], [[algorithm - depth-first search (DFS)]], [[matching]]).
