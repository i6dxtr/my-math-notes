
> [!corollary]
> ### Lemma — Parity relation for Tutte's condition
> Let $G$ be a graph on $n$ vertices. For every $S\subseteq V(G)$, the integers $o(G-S)-|S|$ and $n$ have the same parity; equivalently,
> $$n\equiv o(G-S)-|S|\pmod 2.$$
> [!proof]
> Observe that removing $S$ from $G$ partitions the vertex set into the vertices of $S$ and the vertices of $G-S$. Each odd component of $G-S$ contributes an odd number to the total number of vertices in $G-S$, while each even component contributes an even number. Therefore the parity of $|V(G-S)|$ equals the parity of $o(G-S)$. Since $|V(G)|=|S|+|V(G-S)|$, we have
> $$n-|S|\equiv o(G-S)\pmod 2,$$
> which rearranges to the stated congruence.
Relations
- [[content/foundational/odd components.md]] — Definition: odd components
- [[content/theorems, lemma/theorem - Tutte's theorem.md]] — Tutte's theorem
- [[content/foundational/components (graph).md]] — Component counting and parity arguments
