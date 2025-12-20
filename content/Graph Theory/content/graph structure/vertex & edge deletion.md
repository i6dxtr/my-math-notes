#graph-structure
> [!definition]
> ### Definition: Vertex and Edge Deletion
> Let $G = (V, E)$ be a [[graph]]:
> - For $v \in V$, the graph **$G - v$** is obtained by removing $v$ and all edges incident to $v$. Formally, $G-v = (V\setminus\{v\},\; \{e\in E: v\notin e\})$.
> - For $e \in E$, the graph **$G - e$** is obtained by removing the edge $e$ but keeping all vertices: $G-e=(V,\;E\setminus\{e\})$.
> [!remark]
> Deleting vertices or edges is a fundamental operation for defining cut-vertices and cut-edges, and for constructing induced subgraphs.
### Relations
- Directly used to define [[cut-vertex, cut-edge|cut-vertex, cut-edge]].
- Operations often appear in inductive proofs and constructive arguments (e.g., removing edges to simplify components).
- Removing a vertex yields an induced subgraph; removing an edge yields a (not necessarily induced) subgraph.
- Vertex/edge deletion is a core operation in Tutte and matching arguments (deleting vertices to count odd components), and in connectivity/edge-connectivity results: see [[odd components|odd components]], [[theorem - Tutte's theorem|Tutte's theorem]], [[disconnecting set, edge-connectivity|disconnecting set, edge-connectivity]].
