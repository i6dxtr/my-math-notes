#example 
> [!example]
> ### Exercise 12 — BFST edge distance bound
> Let $G$ be a connected graph, let $x\in V(G)$, and let $T$ be a BFST of $G$ rooted at $x$. Then for every edge $uv\in E(G)$,
> $$\bigl|\,d_T(x,u)-d_T(x,v)\,\bigr|\le 1.$$
> [!proof]
> Since $uv\in E(G)$ we have $d_G(u,v)=1$, hence $\lvert d_G(x,u)-d_G(x,v)\rvert\le 1$.
> Because $T$ is a BFST rooted at $x$, we have $d_T(x,u)=d_G(x,u)$ and $d_T(x,v)=d_G(x,v)$. Therefore
> $$\lvert d_T(x,u)-d_T(x,v)\rvert=\lvert d_G(x,u)-d_G(x,v)\rvert\le 1.\quad\square$$
### Source
- lecture/438Notes_f25.pdf — Algorithm 2.3.8 and Theorem 2.3.8*; Exercise 12 (Sept 26/29, 2025)
- Notes by date/9-26-25.md, 9-28-25.md

### Relations
- BFST notion: [[definition - breadth-first search tree (BFST)]]
- BFS algorithm and distance preservation: [[algorithm - breadth-first search (BFS)]], [[theorem - BFS preserves distances (Theorem 2.3.8)]]
- Distances: [[distance, diameter]]
