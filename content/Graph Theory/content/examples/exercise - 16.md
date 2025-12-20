> [!example]
> ### Exercise 16.
> (i) Prove that for every bipartite graph $G$ we have $\alpha'(G) \ge \frac{e(G)}{\Delta(G)}.$ (Hint: Use the K\u00f6nig-Egerv\u00e1ry theorem)
> 
> (ii) Finish the following proof of Hall's theorem using the K\u00f6nig-Egerv\u00e1ry theorem.
> 
> ad-proof
> **Proof of i.**
> 
> Let $Q$ be a minimum vertex cover of $G$ and note that since every edge is incident with at least one vertex in $Q,$ we have
> 
> $$e(G) \le \sum_{v \in Q} d(v) \le |Q|\Delta(G) = \beta(G)\Delta(G) = \alpha'(G)\Delta(G),$$
> 
> where the last inequality holds by the K\u00f6nig-Egerv\u00e1ry theorem. $\square$~~~ad-proof
**Proof of ii.**.
Proof of Hall's using K\u00f6nig-Egerv\u00e1ry. (Contrapositive: If there is no matching saturating $X,$ then there exists a set $S' \subseteq X$ such that $|N(S')| < |S'|$)

Let $G$ be an $X, Y$-bipartite graph and suppose there is no matching saturating $X.$ Let $M$ be a maximum matching and note that by the previous assumption $|M| < |X|.$ So by Theorem 3.1.16, there exists a vertex cover $Q$ such that $|Q| = |M| < |X|.$ Let $Q_X = Q \cap X$ and let $Q_Y = Q \cap Y.$ Note that since

$$|Q_X| + |Q_Y| = |Q| < |X| = |Q_X| + |X \setminus Q|,$$

we have $|Q_Y| < |X \setminus Q|.$ However, since $Q = Q_X \cup Q_Y$ is a vertex cover, $N(X \setminus Q) \subseteq Q_Y$ and thus $|N(X \setminus Q)| \le |Q_Y| < |X \setminus Q|,$ giving us a set $X \setminus Q$ failing Hall's condition. $\square$


Relations
- [[content/theorems, lemma/theorem - König–Egerváry (1931).md]]
- [[content/theorems, lemma/theorem - Hall's theorem (Theorem 3.1.11).md]]
- [[content/foundational/vertex cover.md]]
