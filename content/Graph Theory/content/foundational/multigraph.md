#definition 
> [!definition]
> ### Definition — Multigraph (non-simple graph)
> A multigraph is an ordered pair $G=(V,E)$ where $V$ is a finite vertex set and $E$ is a multiset of unordered pairs of vertices (allowing multiple edges between the same pair of vertices). Loops may be permitted or forbidden depending on context; when loops are allowed an edge of the form $\{v,v\}$ is called a loop.

> [!remark]
> - When $E$ is a set (no multiplicities) and loops are forbidden, a multigraph is a simple graph; most files in this vault treat "graph" to mean a finite simple graph unless otherwise noted.
> - Degree in a multigraph counts incident edges with multiplicity; loops contribute $2$ to the degree of their incident vertex if loops are allowed and counted in the degree convention.

> [!proof]
> This file records the standard notion of a multigraph used in lectures. No proof required.

### Relations
- Compare with simple graphs: [[graph]].
- Degree conventions and parity: [[degree]], [[handshake lemma]].
- For exercises that mention multigraphs explicitly: see [[exercise - 3 closed odd walk]].
