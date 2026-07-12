#theorem
> [!theorem]
> ### Theorem — Minimum degree implies long paths and cycles
> Let $k\ge 1$ and let $G$ be a (simple) graph.
> 
> 1. If $\delta(G)\ge k$ then every maximal path of $G$ has length at least $k$ (equivalently, every maximal path has order at least $k+1$).
> 
> 2. If $k\ge 2$ and $\delta(G)\ge k$ then $G$ contains a cycle of length at least $k+1$.

> [!proof]
> (1) Let $P=v_{1}v_{2}\dots v_{t}$ be a maximal path in $G$. Because $P$ is maximal, every neighbour of $v_{1}$ is a vertex of $P$. Since $d(v_{1})\ge k$, the vertex $v_{1}$ has at least $k$ distinct neighbours on $P$. Those neighbours can only occupy positions $v_2,\dots,v_t$, so at least one neighbour must be $v_i$ with $i\ge k+1$, otherwise $v_1$ would have at most $k-1$ neighbours on $P$. Hence $t\ge k+1$ and the length of $P$ is at least $k$.
> 
> (2) Let $P=v_{1}\dots v_{t}$ be a maximal path. By part (1) we have $t\ge k+1$. If some neighbour of $v_1$ is $v_i$ with $i\ge 3$, then $v_1v_2\cdots v_i v_1$ is a cycle of length $i\ge k+1$ and we are done. If no such neighbour exists for $v_1$, then all neighbours of $v_1$ are among $\{v_2\}$, contradicting $d(v_1)\ge k\ge 2$ unless $t\ge k+1$ and some other endpoint (say $v_t$) provides the required connection; examining both ends of a maximal path shows at least one endpoint must have a neighbour inside the path far enough to create a cycle of length at least $k+1$. Formally, since $d(v_1)\ge k\ge2$, $v_1$ has a neighbour $v_i$ with $i\ge3$ unless $v_1$ is adjacent only to $v_2$; similarly $v_t$ has a neighbour $v_j$ with $j\le t-2$ unless adjacent only to $v_{t-1}$. If both endpoints were adjacent only to their immediate neighbour, then $d(v_1)=d(v_t)=1$, contradicting $\delta(G)\ge k\ge2$. Therefore a chord exists producing a cycle of length at least $k+1$.
### Relations
- Strengthens maximal-path arguments in [[path|path]] and complements [[proposition - maximal paths & cycles|proposition - maximal paths & cycles]].
- Often used as a building block toward Hamiltonicity and long-cycle results (see Dirac-style remarks and later Hamiltonicity notes).
- Connects degree bounds ($\delta(G)$) to guaranteed substructure (long paths/cycles).
- These minimum-degree ideas are used in tree and spanning-tree exercises and interact with BFS/DFT constructions when reasoning about long paths and distances ([[tree|tree]], [[algorithm - breadth-first search (BFS)|BFS]], [[algorithm - depth-first search (DFS)|DFS]]).
- Minimum-degree and long-path arguments also inform matching and Tutte-style existence results introduced later in the course ([[matching|matching]], [[theorem - Tutte's theorem|Tutte's theorem]], [[theorem - matching + edge cover = n|theorem - matching + edge cover = n]]).
- Useful when comparing degree-based sufficient conditions across topics (connectivity, Hamiltonicity, and cycle decompositions).
