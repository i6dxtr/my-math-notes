> [!theorem]
> ### Lemma — DFST edge endpoints lie on the same branch (Lemma 4.1.22)
> Given a connected graph $G$ and a root $x\in V(G)$, the DFS algorithm (Algorithm 4.1.21) produces a spanning tree $T$ rooted at $x$ such that for every $uv\in E(G)$ with $u,v\in V(T)$, the vertices $u$ and $v$ lie on the same $x$-branch of $T$ (i.e., there exists a path $P$ in $T$ from $x$ to a leaf with $u,v\in V(P)$).
> ![[Pasted image 20250929134924.png|300]]

> [!proof]
> Let $T$ be the spanning tree created by DFS. Without loss of generality, suppose the algorithm first discovers $u$ (before $v$). At that moment there is a path in $T$ from $x$ to $u$ which does not contain $v$.
> 
> The DFS rule always continues from the most recently discovered vertex that still has an unexplored neighbor. Thus, the search will exhaustively explore along the branch containing $u$ before backtracking to any ancestor of $u$. Since $uv\in E(G)$, the moment the search backtracks to $u$ (or an ancestor on the path $x\to u$) with $v$ still unexplored, $v$ will be discovered from that branch and added as a descendant along the same $x$-branch. Therefore the path in $T$ from $x$ to $v$ contains $u$, and $u$ and $v$ lie on the same $x$-branch.
### Relations
- DFS procedure and tree: [[algorithm - depth-first search (DFS)]], [[definition - depth-first search tree (DFST)]]
- Rooted tree and branch notion: [[definition - rooted tree and branch]]
- Basic path/walk notions: [[walk, trail, path, cycle]], [[path]]
- BFS contrast (distance layering): [[algorithm - breadth-first search (BFS)]], [[definition - breadth-first search tree (BFST)]], [[theorem - BFS preserves distances (Theorem 2.3.8)]]
