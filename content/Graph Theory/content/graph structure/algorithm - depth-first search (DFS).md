#algorithm 
> [!remark]
> ### Algorithm — Depth-First Search (DFS) (Algorithm 4.1.21)
> Let $G$ be a connected graph. At the beginning all vertices are unexplored.
> 
> 1. Choose a start vertex $x\in V(G)$. Set $v_1=x$ and put $v_1$ at the beginning of the list of explored vertices.
> 2. Given a list of explored vertices $L=(v_1,v_2,\dots,v_k)$:
>    1. Let $v_i$ be the vertex with largest index such that $v_i$ has an unexplored neighbor in $G$.
>    2. Let $y$ be an unexplored neighbor of $v_i$.
>    3. Set $v_{k+1}=y$ and put $v_{k+1}$ at the end of the list of explored vertices.
>       - Record the edge $v_iv_{k+1}$ (this is the edge added to the DFS tree).
>    4. Repeat until every vertex in $L$ has all neighbors explored (i.e., in the list).
### Notes
- The recorded edges form a spanning tree when $G$ is connected (a DFS tree rooted at $x$).
- DFS explores along a branch as far as possible before backtracking, producing root-to-leaf “$x$-branches”.

### Source
- lecture/438Notes_f25.pdf — Algorithm 4.1.21 (Depth first search)
- Notes by date/9-28-25.md

### Relations
- Rooted DFS output: [[definition - depth-first search tree (DFST)]]
- Same-branch property: [[lemma - DFST edge endpoints on same branch (Lemma 4.1.22)]]
- Rooted trees and branches: [[definition - rooted tree and branch]]
- Connectivity: [[connectedness]]
- Paths and cycles: [[walk, trail, path, cycle]], [[path]]
- Trees: [[tree]]
