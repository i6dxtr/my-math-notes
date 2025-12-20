#theorem

> [!theorem]
> ### Proposition — Maximal paths & cycles (Parts i & ii)
> Let $G$ be a graph and let $P$ be a maximal path in $G$ with vertex sequence $v_1v_2\cdots v_\ell$.
> 1. If $|V(P)|=\ell \le 2\delta(G)$ then the subgraph $G[V(P)]$ contains a cycle on $\ell$ vertices.
> 2. For integers $1\le k\le\frac{n-1}{2}$, if $G$ is connected on $n$ vertices and $\delta(G)\ge k$ then $G$ has a path on at least $2k+1$ vertices.
> [!proof]
> **(Part i)** Let $P=v_1v_2\cdots v_\ell$ be maximal and suppose $\ell\le 2\delta(G)$. Define
> $$S=\{v_{i-1} : v_i\in N(v_1)\}\quad\text{and}\quad T=N(v_\ell).$$
> Since $P$ is maximal every neighbor of $v_1$ and every neighbor of $v_\ell$ lies on $P$. Hence $S\cup T\subseteq\{v_1,\dots,v_{\ell-1}\}$. Compute $$\begin{align} |S\cap T|&=|S|+|T|-|S\cup T|\\ &\ge \delta(G)+\delta(G)-(\ell-1)\\ &\ge 2\delta(G)-(2\delta(G)-1)\\ &=1. \end{align}$$
> Thus $S\cap T\neq\varnothing$; pick $v_i\in S\cap T$. Then $v_1\cdots v_iv_\ell v_{\ell-1}\cdots v_{i+1}v_1$ is a cycle of length $\ell$ contained in $G[V(P)]$.
> 
> **(Part ii)** Let $P$ be a maximal path in $G$. If $|V(P)|\ge 2k+1$ we are done. Otherwise $|V(P)|\le 2k$, and by part (i) the induced subgraph $G[V(P)]$ contains a cycle of length $|V(P)|$. Since $n\ge 2k+1>|V(P)|$ there exists a vertex $w\notin V(P)$. As $G$ is connected there is a path from $w$ to the cycle; choose such a path $Q$ that meets the cycle in exactly one vertex. Splicing $Q$ into the cycle yields a path strictly longer than $P$, contradicting maximality. Hence $G$ must have a path on at least $2k+1$ vertices.
### Relations
- Builds on maximal-path arguments in [[content/graph structure/path.md|path]].
- Used to derive long‑path and Hamiltonicity type consequences in conjunction with degree bounds ([[content/theorems, lemma/theorem - minimum degree & path-cycle length.md|minimum degree → long paths/cycles]]).
- Technique is useful when converting local degree constraints into global structural guarantees.
