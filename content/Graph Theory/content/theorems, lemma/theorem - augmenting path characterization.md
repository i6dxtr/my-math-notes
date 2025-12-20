#theorem
> [!theorem]
> ### Theorem — Augmenting‑path characterization of maximum matchings
> A matching $M$ in a graph $G$ is a maximum matching in $G$ if and only if $G$ has no $M$‑augmenting path.
> [!remark]
> Given an $M$‑augmenting path $P$, toggling the edges of $P$ (replace $M\cap E(P)$ by $E(P)\setminus M$) increases the matching size by $1$. Thus the existence of an $M$‑augmenting path implies $M$ is not maximum.
> [!proof]
> $(\Rightarrow)$ Suppose $G$ has an $M$‑augmenting path $P$. Let $E' = E(P)\setminus M$ and note that
> $$\bigl|(M\setminus (E(P)\cap M))\cup E'\bigr| = |M|+1.$$
> No edge of $M\setminus E(P)$ is incident with the interior vertices of $P$, and by definition the endpoints of $P$ are not incident with edges of $M\setminus E(P)$, so the union above is indeed a matching. Hence $M$ is not maximum.
> 
> $(\Leftarrow)$ Suppose $M$ is not maximum. Let $M'$ be a maximum matching and set $F = M\triangle M'$. By Lemma 3.1.9 every component of $F$ is either a path or an even cycle. If every component had at least as many edges of $M$ as $M'$, then $|M'|\le|M|$, contradicting maximality of $M'$. Hence some component is a path with more edges from $M'$ than from $M$, and that path is an $M$‑augmenting path.
### Relations
- Relies on structural Lemma 3.1.9: [[lemma - symmetric difference of matchings (Lemma 3.1.9)|Lemma 3.1.9]].
- Uses definitions in [[matching|matching]] and [[M-alternating path, M-augmenting path|M‑alternating / M‑augmenting path]].
- Connects to matching algorithms and Hall's theorem for bipartite matchings.
