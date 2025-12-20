#foundational
> [!definition]
> ### Definition: Components
> A **component** in a [[graph]] $G$ is a maximally connected induced subgraph of $G$.
> That is, a subgraph $C$ of $G$ is a component if
> - $C$ is connected, and
> - no proper induced supergraph of $C$ in $G$ is connected.

> [!remark]
> Intuitively, components are the “pieces” of a graph that remain when the graph is disconnected. Every vertex of $G$ lies in exactly one component.

### Relations
- Components are built on the notion of [[connectedness]].
- Formally characterized by [[lemma - connectivity equivalence relation|lemma - connectivity equivalence relation]].
- Removing vertices/edges (see [[vertex & edge deletion|vertex & edge deletion]]) can increase the number of components.
- Useful when reasoning about distances, diameter, and when applying structural theorems component‑wise.
- Components and their parity (odd/even order) play a key role in matching theory and Tutte's condition; see [[odd components]] and [[Tutte's theorem]].
- Components are also important when analyzing edge-connectivity and cut-edges/cut-vertices ([[cut-vertex, cut-edge|cut-vertex, cut-edge]], [[disconnecting set, edge-connectivity|disconnecting set, edge-connectivity]]).
