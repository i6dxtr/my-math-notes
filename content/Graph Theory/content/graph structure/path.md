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
- Fundamental to definitions of [[content/graph structure/walk, trail, path, cycle.md|walk, trail, path, cycle]] and to [[content/graph structure/connectedness.md|connectedness]].
- [[content/theorems, lemma/lemma - walk contains path.md|Lemma 1.2.5]] ensures that every walk contains a path.
- Cycles are central to structural theorems such as [[content/theorems, lemma/theorem - edge is cut iff no cycle.md|theorem - edge is cut iff no cycle]] and the characterization of bipartite graphs ([[content/theorems, lemma/theorem - bipartite characterization.md|theorem - bipartite characterization]]).
- Maximal paths are used in extremal arguments (see [[content/theorems, lemma/proposition - maximal paths & cycles.md|proposition - maximal paths & cycles]]).
- Paths and cycles underpin search algorithm behavior and tree constructions: [[content/graph structure/algorithm - breadth-first search (BFS).md|algorithm - breadth-first search (BFS)]], [[content/graph structure/definition - breadth-first search tree (BFST).md|definition - breadth-first search tree (BFST)]], [[content/graph structure/algorithm - depth-first search (DFS).md|algorithm - depth-first search (DFS)]], [[content/graph structure/definition - depth-first search tree (DFST).md|definition - depth-first search tree (DFST)]].
- Paths are used extensively in matching theory (alternating/augmenting paths lead to maximum matching proofs) and Tutte/Hall applications: [[content/foundational/M-alternating path, M-augmenting path.md|M-alternating path, M-augmenting path]], [[content/theorems, lemma/theorem - Tutte's theorem.md|Tutte's theorem]], [[content/theorems, lemma/theorem - Hall's theorem (Theorem 3.1.11).md|Hall's theorem (Theorem 3.1.11)]].
