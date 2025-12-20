#theorem
> [!theorem]
> ### Theorem — Bipartite Characterization
> A graph $G$ is bipartite if and only if $G$ contains no odd cycle.
> [!proof]
> (⇒) If $G$ is bipartite with bipartition $(A,B)$ then any closed walk alternates between $A$ and $B$, so every closed walk has even length. In particular, $G$ contains no odd cycle.
> 
> (⇐) Conversely, suppose $G$ contains no odd cycle. Work component‑wise, so assume $G$ is connected. Choose a root $x\in V(G)$ and partition
> $$
> A=\{v\in V(G): d(x,v)\text{ is even}\},\qquad B=\{v\in V(G): d(x,v)\text{ is odd}\}.
> $$
> Clearly $A\cup B=V(G)$ and $A\cap B=\varnothing$. If there were an edge $uv$ with $u,v\in A$, then there exist even‑length paths $x\!\leadsto\!u$ and $x\!\leadsto\!v$, and concatenating these with the edge $uv$ yields a closed odd walk; by Lemma 1.2.15 every closed odd walk contains an odd cycle, contradicting the hypothesis. Thus no edge has both endpoints in $A$. The same argument applies to $B$. Therefore $(A,B)$ is a bipartition of $G$, and $G$ is bipartite.
### Relations
- Uses Lemma 1.2.15 ([[content/theorems, lemma/lemma - odd walk contains odd cycle.md|odd walk → odd cycle]]).
- Connects to coloring: bipartite graphs satisfy $\chi(G)\le 2$ ([[content/foundational/chromatic number.md|chromatic number]]).
- Frequently applied in matching theory and structural arguments (see related notes on matchings and Hall's theorem).
- Forms a backbone for many later matching results (Kőnig–Egerváry, Hall's theorem) where bipartite structure simplifies parity and covering arguments ([[content/theorems, lemma/theorem - KÃ¶nigâ€“EgervÃ¡ry (1931).md|KÃ¶nig–Egerváry]]; [[content/theorems, lemma/theorem - Hall's theorem (Theorem 3.1.11).md|Hall's theorem]]).
