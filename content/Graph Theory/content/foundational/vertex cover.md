#graph-property
> [!definition]
> ### Definition: Vertex cover
> Let $G$ be a graph. A set $Q\subseteq V(G)$ is a **vertex cover** if every edge of $G$ has at least one endpoint in $Q$.
> 
> The **vertex cover number** (minimum vertex cover size) is
> $$
> \beta(G)=\min\{\,|Q| : Q\subseteq V(G),\; Q\text{ is a vertex cover}\,\}.
> $$
> Equivalently, $Q$ is a vertex cover iff $V(G)\setminus Q$ is an independent set.

> [!remark]
> Key observations and useful bounds:
> - Complementarity with independent sets:
>   $$\alpha(G)+\beta(G)=n(G),$$
>   since the complement of any vertex cover is an independent set and vice versa.
> - Matching bound: any matching $M$ forces a cover to include at least one endpoint of each edge of $M$, so
>   $$\alpha'(G)\le \beta(G),$$
>   where $\alpha'(G)$ is the size of a maximum matching.
> - Approximation: taking both endpoints of every edge in a maximal matching yields a vertex cover of size at most $2\alpha'(G)$, so $\beta(G)\le 2\alpha'(G)$.
> - Bipartite exactness (König–Egerváry): in bipartite graphs $\beta(G)=\alpha'(G)$ (see the theorem file).
> - Computational note: finding a minimum vertex cover is NP‑complete in general, but polynomial-time solvable in bipartite graphs via matching algorithms (Hall / König).

### Examples
- In the complete graph $K_n$, $\beta(K_n)=n-1$ (every edge touches all but one vertex).
- For a disjoint union of $k$ triangles, $\beta(G)=2k$ while $\alpha'(G)=k$.
### Relations
- Complementary to [[independent set|independent set]].
- Related to [[matching|matching]] and [[maximal matching, maximum matching|maximal/maximum matching]].
- For bipartite graphs see [[theorem - König–Egerváry (1931)]].
- Connected to order & size: [[order, size|order, size]].
