> [!theorem]
> ### Theorem 4.1.7 *(Whitney 1952)*
> For every graph $G$,
> $$
> \kappa(G)\le \kappa'(G)\le \delta(G),
> $$
> where $\kappa(G)$ is the vertex-connectivity, $\kappa'(G)$ the edge-connectivity, and $\delta(G)$ the minimum degree.

> [!proof]
> We prove the two inequalities separately.
> 
> 1. $\kappa'(G)\le \delta(G)$.
> 
> Take a vertex $x$ with $d(x)=\delta(G)$. The set $F$ of all edges incident with $x$ has size $\delta(G)$. Removing $F$ disconnects $x$ from the rest of the graph (or isolates $x$), so $F$ is a disconnecting set and therefore $\kappa'(G)\le |F|=\delta(G)$.
> 
> 2. $\kappa(G)\le \kappa'(G)$.
> 
> Let $F$ be a minimum disconnecting set of edges, so $|F|=\kappa'(G)$. By the lemma that every minimal disconnecting set is an edge-cut, there exists a nonempty proper vertex subset $S$ with $F=[S,V(G)\setminus S]$. For each vertex in $S$ choose one endpoint in $S$ incident with an edge of $F$ and delete that vertex; doing this for every edge in $F$ we delete at most $|F|$ vertices and separate the graph. Hence there exists a separating set of size at most $|F|$, so $\kappa(G)\le |F|=\kappa'(G)$.
> 
> Combining the two inequalities yields $\kappa(G)\le \kappa'(G)\le \delta(G)$.
### Relations
- [[separating set, k-connectivity]] — Definition of $\kappa(G)$ and separating sets.
- [[disconnecting set, edge-connectivity]] — Definition of $\kappa'(G)$ and edge cuts.
- [[lemma - minimal disconnecting set is edge cut]] — Used to pass from a minimum edge cut to a vertex separating set in the second inequality.
- [[degree]] — Use of minimum degree $\delta(G)$ in the first inequality.

