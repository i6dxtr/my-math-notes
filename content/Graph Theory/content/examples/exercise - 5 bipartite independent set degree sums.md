#example 
> [!example]
> ### Exercise 5 — Bipartite characterization, independent sets, and degree sums
> Let $G$ be a graph.
> 1. Prove that $G$ is bipartite if and only if every subgraph $H$ of $G$ has an independent set of order at least $|V(H)|/2$.
> 2. If $G$ is bipartite with bipartition $(A,B)$, prove that
> $$\sum_{v\in A} d(v) \;=\; \sum_{v\in B} d(v).$$> [!proof]
> (1) ($\Rightarrow$) If $G$ is bipartite then every subgraph $H$ is also bipartite. For any bipartition of $H$ one of the two parts has size at least $|V(H)|/2$, and each part is an independent set; hence $H$ contains an independent set of order at least $|V(H)|/2$.
> 
> ($\Leftarrow$) Contrapositive: suppose $G$ is not bipartite. Then $G$ contains an odd cycle $C$ of length $2k+1$. Any independent set in $C$ has size at most $k$, but $|V(C)|=2k+1$ so $k < (2k+1)/2$. Therefore the subgraph $H=C$ has no independent set of order $\ge |V(H)|/2$, contradicting the hypothesis. Thus $G$ must be bipartite.
> 
> (2) Let $G=(A\cup B, E)$ be bipartite with bipartition $(A,B)$. Each edge of $G$ has one endpoint in $A$ and one in $B$, so when summing degrees over $A$ we count each edge exactly once (from the $A$ side), and likewise summing over $B$ counts each edge exactly once. Therefore both sums equal the number of edges $e(G)$, giving
> $$\sum_{v\in A} d(v)=e(G)=\sum_{v\in B} d(v).$$
### Remarks
- Part (1) gives a useful extremal characterization of bipartiteness in terms of independent sets in all subgraphs.
- Part (2) is an immediate counting observation; it is often used when comparing partition sizes or edge distributions in bipartite graphs.

### Relations
- Bipartite characterization and odd-cycle obstruction: [[theorem - bipartite characterization]].
- Independent sets: [[independent set]].
- Degree and handshake counting: [[degree]], [[handshake lemma]].
