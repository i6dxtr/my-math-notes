#definition 
> [!definition]
> ### Definition — Depth-First Search Tree (DFST)
> Let $G$ be a connected graph and let $x\in V(G)$. A spanning tree $T$ of $G$ is a Depth‑First Search Tree (DFST) of $G$ rooted at $x$ if for all $uv\in E(G)$ with $u,v\in V(T)$, the vertices $u$ and $v$ lie on the same $x$-branch (i.e., there exists a path $P$ in $T$ from $x$ to a leaf such that $u,v\in V(P)$).
> [!remark]
> - A DFST can be produced by the DFS algorithm starting from $x$ (Algorithm 4.1.21).
> - The “same-branch” property characterizes DFS trees among spanning trees.
### Source
- lecture/438Notes_f25.pdf — Definition (DFST), Algorithm 4.1.21 and Lemma 4.1.22
- Notes by date/9-28-25.md

### Relations
- Construction procedure: [[content/graph structure/algorithm - depth-first search (DFS).md]]
- Same-branch property: [[content/theorems, lemma/lemma - DFST edge endpoints on same branch (Lemma 4.1.22).md]]
- Rooted trees and branch notion: [[content/graph structure/definition - rooted tree and branch.md]]
- Connectivity basics: [[content/graph structure/connectedness.md]]
- Trees and spanning trees: [[content/foundational/tree.md]]
