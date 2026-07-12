#definition 
> [!definition]
> ### Definition — Breadth-First Search Tree (BFST)
> Let $G$ be a connected graph and let $x\in V(G)$. A spanning tree $T$ of $G$ is a Breadth-First Search Tree (BFST) of $G$ rooted at $x$ if for all $v\in V(G)$,
> $$d_G(x,v)=d_T(x,v).$$

> [!remark]
> - A BFST is produced by the BFS algorithm starting from $x$.
> - In a BFST, vertices are discovered in nondecreasing order of their distance from $x$.
### Source
- lecture/438Notes_f25.pdf — Definition (BFST), Algorithm 2.3.8 and Theorem 2.3.8*
- Notes by date/9-26-25.md

### Relations
- Construction procedure: [[algorithm - breadth-first search (BFS)]]
- Distance preservation statement: [[theorem - BFS preserves distances (Theorem 2.3.8*)]]
- Distances and metrics on graphs: [[distance, diameter]]
- Trees and spanning trees: [[tree]]
- Connectivity basics: [[connectedness]]
