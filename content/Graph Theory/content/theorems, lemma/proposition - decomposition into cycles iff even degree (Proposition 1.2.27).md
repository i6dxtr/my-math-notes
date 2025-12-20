#theorem
> [!theorem]
> ### Proposition — Decomposition into cycles iff every vertex has even degree (Proposition 1.2.27)
> Let $G$ be a (not-necessarily-simple) graph. Then $G$ can be decomposed into cycles (that is, its edge set is the disjoint union of cycles) if and only if every vertex of $G$ has even degree.
> [!proof]
> (⇒) If $G$ decomposes into cycles $\{C_1,\dots,C_t\}$ then every vertex is incident with either $0$ or $2$ edges from each $C_i$, hence has even degree.
> 
> (⇐) Suppose every vertex of $G$ has even degree. Proceed by induction on $m:=e(G)$. If $m=0$ the claim is trivial. For $m\ge 1$, since every vertex has even degree there exists a component in which every vertex has degree at least $2$; by Lemma 1.2.5 such a component contains a cycle $C$. Delete the edges of $C$ from $G$ to obtain $G'$. Every vertex of $G'$ still has even degree, and $e(G')<m$, so by the inductive hypothesis $G'$ decomposes into cycles. Together with $C$ this yields a decomposition of $G$ into cycles.
### Relations
- Handshake lemma and parity: [[handshake lemma]]
- Eulerian circuit and characterization: [[theorem - eulerian circuit condition]]
- Uses cycles and trail definitions: [[walk, trail, path, cycle]]
- Connected to decomposition techniques used in Tutte matching proofs and parity lemmas: see [[lemma - parity lemma (Tutte)|parity lemma (Tutte)]], [[theorem - Tutte's theorem|Tutte's theorem]].
