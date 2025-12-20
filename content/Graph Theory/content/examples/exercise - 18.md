> [!example]
> ### Exercise 18. Let $G$ be an $X, Y$-bipartite graph and let $d = \max\{|S| - |N(S)| : S \subseteq X\}.$
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
> 
> 
> Relations
> - [[content/theorems, lemma/theorem - Hall's theorem (Theorem 3.1.11).md]]
> - [[content/examples/exercise - 18.md]]
> - [[content/foundational/matching.md]]