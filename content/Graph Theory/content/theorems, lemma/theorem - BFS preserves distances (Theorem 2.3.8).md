#theorem 
> [!theorem]
> ### Theorem — BFS preserves distances (Theorem 2.3.8)
> Given a connected graph $G$ and a vertex $x\in V(G)$, Algorithm 2.3.8 (BFS) produces a spanning tree $T$ such that for all $v\in V(G)$,
> $$d_G(x,v)=d_T(x,v).$$
> [!proof]
> - The process builds a spanning tree: if BFS terminated before all vertices were explored, $G$ would be disconnected. At each step we add a new vertex $v_{k+1}$ and one new edge $v_iv_{k+1}$, maintaining a tree.
> - Base case $(d=0)$: If $d_G(x,v)=0$, then $v=x$ so $d_T(x,v)=0$.
> - Inductive step: Let $d\ge 1$ and suppose for every $u$ with $d_G(x,u)\le d-1$ we have $d_T(x,u)=d_G(x,u)$. Now take $v$ with $d_G(x,v)=d$. Then $v$ has a neighbor $u$ with $d_G(x,u)=d-1$. By the inductive hypothesis $d_T(x,u)=d-1$ and BFS will discover $v$ from some such $u$, adding edge $uv$ so $d_T(x,v)=d$.
### Source
- lecture/438Notes_f25.pdf — Theorem 2.3.8*
- Notes by date/9-26-25.md

### Relations
- Algorithmic construction: [[content/graph structure/algorithm - breadth-first search (BFS).md]]
- BFST definition: [[content/graph structure/definition - breadth-first search tree (BFST).md]]
- Distance notions: [[content/foundational/distance, diameter.md]]
- Paths and trees: [[content/graph structure/path.md]], [[content/foundational/tree.md]]
