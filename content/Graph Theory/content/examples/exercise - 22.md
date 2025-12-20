> [!example]
> ### Exercise 22. *(Expansion Lemma)*
> _If $G$ is a $k$-connected graph and $G'$ is obtained from $G$ by adding a new vertex which is adjacent to at least $k$ vertices in $G,$ then $G'$ is $k$-connected._
> 
> **Lemma 4.2.3 (Expansion Lemma).** _If $G$ is a $k$-connected graph and $G'$ is obtained from $G$ by adding a new vertex $z$ which is adjacent to at least $k$ vertices in $G,$ then $G'$ is $k$-connected._~~~ad-proof
Note that since $G$ is $k$ connected, $G$ has at least $k+1$ vertices. Let $G'$ be obtained from $G$ by adding a new vertex $z$ and making $z$ adjacent to at least $k$ vertices in $G.$ * Let $S' \subseteq V(G')$ with $|S'| \le k-1.$ Let $S = S' \cap V(G)$ and consider $G' - S'.$
- If $z \in S',$ then $G' - S' = G - S$ and since $G$ is $k$-connected and $|S| = |S'| - 1 \le k-2,$ $G-S = G' - S'$ is connected; i.e. $S'$ is not a separating set of $G'.$
- If $z \notin S',$ then $S = S'.$ Since $|S| = |S'| \le k-1$ and $G$ is $k$-connected, $G-S$ is connected and $z$ has at least one neighbor in $G-S,$ so $G' - S'$ is connected.
- Thus $G'$ is $k$-connected. $\square$


Relations
- [[theorem - 2-connected via internally disjoint paths]]
- [[ Menger-type equivalences]]
- [[separating set, connectivity]]
