
> [!definition]
> ### Disconnecting set of edges and edge-connectivity
> A **disconnecting set** (or edge cut) of a graph $G$ is a set $F\subseteq E(G)$ such that $G-F$ has more than one component.
> 
> A graph is $k$**-edge-connected** if every disconnecting set has size at least $k$. The edge-connectivity of $G$, denoted $\kappa'(G)$, is the minimum size of a disconnecting set (by convention $\kappa'(K_1)=0$).
> 
> Given disjoint, nonempty vertex sets $S,T\subseteq V(G)$ we write
> $$[S,T]=\{\,uv\in E(G): u\in S,\,v\in T\,\}$$
> for the set of edges with one endpoint in $S$ and one in $T$. For a proper nonempty subset $S\subset V(G)$ an **edge-cut** has the form $[S,V(G)\setminus S]$.

> [!theorem]
> ### Minimal disconnecting sets are cuts
> Every minimal disconnecting set is an edge-cut of the form $[S,V(G)\setminus S]$ for some nonempty proper $S\subset V(G)$.

> [!proof]
> Let $F$ be a minimal disconnecting set of $G$, so $G-F$ has at least two components and no proper subset of $F$ is disconnecting. Choose a component $C$ of $G-F$ and set $S=V(C)$. Any edge with exactly one endpoint in $S$ must belong to $F$, otherwise that edge would join $C$ to another component of $G-F$, contradicting that $C$ is a component of $G-F$. Thus $[S,V(G)\setminus S]\subseteq F$. But $[S,V(G)\setminus S]$ itself disconnects $G$, so by minimality of $F$ we must have $F=[S,V(G)\setminus S]$.

> [!theorem]
> ### Whitney inequality (vertex, edge, and degree connectivity)
> For every graph $G$,
> $$\kappa(G)\le \kappa'(G)\le \delta(G).$$
> That is, vertex-connectivity is at most edge-connectivity, which is at most the minimum degree.

> [!proof]
> (1) $\kappa'(G)\le \delta(G)$: let $v$ be a vertex of minimum degree $\delta(G)$. The set of edges incident with $v$ has size $\delta(G)$; removing them isolates $v$, so it is a disconnecting set. Hence $\kappa'(G)\le \delta(G)$.
> 
> (2) $\kappa(G)\le \kappa'(G)$: let $F$ be a minimum disconnecting set, so by the previous theorem there is a nonempty proper $S\subset V(G)$ with $F=[S,V(G)\setminus S]$. If every vertex of $S$ were adjacent to every vertex of $V(G)\setminus S$ then $|F|=|S|\cdot |V(G)\setminus S|\ge n-1\ge \kappa(G)$, so the inequality holds. Otherwise there exist $u\in S$ and $v\in V(G)\setminus S$ with $uv\notin E(G)$. Choose the endpoints of edges from $F$ other than those incident to $u$ or $v$ to form a vertex set separating $G$; one checks that the number of chosen vertices is at most $|F|$, yielding $\kappa(G)\le |F|=\kappa'(G)$. (A standard more explicit argument constructs a vertex separator from the endpoints of the cut, giving the same bound.)

> [!remark]
> Special cases and useful facts:
> - If $\kappa'(G)=1$ then $G$ contains a bridge (cut-edge).
> - For regular graphs it is often useful to combine $\kappa'(G)\le\delta(G)$ with other structural facts to bound $\kappa'(G)$.

> [!example]
> ### Example — strict inequalities
> 1. (Strict $\kappa(G)<\kappa'(G)$) Let $G$ be the graph formed by two triangles (copies of $C_3$) that share exactly one vertex. The shared vertex is a cut-vertex so $\kappa(G)=1$. However no single edge disconnects the graph (removing any single edge leaves each triangle connected through the shared vertex), so $\kappa'(G)\ge 2$. In fact $\kappa'(G)=2$ and $\delta(G)=2$, giving $1=\kappa(G)<\kappa'(G)=\delta(G)=2$.
> 
> 2. (Strict $\kappa'(G)<\delta(G)$) Take two disjoint copies of $K_4$ and join them by exactly two independent edges (i.e. pick two distinct vertices in each $K_4$ and add two disjoint edges between the copies). Every vertex inside a $K_4$ has degree at least $3$, so $\delta(G)\ge 3$, but removing the two bridging edges disconnects the graph, hence $\kappa'(G)\le 2$. Thus $\kappa'(G)<\delta(G)$ in this construction.

> [!example]
> ### Bridges and edge-connectivity
> If $G$ contains a bridge (an edge whose deletion increases the number of components), then that edge alone is a disconnecting set and $\kappa'(G)=1$. Conversely if $\kappa'(G)=1$ then $G$ has a bridge.

### Relations
- [[vertex & edge deletion]] — Deletion operations $G-e$ and $G-F$ are used in definitions and proofs.
- [[lemma - minimal disconnecting set is edge cut]] — (If present) alternative statement/proof of the minimal disconnecting-set lemma.
- [[theorem - Whitney inequality (4.1.7)]] — (If present) an expanded theorem file for the inequality $\kappa\le\kappa'\le\delta$.
- [[degree]] — The minimum degree $\delta(G)$ provides an upper bound for $\kappa'(G)$.
- [[cut-vertex, cut-edge]] — Bridges (cut-edges) relate directly to $\kappa'(G)=1$; cut-vertices relate to vertex connectivity $\kappa(G)$.
- [[MOC - Graph Theory]] — Map of concepts and where edge-connectivity fits in the course MOC.

