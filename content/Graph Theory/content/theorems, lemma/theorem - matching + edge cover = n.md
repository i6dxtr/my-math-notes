
> [!theorem]
> ### Theorem — Matching and edge-cover complementarity
> Let $G$ be a graph on $n$ vertices with no isolated vertices. Then
> $$\alpha'(G) + \beta'(G) = n,$$
> where $\alpha'(G)$ is the size of a maximum matching and $\beta'(G)$ is the size of a minimum edge cover.
> ![[Pasted image 20251015141231.png|350]]

> [!proof]
> We prove equality by showing both inequalities.
> 
> (≤) Let $M$ be a maximum matching in $G$. Every vertex not covered by $M$ (that is, in $V(G)\setminus V(M)$) has at least one neighbor because $G$ has no isolated vertices. For each vertex $v\in V(G)\setminus V(M)$ choose one incident edge joining $v$ to some vertex of $V(M)$. Take the set $L$ consisting of the edges of $M$ together with the chosen edges. Every vertex of $G$ is incident with an edge of $L$, so $L$ is an edge cover. Thus
> $$\beta'(G)\le |L| = |M| + (|V(G)| - 2|M|) = n - |M| = n - \alpha'(G).$$
> 
> (≥) Let $L$ be a minimum edge cover of $G$. By the star-forest lemma, each component of $H=(V(G),L)$ is a non-trivial star. From each star component choose one edge incident with its center; these chosen edges form a matching $M'$ (one chosen edge per star). Every star with $k\ge 1$ edges contributes exactly one edge to $M'$, while covering $k+1$ vertices in the component. Summing over all components gives
> $$|L| = \sum (k_i) \quad\text{and}\quad n = \sum (k_i+1) = |L| + (\#\text{components}).$$
> Since $M'$ has size equal to the number of components, $|M'| = n - |L|$. As $M'$ is a matching, $\alpha'(G)\ge |M'| = n - |L|$. Rearranging gives $|L| \ge n - \alpha'(G)$. Because $L$ was a minimum edge cover, $\beta'(G)=|L|\ge n-\alpha'(G)$.
> 
> Combining the two inequalities yields $\alpha'(G)+\beta'(G)=n$.
Relations
- [[matching]] — Matchings, $\alpha'(G)$
- [[edge cover]] — Edge covers, $\beta'(G)$
- [[lemma - star forest]] — Star-forest structure of minimum edge covers (used in the proof)
- [[theorem - matching + edge cover = n]] — (this file)
