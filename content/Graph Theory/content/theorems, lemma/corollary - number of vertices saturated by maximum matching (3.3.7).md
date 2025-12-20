> [!corollary]
> ### Corollary 3.3.7 — Number of vertices saturated by a maximum matching
> Let $G$ be a graph on $n$ vertices and define
> $$
> d \;=\; \max\{\,o(G-S)-|S| : S\subseteq V(G)\,\}.
> $$
> Then the number of vertices of $G$ saturated by a maximum matching in $G$ is exactly $n-d$.
> [!proof]
> First note $d\ge 0$ because taking $S=\emptyset$ gives $o(G)-0\ge 0$.
> 
> Lower bound on unsaturated vertices. For any $S\subseteq V(G)$, every matching leaves at least $o(G-S)-|S|$ vertices unsaturated: each odd component of $G-S$ requires at least one vertex unmatched to $S$. Taking the maximum over $S$ shows every matching leaves at least $d$ vertices unsaturated, so every matching saturates at most $n-d$ vertices.
> 
> Existence (achievability). Let $K$ be a set of $d$ new vertices and form $G'$ by adding $K$ to $G$ and joining every vertex of $K$ to every vertex of $V(G)\cup K$ (i.e. make $K$ universal and clique among themselves). By the parity lemma, $n$ and $d$ have the same parity, so $|V(G')|=n+d$ is even.
> 
> We claim $G'$ satisfies Tutte's condition. Let $S\subseteq V(G')$ and consider two cases.
> 
> Case 1: $K\not\subseteq S$. Then $G'-S$ contains at least one vertex from $K$, and since vertices of $K$ are adjacent to all others the graph $G'-S$ is connected; hence $o(G'-S)\le 1\le |S|$.
> 
> Case 2: $K\subseteq S$. Put $S'=S\cap V(G)$. Then $G'-S=G-S'$, so
> $$
> o(G'-S)=o(G-S')\le |S'|+d = |S|.
> $$
> 
> Thus $G'$ satisfies Tutte's condition and, by Tutte's theorem, $G'$ has a perfect matching $M'$. Restricting $M'$ to edges with both endpoints in $V(G)$ yields a matching $M$ in $G$ that saturates at least $n-d$ vertices. Combined with the upper bound above, this shows a maximum matching saturates exactly $n-d$ vertices.
### Relations
- [[content/theorems, lemma/theorem - Tutte's theorem.md]] — Uses Tutte's theorem to produce a perfect matching in the augmented graph $G'$.
- [[content/theorems, lemma/lemma - parity lemma (Tutte).md]] — Parity is used to ensure $|V(G')|$ is even when adding $d$ vertices.
- [[content/foundational/matching.md]] — Connects the corollary to the standard definitions of saturation, maximum and perfect matchings.

Source: Notes by date/10-22-25.md
