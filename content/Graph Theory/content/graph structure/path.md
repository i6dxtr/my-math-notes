#graph-structure
> [!definition]
> ### Definition: Path
> A **path** of length $k-1$ is a sequence of distinct vertices
> $$v_{1}, v_{2}, \dots, v_{k}$$
> such that each $v_{i}v_{i+1} \in E(G)$ for $i = 1, \dots, k-1.$
> The path may be denoted $v_{1}v_{2}\dots v_{k}$ and has order $k$ and length $k-1$.
> [!definition]
> ### Definition: Cycle
> If $k \ge 3$, a **cycle** of length $k$ is a closed walk
> $$v_{1}v_{2}\cdots v_{k}v_{1}$$
> with all $v_{i}$ distinct except $v_{1} = v_{k}$. We may denote the cycle by $C_k$ when its length is $k$.
> [!example]
> ![[Pasted image 20250827134534.png|400]]
> ![[Pasted image 20250827134551.png|400]]
### Relations
- Fundamental to definitions of [[walk, trail, path, cycle|walk, trail, path, cycle]] and to [[connectedness|connectedness]].
- [[lemma - walk contains path|Lemma 1.2.5]] ensures that every walk contains a path.
- Cycles are central to structural theorems such as [[theorem - edge is cut iff no cycle|theorem - edge is cut iff no cycle]] and the characterization of bipartite graphs ([[theorem - bipartite characterization|theorem - bipartite characterization]]).
- Maximal paths are used in extremal arguments (see [[proposition - maximal paths & cycles|proposition - maximal paths & cycles]]).
- Paths and cycles underpin search algorithm behavior and tree constructions: [[algorithm - breadth-first search (BFS)|algorithm - breadth-first search (BFS)]], [[definition - breadth-first search tree (BFST)|definition - breadth-first search tree (BFST)]], [[algorithm - depth-first search (DFS)|algorithm - depth-first search (DFS)]], [[definition - depth-first search tree (DFST)|definition - depth-first search tree (DFST)]].
- Paths are used extensively in matching theory (alternating/augmenting paths lead to maximum matching proofs) and Tutte/Hall applications: [[M-alternating path, M-augmenting path|M-alternating path, M-augmenting path]], [[theorem - Tutte's theorem|Tutte's theorem]], [[theorem - Hall's theorem (Theorem 3.1.11)|Hall's theorem (Theorem 3.1.11)]].
