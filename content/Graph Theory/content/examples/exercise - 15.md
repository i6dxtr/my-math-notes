> [!example]
> ### Exercise 15.
> (i) Complete the proof of Hall's theorem above.
> (ii) Let $G$ be an $X, Y$-bipartite graph such that $|X| = |Y| = n.$ Prove that if $\delta(G) \ge n/2,$ then $G$ has a perfect matching. (Hint: Prove that Hall's condition is satisfied)> [!proof]
> $(\Rightarrow)$ If $G$ has a matching $M$ which saturates $X,$ then clearly $|N(S)| \ge |S|$ for all $S \subseteq X$ (since $S$ is saturated by $M$).
> $(\Leftarrow)$ We prove the contrapositive Let $M$ be a maximum matching and suppose that $M$ doesn't saturate $X;$ i.e. there exists $u \in X$ so that $u$ is unsaturated by $M.$ Let
> 
> $$S = \{x \in X : \text{there exists an } M \text{ alternating } u,x\text{-path}\}$$
> 
> and
> 
> $$T = \{y \in Y : \text{there exists an } M \text{ alternating } u,y\text{-path}\}.$$
> 
> - First note that $u \in S.$
>     
> - Next note that every vertex in $T$ is saturated by $M;$ otherwise we would have an $M$-augmenting path, contradicting the fact that $M$ is a maximum matching.
>     
> - So $M$ matches $T$ with $S \setminus \{u\};$ thus $|T| = |S| - 1.$
>     
> - Note that any $M$-alternating path starting at $u$ (which necessarily begins with an edge not in $M$) and ending at $y \in T$ must end with an edge not in $M$ and any $M$-alternating path starting at $u$ and ending at $x \in S$ must end with an edge in $M.$
>     
> 
> We now show that $N(S) \subseteq T.$ Suppose for contradiction there exists $x' \in S$ and $y' \in Y \setminus T$ such that $x'y' \in E(G).$ But now the $M$-alternating path from $u$ to $x',$ together with the edge $x'y'$ gives us an $M$-alternating path from $u$ to $y',$ contradicting the fact that $y' \notin T.$ $\square$
> 
> Proof of Exercise 15(ii).
> 
> Let $S \subseteq X.$ If $|S| \le n/2,$ then since $\delta(G) \ge n/2,$ we have $|N(S)| \ge n/2 \ge |S|.$ So suppose $|S| > n/2.$ But now for all $y \in Y,$ $|N(y) \cap S| \ge |N(y)| + |S| - |X| > 0,$ so $|N(S)| = |Y| \ge |S|.$ Thus there is a matching saturating $X$ and since $G$ is balanced this is a perfect matching. $\square$
Relations
- [[content/foundational/matching.md]]
- [[content/theorems, lemma/theorem - Hall's theorem (Theorem 3.1.11).md]]
- [[content/theorems, lemma/theorem - König–Egerváry (1931).md]]
