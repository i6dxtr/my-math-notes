#lemma 
> [!theorem]
> ### Lemma — DFST edge endpoints lie on the same branch (Lemma 4.1.22)
> Given a connected graph $G$ and a root $x\in V(G)$, the DFS algorithm (Algorithm 4.1.21) produces a spanning tree $T$ rooted at $x$ such that for every $uv\in E(G)$ with $u,v\in V(T)$, the vertices $u$ and $v$ lie on the same $x$-branch of $T$ (i.e., there exists a path $P$ in $T$ from $x$ to a leaf with $u,v\in V(P)$).
> ![[Pasted image 20250929134924.png|300]]
> [!proof]
> Let $T$ be the spanning tree created by DFS. Without loss of generality, suppose the algorithm first discovers $u$ (before $v$). At that moment there is a path in $T$ from $x$ to $u$ which does not contain $v$.
> 
> The DFS rule always continues from the most recently discovered vertex that still has an unexplored neighbor. Thus, the search will exhaustively explore along the branch containing $u$ before backtracking to any ancestor of $u$. Since $uv\in E(G)$, the moment the search backtracks to $u$ (or an ancestor on the path $x\to u$) with $v$ still unexplored, $v$ will be discovered from that branch and added as a descendant along the same $x$-branch. Therefore the path in $T$ from $x$ to $v$ contains $u$, and $u$ and $v$ lie on the same $x$-branch.
### Relations
- DFS procedure and tree: [[content/graph structure/algorithm - depth-first search (DFS).md]], [[content/graph structure/definition - depth-first search tree (DFST).md]]
- Rooted tree and branch notion: [[content/graph structure/definition - rooted tree and branch.md]]
- Basic path/walk notions: [[content/graph structure/walk, trail, path, cycle.md]], [[content/graph structure/path.md]]
- BFS contrast (distance layering): [[content/graph structure/algorithm - breadth-first search (BFS).md]], [[content/graph structure/definition - breadth-first search tree (BFST).md]], [[content/theorems, lemma/theorem - BFS preserves distances (Theorem 2.3.8).md]]
