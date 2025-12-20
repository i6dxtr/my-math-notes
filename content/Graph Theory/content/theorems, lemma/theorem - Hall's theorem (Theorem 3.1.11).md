#theorem
> [!theorem]
> ### Theorem 3.1.11 — Hall's Marriage Theorem
> Let $G$ be an $X,Y$‑bipartite graph. Then $G$ has a matching that saturates $X$ if and only if
> $$|N(S)| \ge |S| \quad\text{for all } S\subseteq X.$$
> [!proof]
> (⇒) If $G$ has a matching $M$ which saturates $X$, then clearly $|N(S)|\ge |S|$ for all $S\subseteq X$ (since every vertex of $S$ is matched to a distinct vertex in $N(S)$).
> 
> (⇐) [We prove the contrapositive] Let $M$ be a maximum matching and suppose that $M$ doesn't saturate $X$; i.e. there exists $u\in X$ so that $u$ is unsaturated by $M$. Let
> $$
> S=\{x\in X : \text{ there exists an }M\text{‑alternating }u,x\text{‑path}\}
> $$
> and
> $$
> T=\{y\in Y : \text{ there exists an }M\text{‑alternating }u,y\text{‑path}\}.
> $$
> First note that $u\in S$. Next note that every vertex in $T$ is saturated by $M$; otherwise we would have an $M$‑augmenting path, contradicting the fact that $M$ is a maximum matching. So $M$ matches $T$ with $S\setminus\{u\}$; thus $|T|=|S|-1$. Note that any $M$‑alternating path starting at $u$ (which necessarily begins with an edge not in $M$) and ending at $y\in T$ must end with an edge not in $M$ and any $M$‑alternating path starting at $u$ and ending at $x\in S$ must end with an edge in $M$.
> 
> We now show that $N(S)\subseteq T$. Suppose for contradiction that there exists $v\in N(S)\setminus T$. Then $v$ is adjacent to some $x\in S$ but there is no $M$‑alternating path from $u$ to $v$. Construct an $M$‑alternating path from $u$ to $x$ (one exists by definition of $S$) and append the edge $xv$; this yields an $M$‑alternating path from $u$ to $v$, contradiction. Therefore $N(S)\subseteq T$, so $|N(S)|\le |T|=|S|-1$, which contradicts the hypothesis that $|N(S)|\ge |S|$ for all $S\subseteq X$. This completes the proof.
### Relations
- Uses alternating/augmenting path definitions: [[M-alternating path, M-augmenting path|M‑alternating / M‑augmenting path]].
- Structural lemma on symmetric differences is relevant: [[lemma - symmetric difference of matchings (Lemma 3.1.9)|Lemma 3.1.9]].
- Relates to matching basics: [[matching|matching]] and maximal vs maximum matching [[maximal matching, maximum matching|maximal/maximum matching]].
- Applied in examples such as the deck‑of‑cards selection problem and many bipartite matching algorithms.


