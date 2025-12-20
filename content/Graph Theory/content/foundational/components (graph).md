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
- Formally characterized by [[content/theorems, lemma/lemma - connectivity equivalence relation.md|lemma - connectivity equivalence relation]].
- Removing vertices/edges (see [[content/graph structure/vertex & edge deletion.md|vertex & edge deletion]]) can increase the number of components.
- Useful when reasoning about distances, diameter, and when applying structural theorems component‑wise.
- Components and their parity (odd/even order) play a key role in matching theory and Tutte's condition; see [[odd components]] and [[Tutte's theorem]].
- Components are also important when analyzing edge-connectivity and cut-edges/cut-vertices ([[content/graph structure/cut-vertex, cut-edge.md|cut-vertex, cut-edge]], [[content/foundational/disconnecting set, edge-connectivity.md|disconnecting set, edge-connectivity]]).
