#graph-structure
> [!definition]
> ### Definition: Cut-vertex
> A vertex $v \in V(G)$ is a **cut-vertex** if the number of [[content/foundational/components (graph).md|components]] in $G - v$ is strictly greater than the number of components in $G$.
> [!definition]
> ### Definition: Cut-edge
> An edge $e \in E(G)$ is a **cut-edge** (or bridge) if the number of components in $G - e$ is strictly greater than the number of components in $G$.
> [!remark]
> Cut-vertices and cut-edges identify points of vulnerability in a graph's connectivity. In connected graphs, a cut-vertex or cut-edge increases the number of connected components when removed.
### Relations
- Characterized by [[content/theorems, lemma/theorem - edge is cut iff no cycle.md|theorem - edge is cut iff no cycle]] for cut‑edges.
- Defined using [[content/graph structure/vertex & edge deletion.md|vertex & edge deletion]].
- Related to block structure and articulation points in network analysis.
- Removing a cut-vertex splits the graph into two or more components; these components are used in recursive algorithms and decomposition proofs.
- Cut-edges and cut-vertices are relevant for matching and Petersen corollaries (graphs with no cut-edge may have perfect matchings under degree conditions); see [[content/theorems, lemma/corollary - Petersen 3-regular perfect matching (3.3.8).md|Petersen 3-regular perfect matching (3.3.8)]].
- Also connected to edge-connectivity and Whitney's inequalities ([[content/foundational/disconnecting set, edge-connectivity.md|disconnecting set, edge-connectivity]], [[content/foundational/separating set, connectivity.md|separating set, connectivity]]).
