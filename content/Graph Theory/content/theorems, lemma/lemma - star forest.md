
> [!theorem]
> ### Lemma — Star forest (minimum edge cover)
> Let $G$ be a graph with no isolated vertices. If $L$ is a minimum edge cover of $G$, then every component of the graph $H=(V(G),L)$ is a non-trivial star.
> 
> ![[Pasted image 20251015140040.png|400]]
> [!proof]
> Since $G$ has no isolated vertices, neither does $H$. Let $uv\in L$. Suppose for contradiction that in $H$ both $u$ and $v$ have degree at least $2$. Then there are edges $ux,vy\in L$ with $x\neq v$ and $y\neq u$, so removing $uv$ from $L$ leaves every vertex still incident with an edge from $L-uv$, contradicting minimality of $L$. Hence for every edge of $L$ at least one endpoint has degree $1$ in $H$, and each component of $H$ is therefore a star with at least one edge.
Relations
- [[content/foundational/edge cover.md]] — Definition: edge cover, $\beta'(G)$
- [[content/foundational/matching.md]] — Matchings and the construction used to relate matchings and edge covers
- [[content/theorems, lemma/theorem - matching + edge cover = n.md]] — Relation between maximum matching and minimum edge cover
