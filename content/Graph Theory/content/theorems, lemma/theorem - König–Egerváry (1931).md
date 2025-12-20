> [!theorem]
> ### Theorem (König 1931, Egerváry 1931)
> Let $G=(X\cup Y,E)$ be a bipartite graph with bipartition $(X,Y)$. Then the size of a maximum matching equals the size of a minimum vertex cover:
> $$
> \alpha'(G)=\beta(G).
> $$
> In other words, in every bipartite graph the maximum number of pairwise disjoint edges equals the minimum number of vertices that meet every edge.
> [!proof]
> We prove $\beta(G)\le \alpha'(G)$ (the reverse inequality $\alpha'(G)\le\beta(G)$ is immediate: a vertex cover must pick at least one endpoint from each edge of any matching).
> 
> Let $M$ be a maximum matching in $G$ and let $Q$ be a minimum vertex cover. Write $Q_X=Q\cap X$ and $Q_Y=Q\cap Y$. Consider the induced subgraphs
> $$
> \begin{align*}
> H &= G\bigl[\,Q_X\ \cup\ (Y\setminus Q)\,\bigr],\\
> H'&= G\bigl[\,Q_Y\ \cup\ (X\setminus Q)\,\bigr].
> \end{align*}
> $$
> Since $Q$ is a vertex cover there are no edges between $X\setminus Q$ and $Y\setminus Q$, so every edge incident to a vertex of $X\setminus Q$ has its other endpoint in $Q_Y$, and similarly for $Y\setminus Q$.
> 
> We show that $H$ satisfies Hall’s condition for the part $Q_X$: for every $S\subseteq Q_X$ we must have $|N_H(S)|\ge |S|$. If some set $S\subseteq Q_X$ violated this, i.e. $|N_H(S)|<|S|$, then replacing $S$ inside the cover by $N_H(S)$ produces a smaller vertex cover:
> $$
> Q'=(Q\setminus S)\cup N_H(S).
> $$
> Indeed every edge with an endpoint in $S$ meets $N_H(S)$ by definition, and no new edges outside $Q'$ are uncovered since $N_H(S)\subseteq Y$. This contradicts the minimality of $Q$. Hence Hall’s condition holds in $H$, so by Hall’s theorem there exists a matching in $H$ that saturates $Q_X$; in particular there are $|Q_X|$ disjoint edges of $H$ matching $Q_X$ into $Y\setminus Q$.
> 
> An identical argument applied to $H'$ shows there exists a matching in $H'$ saturating $Q_Y$ (matching $Q_Y$ into $X\setminus Q$), giving $|Q_Y|$ disjoint edges.
> 
> Combining these two matchings yields a collection of $|Q_X|+|Q_Y|=|Q|$ disjoint edges in $G$. Therefore $|Q|\le |M|=\alpha'(G)$. Together with the trivial lower bound $\alpha'(G)\le\beta(G)$ we obtain $\alpha'(G)=\beta(G)$ as required.
> [!remark]
> Remarks and consequences:
> - The theorem gives an exact duality between matching and covering in bipartite graphs and underlies many algorithmic results (maximum bipartite matching can be used to compute minimum vertex covers).
> - A standard constructive proof produces a minimum vertex cover from a maximum matching using the alternating‑path / BFS exploration from unmatched vertices; this is the basis of the Kőnig algorithmic correspondence (often taught alongside the proof of Hall’s theorem).
> - Together with Hall’s theorem, König–Egerváry provides several useful corollaries, for example that every $k$‑regular bipartite graph has a perfect matching.
### Relations
- [[matching|matching]] and [[maximal matching, maximum matching|maximal/maximum matching]]
- [[vertex cover|vertex cover]] and [[independent set|independent set]]
- [[theorem - Hall's theorem (Theorem 3.1.11)|Hall’s theorem (Theorem 3.1.11)]] — used in the proof
- Algorithmic remark: see [[example - blossom algorithm remark|blossom algorithm remark]] for matching algorithms (general graphs)