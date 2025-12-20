#algorithm 
> [!remark]
> ### Algorithm — Breadth-First Search (BFS) (Algorithm 2.3.8)
> Let $G$ be a connected graph. At the beginning all vertices are unexplored.
> 
> 1. Choose a start vertex $x\in V(G)$. Set $v_1=x$ and put $v_1$ at the beginning of the list of explored vertices.
> 2. Given a list of explored vertices $L=(v_1,v_2,\dots,v_k)$:
>    1. Let $v_i$ be the vertex with smallest index such that $v_i$ has an unexplored neighbor in $G$.
>    2. Let $y$ be an unexplored neighbor of $v_i$.
>    3. Set $v_{k+1}=y$ and put $v_{k+1}$ at the end of the list of explored vertices.
>       - Record the edge $v_iv_{k+1}$ (this is the edge added to the BFS tree).
>    4. Repeat until every vertex in $L$ has all neighbors explored (i.e., in the list).
### Notes
- The set of recorded edges forms a spanning tree when $G$ is connected (the BFS tree rooted at $x$).
- BFS discovers vertices in nondecreasing order of distance from $x$.

### Source
- lecture/438Notes_f25.pdf — Algorithm 2.3.8 (Breadth first search)
- Notes by date/9-26-25.md

### Relations
- Rooted BFS output: [[definition - breadth-first search tree (BFST)]]
- Distance preservation: [[theorem - BFS preserves distances (Theorem 2.3.8*)]]
- Distance notions: [[distance, diameter]]
- Connectivity: [[connectedness]]
- Paths and cycles: [[walk, trail, path, cycle]], [[path]]
- Trees: [[tree]]
