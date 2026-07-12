> [!corollary]
> ### Corollary 3.3.8 *(Petersen 1891)*
> Every $3$-regular graph with no cut-edge has a perfect matching.

> [!proof]
> We show the graph $G$ satisfies Tutte's condition, hence by Tutte's theorem $G$ has a perfect matching.
> 
> Let $S\subseteq V(G)$. If $S=\emptyset$ then by the Handshake lemma every component of $G$ has even order, so $o(G)=0=|S|$.
> 
> Assume $S\neq\emptyset$. Let $H$ be an odd component of $G-S$. By the Handshake lemma the total degree of vertices of $H$ is odd, hence the number of edges joining $V(H)$ to $S$, denoted $e(V(H),S)$, is odd. Because $G$ has no cut-edges we cannot have $e(V(H),S)=1$ (that would make some edge a bridge), so $e(V(H),S)\ge 3$. Summing over all odd components of $G-S$ gives
> $$
> 3\,o(G-S) \le \sum_{H\ \text{odd comp.}} e\bigl(V(H),S\bigr) \le e\bigl(V(G)-S,\,S\bigr).
> $$
> But each vertex in $S$ has degree $3$, so $e(V(G)-S,S)\le 3|S|$. Therefore
> $$
> 3\,o(G-S)\le 3|S| \Longrightarrow o(G-S)\le |S|.
> $$
> 
> Thus Tutte's condition holds for every $S\subseteq V(G)$, and by Tutte's theorem $G$ has a perfect matching. ∎
### Relations
- [[theorem - Tutte's theorem]] — Applies Tutte's theorem to deduce existence of a perfect matching.
- [[handshake lemma]] — Uses degree-sum parity facts to bound boundary edges from odd components.
- [[cut-vertex, cut-edge]] — Uses the "no cut-edge" hypothesis to rule out the case e(V(H),S)=1.

