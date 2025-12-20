> [!theorem]
> ### Theorem 3.3.3 — Tutte's theorem
> A graph $G$ has a perfect matching if and only if
> $$
> o\bigl(G-S\bigr)\le \lvert S\rvert \text{for every } S\subseteq V(G),
> $$
> i.e. $G$ satisfies Tutte's condition.
> [!proof]
> Proof sketch.
> 
> (⇒) If $G$ has a perfect matching $M$, then every odd component of $G-S$ must contribute at least one vertex matched to $S$ under $M$. Hence $\lvert S\rvert\ge o(G-S)$.
> 
> (⇐) The nontrivial direction is proved by induction on $n=|V(G)|$. The notes give a full inductive proof: pick a maximal nonempty set $T$ with $o(G-T)=|T|$, show every component of $G-T$ is odd, remove one vertex from each component and apply the induction hypothesis to obtain perfect matchings on the resulting subgraphs, then use Hall's theorem on an auxiliary bipartite graph to match the vertices of $T$ to the components. See the detailed proof file for the complete induction with claims.
### Relations
- [[odd components]] — Definition of $o(H)$ and Tutte's condition (used in statement).
- [[theorem - Tutte's theorem (detailed proof)]] — Expanded full proof (induction and auxiliary claims).
- [[matching]] — Definitions of matchings, perfect matchings; Tutte characterizes existence of perfect matchings.

