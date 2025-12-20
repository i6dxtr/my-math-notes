#definition 
> [!definition]
> ### Definition — Hypergraph, $k$-uniform hypergraph
> A hypergraph is an ordered pair $H=(V,\mathcal{E})$ where $V$ is a finite vertex set and $\mathcal{E}\subseteq 2^V$ is a collection of subsets of $V$ called hyperedges.
> 
> A hypergraph is $k$-uniform if every hyperedge has size $k$, i.e. $\mathcal{E}\subseteq \binom{V}{k}$. In particular, a $2$-uniform hypergraph is the same thing as an (undirected) simple graph. ![[Pasted image 20250920190216.png]]

> [!remark]
> Hypergraphs generalize graphs by allowing edges that join more than two vertices. Many graph-theoretic definitions extend to hypergraphs but require care (e.g. paths and cycles have multiple non-equivalent generalizations). For combinatorial counting, refer to [[notation - combinatorics]].

### Relations
- Undirected graphs as $2$-uniform hypergraphs: [[graph]].
- Notation for $k$-subsets and power set: [[notation - combinatorics]].
