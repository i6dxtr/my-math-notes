> [!theorem]
> ### Lemma — Complementarity of independent sets and vertex covers
> For every graph $G$ on $n$ vertices,
> $$\alpha(G) + \beta(G) = n.$$
![[Pasted image 20251015134855.png|300]]

> [!proof]
> Let $G=(V,E)$. If $Q$ is a vertex cover of $G$, then $V\setminus Q$ is an independent set, since no edge has both endpoints in $V\setminus Q$. Conversely, if $A$ is an independent set of $G$, then $V\setminus A$ is a vertex cover. Therefore a minimum vertex cover $Q$ satisfies that $V\setminus Q$ is a maximum independent set, and hence
> $$\alpha(G)=|V\setminus Q|=n-\beta(G).$$
> Rearranging gives $\alpha(G)+\beta(G)=n$.
Relations
- [[independent set]] — Independent set, $\alpha(G)$
- [[vertex cover]] — Vertex cover, $\beta(G)$ (see also [[matching]] for relations via Kőnig–Egerváry in bipartite graphs)
- [[lemma - alpha plus beta equals n]] — (this file)
