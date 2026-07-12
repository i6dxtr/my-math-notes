
> [!example] Exercise 15.
> (i) Complete the proof of Hall's theorem above.
> (ii) Let $G$ be an $X, Y$-bipartite graph such that $|X| = |Y| = n.$ Prove that if $\delta(G) \ge n/2,$ then $G$ has a perfect matching. (Hint: Prove that Hall's condition is satisfied)

> [!proof]
>
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

---

> [!example] Exercise 16.
>
> (i) Prove that for every bipartite graph $G$ we have $\alpha'(G) \ge \frac{e(G)}{\Delta(G)}.$ (Hint: Use the König-Egerváry theorem)
>
> (ii) Finish the following proof of Hall's theorem using the König-Egerváry theorem.
>

> [!proof]
> **Proof of i.**
>
> Let $Q$ be a minimum vertex cover of $G$ and note that since every edge is incident with at least one vertex in $Q,$ we have
>
> $$e(G) \le \sum_{v \in Q} d(v) \le |Q|\Delta(G) = \beta(G)\Delta(G) = \alpha'(G)\Delta(G),$$
>
> where the last inequality holds by the König-Egerváry theorem. $\square$
>

> [!proof]
> **Proof of ii.**.
> Proof of Hall's using König-Egerváry. (Contrapositive: If there is no matching saturating $X,$ then there exists a set $S' \subseteq X$ such that $|N(S')| < |S'|$)
>
> Let $G$ be an $X, Y$-bipartite graph and suppose there is no matching saturating $X.$ Let $M$ be a maximum matching and note that by the previous assumption $|M| < |X|.$ So by Theorem 3.1.16, there exists a vertex cover $Q$ such that $|Q| = |M| < |X|.$ Let $Q_X = Q \cap X$ and let $Q_Y = Q \cap Y.$ Note that since
>
> $$|Q_X| + |Q_Y| = |Q| < |X| = |Q_X| + |X \setminus Q|,$$
>
> we have $|Q_Y| < |X \setminus Q|.$ However, since $Q = Q_X \cup Q_Y$ is a vertex cover, $N(X \setminus Q) \subseteq Q_Y$ and thus $|N(X \setminus Q)| \le |Q_Y| < |X \setminus Q|,$ giving us a set $X \setminus Q$ failing Hall's condition. $\square$

---

> [!example] Exercise 17.
>
>
> (i) We proved part of Theorem 3.1.22 by showing that $\beta'(G) \le n - \alpha'(G).$ Now finish the proof by proving that $\beta'(G) \ge n - \alpha'(G).$ (Hint: Start by letting $L$ be a minimum edge cover and then apply the Star Forest Lemma.)
>
> (ii) Prove that if $G$ is a bipartite graph with no isolated vertices, then $\alpha(G) = \beta'(G).$ (Hint: What is implied by Lemma 3.1.21 and Theorem 3.1.22?)
>

> [!proof]
> **Proof of i.**
>
> Let $M$ be a maximum matching in $G.$ Since $M$ is maximum, every other edge has at least one endpoint in $M$ and since $G$ has no isolated vertices, every vertex not incident with an edge in $M$ is incident with some edge having exactly one endpoint in $M.$ Thus there exists an edge cover of size $|M| + (n - 2|M|) = n - |M| = n - \alpha'(G).$ i.e. $\beta'(G) \le n - \alpha'(G).$
>
> Next we show that $\beta'(G) \ge n - \alpha'(G).$ Let $L$ be a minimum edge cover of $G.$ By the Star Forest Lemma, every component of $L$ is a star. Say that $L$ has $k$ components. So there is a matching with $k$ edges (one from each component). There are $k$ center vertices and thus $n-k$ leaf vertices, so the number of edges in $L$ is $n-k.$ Thus $|L| = n-k = n - |M|$ and thus $\beta'(G) = n - |M| \ge n - \alpha'(G).$ Thus $\alpha'(G) + \beta'(G) = n.$ $\square$
>
> **Proof of ii.**
>
> By Lemma 3.1.21 and Theorem 3.1.22 we have
>
> $$\alpha(G) + \beta(G) = n = \alpha'(G) + \beta'(G)$$
>
> and since $G$ is bipartite we have $\alpha'(G) = \beta(G).$ Together, this implies that $\alpha(G) = \beta'(G).$ $\square$

---

> [!example] Exercise 18. Let $G$ be an $X, Y$-bipartite graph and let $d = \max\{|S| - |N(S)| : S \subseteq X\}.$
>
> (i) Prove that $d \ge 0.$
>
> (ii) Prove that $G$ has a matching saturating all but $d$ many vertices in $X.$ (Hint: Create a new graph $G'$ by adding an independent set of $d$ vertices which are adjacent to everything in $X.$ Now prove that $G'$ has a matching which saturates $X.$)
>
> Proof of Exercise 18.
>
> Theorem ("Deficiency version" of Hall's theorem, see Exercise 3.1.32). Let $G$ be an $X, Y$-bipartite graph and let $d = \max\{|S| - |N(S)| : S \subseteq X\}.$ The number of vertices of $X$ saturated by a maximum matching in $G$ is exactly $|X| - d.$ Equivalently, if there exists a non-negative integer $d$ such that $|N(S)| + d \ge |S|$ for all $S \subseteq X,$ then $G$ has a matching saturating all but at most $d$ vertices of $G.$
>
> **Proof.** Let $d = \max\{|S| - |N(S)| : S \subseteq X\}$ and note that $d \ge 0$ since $|\emptyset| - |N(\emptyset)| = 0.$ Note that for all $S \subseteq X,$ at least $|S| - |N(S)|$ vertices of $X$ are unsaturated by any matching, so every matching saturates at most $|X| - d$ vertices of $X.$
>
> Let $G'$ be the bipartite graph obtained from $G$ by adding an independent set $Y'$ of order $d$ and making it adjacent to every vertex in $X.$ Let $S' \subseteq X$ and note that $|N_{G'}(S')| = |N_G(S')| + d \ge |S'|.$ Thus $G'$ has a matching $M'$ saturating $X.$ Let $M$ be the matching consisting of edges from $M'$ which are in $G.$ Thus $M$ saturates $|X| - d$ vertices in $X.$ $\square$

---

> [!example] Exercise 19.
> Let $G$ be a graph such that $\beta(G) = 2\alpha'(G).$
>
> (i) Prove that $\max\{o(G-S) - |S| : S \subseteq V(G)\} = \alpha(G).$ (Hint: Lemma 3.1.21 says something about $n - \alpha(G)$ and Corollary 3.3.7 says something about $n - \max\{o(G-S) - |S| : S \subseteq V(G)\}.)$
>
> (ii) Prove that every component of $G$ is a clique with an odd number of vertices. (Hint: Begin by choosing a set $S$ achieving the maximum in part (i).)
>

> [!proof]
> By Lemma 3.1.21 and the assumption, we have $n - \alpha(G) = \beta(G) = 2\alpha'(G).$ So by Corollary 3.3.7, we have $n - \alpha(G) = 2\alpha'(G) = n - \max\{o(G-S) - |S| : S \subseteq V(G)\}$ and thus $\max\{o(G-S) - |S| : S \subseteq V(G)\} = \alpha(G).$ Let $S$ be a set achieving the maximum; i.e. let $S \subseteq V(G)$ such that $o(G-S) - |S| = \alpha(G).$
>
> - If $|S| \ge 1,$ then $o(G-S) \ge \alpha(G) + |S| > \alpha(G),$ but choosing exactly one vertex from each odd component of $G-S$ gives us an independent set in $G-S$ (which is an independent set in $G$) with more than $\alpha(G)$ vertices, a contradiction.
>
> - So suppose $S = \emptyset.$ In this case we have $o(G) = \alpha(G),$ which also implies that $G$ has no even components because again, this would give a larger independent set. * So every component of $G$ is odd. Furthermore, every component of $G$ is a clique, because otherwise we would have two non-adjacent vertices in some component of $G$ which would again give us an independent set of order larger than $\alpha(G)$ which is impossible.
>
> - Thus every component of $G$ is an odd clique. $\square$

---

> [!example] Exercise 20.
> _Let $n \ge 2.$ Prove that if $G$ is a graph on $n$ vertices with $\delta(G) \ge n-2,$ then $\kappa(G) = \delta(G).$_
>

> [!proof]
> If $\delta(G) = n-1,$ then $G$ is complete and we have $\kappa(G) = n-1 = \delta(G).$ So suppose $\delta(G) = n-2.$
> - Let $x$ be a vertex with $d(x) = n-2$ and let $y$ be the vertex such that $xy \notin E(G).$ Note that $V(G) \setminus \{x,y\}$ is a vertex cut, so $\kappa(G) \le n-2.$ * Note that for all $u, v \in V(G)$ with $uv \notin E(G),$ we have $|N(u) \cap N(v)| = d(u) + d(v) - (n-2) \ge 2(n-2) - (n-2) = n-2.$
> - Let $S \subseteq V(G)$ with $|S| \le n-3$ and let $u, v \in V(G) \setminus S.$ We have $|N(u) \cap N(v)| \ge n-2$ and thus $u$ and $v$ have a common neighbor in $V(G) \setminus S$ which means $G-S$ is connected. $\square$

---

Proof of Exercise 21.

(i) Let $G$ be a graph on $n$ vertices and let $v \in V(G).$ If $G-v$ is complete, then $\kappa(G-v) = n-1-1 \ge \kappa(G)-1.$ So suppose $G-v$ is not complete and let $S'$ be a minimum vertex cut of $G-v.$ If $|S'| \le \kappa(G) - 2,$ then $S' \cup \{v\}$ is a vertex cut of size at most $\kappa(G) - 1$ in $G-v$ (sic), which is not possible, so $|S'| \ge \kappa(G) - 1$ which proves the first claim.

(ii) Let $e \in E(G)$ and let $F'$ be a minimum disconnecting set of $G-e.$ If $|F'| \le \kappa'(G)-2,$ then $F' \cup \{e\}$ is an disconnecting set of size at most $\kappa'(G)-1,$ which is not possible, so $|F'| \ge \kappa'(G)-1.$ Let $F$ be a minimum disconnecting set of $G,$ then clearly $F \setminus \{e\}$ (which may equal $F$) is an disconnecting set in $G-e,$ so $\kappa'(G) \ge \kappa'(G-e).$

_For the example, let $0 \le k < \ell$ and let $G$ be the graph consisting of a complete graph $K_{\ell+1}$ together with a vertex $v$ having $k$ neighbors in $K_{\ell+1}.$ We have $\kappa(G) = k,$ but $\kappa(G-v) = \kappa(K_{\ell+1}) = \ell.$_ $\square$

---

> [!example] Exercise 22. *(Expansion Lemma)*
> _If $G$ is a $k$-connected graph and $G'$ is obtained from $G$ by adding a new vertex which is adjacent to at least $k$ vertices in $G,$ then $G'$ is $k$-connected._
>
> **Lemma 4.2.3 (Expansion Lemma).** _If $G$ is a $k$-connected graph and $G'$ is obtained from $G$ by adding a new vertex which is adjacent to at least $k$ vertices in $G,$ then $G'$ is $k$-connected._
>

> [!proof]
> Note that since $G$ is $k$ connected, $G$ has at least $k+1$ vertices. Let $G'$ be obtained from $G$ by adding a new vertex $z$ and making $z$ adjacent to at least $k$ vertices in $G.$ * Let $S' \subseteq V(G')$ with $|S'| \le k-1.$ Let $S = S' \cap V(G)$ and consider $G' - S'.$
> - If $z \in S',$ then $G' - S' = G - S$ and since $G$ is $k$-connected and $|S| = |S'| - 1 \le k-2,$ $G-S = G' - S'$ is connected; i.e. $S'$ is not a separating set of $G'.$
> - If $z \notin S',$ then $S = S'.$ Since $|S| = |S'| \le k-1$ and $G$ is $k$-connected, $G-S$ is connected and $z$ has at least one neighbor in $G-S,$ so $G' - S'$ is connected.
> - Thus $G'$ is $k$-connected. $\square$
>

---

> [!example] Exercise 23. Let $G$ be a graph with at least four vertices. Prove that the following are equivalent:
>
> (i) $G$ is 2-connected
>
> (ii) for every $x \in V(G)$ and every $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2,$ there exists two paths $P$ and $Q$ such that $x$ is an endpoint of $P$ and $Q$ and the other endpoint of $P$ and $Q$ is in $Y$ and $(V(P) \setminus \{x\}) \cap (V(Q) \setminus \{x\}) = \emptyset$
>
> (iii) for all disjoint $X, Y \subseteq V(G)$ with $|X|, |Y| \ge 2,$ there are two disjoint paths $P$ and $Q$ such that $P$ and $Q$ each have one endpoint in $X$ and the other in $Y.$
>
> (Hint: As I mentioned in class, the Expansion Lemma will be helpful in proving (i) $\Rightarrow$ (ii) $\Rightarrow$ (iii))
>

> [!proof]
>
> (i) $\Rightarrow$ (ii) Suppose $G$ is 2-connected. Let $x \in V(G)$ and $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2.$ Add a vertex $y'$ such that $y'$ has 2 neighbors in $Y$ to get a graph $G'$ which is still 2-connected by the Expansion Lemma. By Theorem 4.2.2, $G'$ has two internally disjoint $x, y'$-paths $P', Q'.$ Now $P = P' - y'$ and $Q = Q' - y'$ are the paths we are looking for.
>
> (i) $\Leftarrow$ (ii) Suppose that for every $x \in V(G)$ and every $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2,$ there exists two $x, Y$-paths $P$ and $Q$ such that $(V(P) \setminus \{x\}) \cap (V(Q) \setminus \{x\}) = \emptyset.$ Suppose for contradiction $\kappa(G) \le 1.$ If $\kappa(G) = 0,$ let $\{x, y, y'\}$ be chosen so that $x$ is in a different component from $y$ and $y'.$ Now let $Y = \{y, y'\}.$ Using the property of $G,$ there is a path from $x$ to $y$ and $y',$ a contradiction. So suppose $\kappa(G) = 1$ and let $y$ be a cut vertex of $G.$ Let $x$ and $y'$ be chosen so that $x$ is in a different component of $G-y$ from $y'.$ Now let $Y = \{y, y'\}.$ So there is an $x, y$-path $P$ and $x, y'$-path $Q$ such that $P-x$ is disjoint from $Q-x,$ but every path from $x$ to $y'$ goes through $y,$ a contradiction.
>
> (ii) $\Rightarrow$ (iii) Suppose that for every $x \in V(G)$ and every $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2,$ there exists two $x, Y$-paths $P$ and $Q$ such that $(V(P) \setminus \{x\}) \cap (V(Q) \setminus \{x\}) = \emptyset.$ Since we know that (i) $\Leftrightarrow$ (ii), we have that $G$ is 2-connected. Let $X, Y \subseteq V(G)$ be disjoint with $|X|, |Y| \ge 2.$ Add a vertex $x'$ such that $x'$ has two neighbors in $X.$ By the Expansion Lemma, $G'$ is still 2-connected and thus (ii) holds for $G'.$ So there are two $x', Y$-paths $P'$ and $Q'$ such that $P'-x'$ is disjoint from $Q'-x'$ and thus $P = P' - x'$ and $Q = Q' - y'$ are two disjoint $X, Y$-paths.
>
> (iii) $\Rightarrow$ (i) Suppose for contradiction $\kappa(G) \le 1.$ If $\kappa(G) = 0,$ let $\{x, x', y, y'\}$ be chosen so that $x'$ is in a different component from $y$ and $y'.$ Now let $X = \{x, x'\}$ and $Y = \{y, y'\}.$ Using the property there are two completely disjoint $X, Y$-paths, there is a path from $x'$ to $y$ or $y',$ a contradiction. So suppose $\kappa(G) = 1$ and let $x$ be a cut vertex of $G.$ Let $x', y, y'$ be chosen so that $x'$ is in a different component of $G-x$ from $y$ and $y'.$ Now let $X = \{x, x'\}$ and $Y = \{y, y'\}.$ The property there are two completely disjoint $X, Y$-paths contradicts the fact that every path from $x'$ to $Y$ must contain the cut vertex $x.$ So $G$ is 2-connected. $\square$

---

> [!example] Exercise 24. Let $k$ and $n$ be integers with $1 \le k \le n-1.$ If $G$ is a graph on $n$ vertices with $\delta(G) \ge \frac{n+k-2}{2},$ then $\kappa(G) \ge k.$
>
> Furthermore, prove that for all $1 \le k \le n-1,$ there exists a graph $F$ on $n$ vertices with $\delta(G) = \lfloor \frac{n+k-3}{2} \rfloor$ such that $\kappa(G) < k.$

---

> [!example] Exercise 25. Let $G$ be a $k$-connected graph.
>
> (i) Prove that if $k \ge 2$ and $S \subseteq V(G)$ with $|S| = k,$ then $G$ has a cycle $C$ such that $S \subseteq V(C).$
>
> (Hint: Begin by letting $C$ be a cycle which contains as many vertices from $S$ as possible. If $C$ doesn't contain every vertex from $S,$ use the "Fan Lemma.")
>
> (ii) Prove that if $k \ge 1$ and $S \subseteq V(G)$ with $|S| = k+1,$ then $G$ has a path $P$ such that $S \subseteq V(P).$
>
> (Hint: When $k=1$ this is easy and when $k \ge 2,$ we can use part (i).)
>

> [!proof]
> **Proof of i.** Let $C$ be a cycle which contains as many vertices from $S$ as possible and suppose there exists some $x \in S \setminus V(C).$ Let $V(C)$ and let $F$ be a $x, V(C)$-fan containing $\min\{|V(C)|, k\}$-many paths. If $|V(C)| \le k-1,$ then we clearly have a cycle which contains $\{x\} \cup V(C),$ contradicting the maximality of $C.$ So suppose $|V(C)| \ge k.$ Let $P_1, \dots, P_k$ be the paths in $F$ and $x_1, \dots, x_k$ be the endpoints of $P_1, \dots, P_k$ in $V(C)$ cyclically ordered. For all $i \in [k],$ let $[x_i, x_{i+1})$ denote the vertices on the segment $x_i C x_{i+1} - x_{i+1}$ (if $i=k,$ then let $[x_k, x_{k+1})$ denote the vertices on the segment $v_k C v_1 - v_1).$ Since we are $|S \cap V(C)| < k$ and we have partitioned $V(C)$ into $k$ non-empty intervals, there exists some $i \in [k]$ such that $S \cap [x_i, x_{i+1}) = \emptyset.$ But now $x_i P_i x P_{i+1} x_{i+1} C x_i$ is a cycle which contains more vertices from $S$ than $C.$ $\square$
>
> **Proof of ii.** Let $S = \{v_1, \dots, v_k, v_{k+1}\}.$ By Theorem 4.2.24, there exists a cycle $C = u_1 u_2 \dots u_t$ containing $v_1, \dots, v_k.$ If $v_{k+1} \in V(C),$ then we are done; so suppose not. Let $Q$ be a shortest $v_{k+1}, V(C)$-path with endpoint $u_i.$ Now $P = v_{k+1} Q u_i u_{i+1} C u_{i-1}$ is a path such that $S \subseteq V(P).$ $\square$

---

> [!example] Exercise 26. _For all graphs $G$ and all $xy \in E(G),$ $\kappa(G) \ge \kappa(G-xy) \ge \kappa(G) - 1.$_
>
> **Lemma 4.2.20.** _For all graphs $G$ and all $xy \in E(G),$ $\kappa(G) \ge \kappa(G-xy) \ge \kappa(G)-1.$_
>

> [!proof]
> Let $xy \in E(G).$ If $S$ is a vertex cut of $G,$ then $S$ is a vertex cut of $G-xy.$ So $\kappa(G-xy) \le \kappa(G).$
>
> Let $G' = G-xy$ and let $S'$ be a minimum vertex cut of $G'$ (which exists since $G'$ cannot be complete).
>
> - If $x \in S'$ or $y \in S',$ then we have $G' - S' = G - S',$ and thus $S'$ is a vertex cut of $G$ which implies $\kappa(G') = |S'| \ge \kappa(G).$
>
> - So suppose $x, y \notin S'.$
>
>     - If $(G' - S') - x$ has more than one component, then $S' \cup \{x\}$ is a vertex cut of $G$ which implies $|S'| + 1 = |S' \cup \{x\}| \ge \kappa(G)$ and thus $\kappa(G') = |S'| \ge \kappa(G) - 1.$
>
>     - Likewise if $(G' - S') - y$ has more than one component.
>
> - So the only possibility is that $G' - S'$ has two components, each consisting of a single vertex. But then $\kappa(G') = |S'| = n-2 = n-1-1 \ge \kappa(G) - 1.$ $\square$
>

---

> [!example] Exercise 27.
>
> (i) Prove that every graph has a vertex ordering such that the greedy coloring algorithm uses $\chi(G)$ colors with respect to the ordering. Furthermore, there exists a graph $G$ and a vertex ordering of $G$ so that the greedy coloring algorithm uses more than $\chi(G)$ colors.
>
> (ii) Let $k$ be a positive integer and let $G$ be a graph with $\chi(G) = k.$ Prove that for every proper $k$-coloring of $G$ and every color $i \in [k],$ there a vertex of color $i$ which is adjacent to at least one vertex of every other color.

---

> [!example] Exercise 28.
>
> (i) Prove that if $G$ is a triangle-free graph (that is, a graph with $\omega(G) \le 2$), then the graph $G'$ obtained by applying Mycielski’s construction to $G$ is also triangle-free; in particular, $\omega(G') = 2.$
>
> (ii) Let $G$ be a graph. Prove that if $G'$ is the graph obtained by applying Mycielski’s construction to $G,$ then $\chi(G') \le \chi(G) + 1.$

---

> [!example] Exercise 29.
>
> (i) If $G$ is a graph with $m$ edges, then $\chi(G) < 1 + \sqrt{2m}.$ (Hint: Use Lemma Z)
>
> (ii) Let $G$ be a graph on $n$ vertices and let $k, \ell$ be positive integers such that $n \le k\ell.$ Prove that if $G$ is triangle-free (i.e. $\omega(G) \le 2$), then $\chi(G) \le k + \ell - 1.$
>
> (Hint 1: Induction on $\ell$)
>
> (Hint 2: What does being triangle-free tell us about the neighborhood of every vertex? In particular, what happens if $G$ has a vertex of degree at least $k$?)
>

> [!proof]
> (i) By Lemma Z we have $m \ge \binom{\chi(G)}{2} > \frac{(\chi(G)-1)^2}{2}$ and thus $\chi(G) < 1 + \sqrt{2m}.$
>
> (ii) First suppose $\ell = 1.$ We have $\chi(G) \le n \le k.$
>
> So let $\ell \ge 2,$ let $G$ be a graph with $n \le k\ell$ vertices, and suppose the result holds for triangle-free graphs with at most $k(\ell - 1)$ vertices.
>
> If $\Delta(G) \le k - 1,$ then $\chi(G) \le k \le k + \ell - 1$ as desired, so suppose $G$ contains a vertex of degree at least $k.$ Since $G$ is triangle-free, this gives us an independent set $A$ with at least $k$ vertices. Since $G - A$ is triangle-free and has at most $k\ell - k = k(\ell - 1)$ vertices, $\chi(G - A) \le k + (\ell - 1) - 1.$ Using a new color on $A$ gives us a $k + \ell - 1$ coloring of $G.$ $\square$
