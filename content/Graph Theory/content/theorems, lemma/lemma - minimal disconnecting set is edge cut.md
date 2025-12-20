> [!lemma]
> ### Lemma — Every minimal disconnecting set is an edge cut
> Let $G$ be a graph on $n\ge 2$ vertices. Every minimal disconnecting set $F\subseteq E(G)$ is an edge‑cut: there exists a proper nonempty $S\subset V(G)$ such that
> $$
> F=[S,V(G)\setminus S].
> $$
> [!proof]
> Let $F$ be a minimal disconnecting set, so $G-F$ has more than one component. Let $H$ be a component of $G-F$. By minimality of $F$ there are no edges in $F$ with both endpoints in $V(H)$, and likewise no edges in $F$ with both endpoints in $V(G)\setminus V(H)$. Therefore every edge of $F$ has one endpoint in $V(H)$ and the other in $V(G)\setminus V(H)$, i.e.
> $$
> F=\bigl[V(H),\,V(G)\setminus V(H)\bigr],
> $$
> as required.
### Relations
- [[disconnecting set, edge-connectivity]] — Formal definitions of disconnecting sets and edge cuts.
- [[theorem - Whitney inequality (4.1.7)]] — This lemma is used in the proof of Whitney's inequality relating vertex- and edge-connectivity.
- [[vertex & edge deletion]] — Uses the notion of deleting edges $G-F$.

