> [!theorem]
> ### Theorem M (Menger’s theorem — local sets version, Pym 1969)
> For every graph $G$ and all $X,Y\subseteq V(G)$, we have
> $$\lambda(X,Y)=\kappa(X,Y),$$
> i.e. the maximum number of pairwise vertex-disjoint $X,Y$-paths equals the minimum size of an $X,Y$-barrier.
> [!remark]
> We always have $\lambda(X,Y)\le\kappa(X,Y)$ by definition; the theorem is the nontrivial reverse inequality $\lambda(X,Y)\ge\kappa(X,Y)$.
> [!proof]
> The proof proceeds by induction on the number of vertices (and edges) of $G$.
> 
> Base cases: the claim is trivial for graphs with at most two vertices by direct checking. Now assume the claim holds for all graphs with fewer vertices or fewer edges.
> 
> Let $k:=\kappa(X,Y)\ge 1$ (otherwise the claim is immediate). Consider two cases:
> 
> Case 1: There exists an $X,Y$-barrier $Z$ of size $k$ with $X\not\subseteq Z$ and $Y\not\subseteq Z$.
> Then every $X,Z$-barrier and every $Y,Z$-barrier is an $X,Y$-barrier, so $\kappa(X,Z)\ge k$ and $\kappa(Y,Z)\ge k$. Let $G_1$ be the subgraph induced by all vertices appearing on some $X,Z$-path and let $G_2$ be the subgraph induced by vertices appearing on some $Y,Z$-path. Both $G_1$ and $G_2$ have fewer vertices than $G$, so by induction there are $k$ vertex-disjoint $X,Z$-paths and $k$ vertex-disjoint $Y,Z$-paths; concatenating appropriately yields $k$ vertex-disjoint $X,Y$-paths in $G$.
> 
> Case 2: Every minimum $X,Y$-barrier is equal to $X$ or $Y$. Without loss of generality suppose $X$ is a minimum barrier of size $k$. If $X\subseteq Y$ then the claim is trivial, so assume not and pick $x\in X\setminus Y$. Since $X\setminus\{x\}$ has size at most $k-1$, there exists an $x$-$Y$ path in $G-(X\setminus\{x\})$. Let $w$ be the first vertex after $x$ on such a path that lies outside $X$; consider the graph $G'$ obtained by deleting the edge $xw$. Let $Z'$ be a smallest $X,Y$-barrier in $G'$. If $|Z'|\ge k$ then by induction $G'$ has $k$ vertex-disjoint $X,Y$-paths and we are done. Otherwise $|Z'|\le k-1$ and any $X,Y$-path in $G-Z'$ must use the edge $xw$. Then $Z'\cup\{x\}$ and $Z'\cup\{w\}$ are $X,Y$-barriers in $G$; by hypothesis these equal $X$ and $Y$ respectively. From this one constructs $k$ vertex-disjoint $X,Y$-paths in $G$ (namely $k-1$ trivial paths from $X\cap Y$ and the single-edge path $xw$).
> 
> This completes the induction and proves the theorem.
Relations
- Definition: [[content/foundational/X,Y-barrier.md]].
- See [[content/foundational/X,Y-paths and fans.md]] and [[content/theorems, lemma/theorem - Menger / Menger-type equivalences.md]] for equivalent formulations and corollaries.
- Application: [[content/theorems, lemma/theorem - König–Egerváry (1931).md]] (use Menger in bipartite setting to relate matchings and vertex covers).
