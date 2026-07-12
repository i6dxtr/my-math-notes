#graph-property
> [!definition]
> ### Identities & inequalities — Independent sets, matchings, and covers
> This note collects common equalities and inequalities relating the main packing/covering parameters of a graph:
> - independence number $\alpha(G)$,
> - vertex cover number $\beta(G)$,
> - matching number (maximum matching size) $\alpha'(G)$,
> - minimum edge cover size $\beta'(G)$,
> and related trivial bounds. Short proofs or proof sketches are given for the principal relations.

> [!remark]
> Notation recap:
> - $n(G)=|V(G)|$,
> - $\alpha(G)=\max\{|A| : A\subseteq V(G),\; G[A]\text{ has no edges}\}$,
> - $\beta(G)=\min\{|Q| : Q\subseteq V(G),\; Q\text{ meets every edge}\}$,
> - $\alpha'(G)=\max\{|M| : M\text{ a matching in }G\}$,
> - $\beta'(G)=\min\{|L| : L\subseteq E(G),\;L\text{ covers all vertices}\}$ (edge cover).
> All displayed relations use this notation.

> [!remark]
> Basic parameter bounds
> - Trivial ranges:
>   $$1\le \alpha(G)\le n(G),\qquad 0\le \alpha'(G)\le\Big\lfloor\frac{n(G)}{2}\Big\rfloor.$$
> - If $G$ has an isolated vertex then $\beta'(G)=\infty$ (by convention); otherwise $\beta'(G)\le n(G)-\alpha'(G)$ (see below).

> [!theorem]
> ### Complementarity of independent sets and vertex covers
> For every graph $G$,
> $$
> \alpha(G) + \beta(G) = n(G).
> $$

> [!proof]
> If $A\subseteq V(G)$ is independent then $V(G)\setminus A$ is a vertex cover (every edge has at least one endpoint outside $A$), hence $\beta(G)\le n(G)-\alpha(G)$. Conversely, if $Q$ is a vertex cover then $V(G)\setminus Q$ is independent, so $\alpha(G)\ge n(G)-\beta(G)$. Combining the two inequalities yields the identity.

---

> [!remark]
> This identity is often presented as a simple duality: independent sets and vertex covers are complements.

> [!theorem]
> ### Matching vs vertex cover (general inequality)
> For every graph $G$,
> $$
> \alpha'(G)\le \beta(G)\le 2\alpha'(G).
> $$

> [!proof]
> Left inequality ($\alpha'(G)\le\beta(G)$). Every vertex cover must contain at least one endpoint of each edge of any matching, so a cover has size at least the matching size.
> 
> Right inequality ($\beta(G)\le 2\alpha'(G)$). Let $M$ be a maximal matching (not necessarily maximum). The set $Q$ of all endpoints of edges in $M$ has size $2|M|$ and is a vertex cover: if an edge $e$ has both endpoints unsaturated by $M$, then $M\cup\{e\}$ would be a larger matching contradicting maximality. Taking $M$ as a maximum matching gives the bound $\beta(G)\le 2\alpha'(G)$.

> [!remark]
> The left inequality is tight in bipartite graphs (by König–Egerváry); the right inequality is tight for graphs composed of disjoint triangles (each triangle has $\alpha'=1$ and $\beta=2$).

---

> [!theorem]
> ### Matching and edge cover identity
> If $G$ has no isolated vertices, then
> $$
> \alpha'(G) + \beta'(G) = n(G).
> $$
> Equivalently, $\beta'(G)=n(G)-\alpha'(G)$.

> [!proof]
> Let $M$ be a maximum matching. Every vertex not saturated by $M$ must be incident to some edge; add one such incident edge per unsaturated vertex to extend $M$ to an edge cover. Counting gives an edge cover of size $|M| + (n-2|M|)=n-|M|$, hence $\beta'(G)\le n-\alpha'(G)$. The star-forest lemma (components of a minimum edge cover form stars) yields the reverse inequality and equality.

> [!remark]
> When a perfect matching exists ($\alpha'(G)=n/2$), a perfect matching is itself a minimum edge cover and $\beta'(G)=n/2$.

---

> [!remark]
> Bipartite exactness — König–Egerváry theorem:
> For bipartite graphs $G$ we have the stronger equality
> $$
> \alpha'(G)=\beta(G).
> $$
> See [[theorem - König–Egerváry (1931)|König–Egerváry (1931)]].

> [!remark]
> Additional useful inequalities and observations
> - Relation to degrees: $\alpha'(G) \ge \dfrac{e(G)}{\Delta(G)}$ (use simple average arguments and König–Egerváry for bipartite graphs; see Exercise 16(i) in lecture notes).
> - For bipartite $G=(X,Y)$ with $|X|=|Y|=n$, if $\delta(G)\ge n/2$ then $G$ has a perfect matching (Hall’s condition via degree counting).
> - Algorithmic corollary: in bipartite graphs, a maximum matching (e.g., Hopcroft–Karp) yields a minimum vertex cover via the standard alternating-path BFS construction.

### Relations
- Independent sets and vertex covers: [[independent set|independent set]], [[vertex cover|vertex cover]].
- Matchings and augmenting paths: [[matching|matching]], [[M-alternating path, M-augmenting path|augmenting paths]].
- Edge covers and the star-forest lemma: [[edge cover|edge cover]], [[lemma - star forest|Star forest lemma]].
- König–Egerváry theorem (bipartite equality): [[theorem - König–Egerváry (1931)|König–Egerváry (1931)]].
- Use this note as a quick reference when proving parameter bounds in exercises and theorems (Tutte, Hall, matching existence results).
~~~
