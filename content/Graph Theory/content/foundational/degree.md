#definition
> [!definition]
> Given a [[graph]] $G = (V, E)$ and a vertex $v \in V(G)$,
> $$
> d(v) = \lvert \{ u \in V(G) : \{u, v\} \in E \} \rvert
> $$
> is called the **degree** of $v$.
> 
> #### Incidence
> Given an edge $e \in E(G)$ and a vertex $v \in V(G)$, we say $e$ and $v$ are **incident** if $v \in e$.
> 
> 
> #### Minimum/Maximum Degree
> The **degree** of a vertex $v \in V(G)$ (denoted $d(v)$) is also equal to the size of its neighborhood:
> $$
> d(v) = \lvert N(v) \rvert = \lvert \{ e \in E(G) : v \in e \} \rvert.
> $$
> 
> The **minimum degree** of $G$ (denoted $\delta(G)$) is
> $$
> \delta(G) = \min \{ d(v) : v \in V(G) \}
> $$
> and the **maximum degree** of $G$ (denoted $\Delta(G)$) is
> $$
> \Delta(G) = \max \{ d(v) : v \in V(G) \}.
> $$

> [!remark]
> #### Relations
> - The minimum and maximum degree parameters ($\delta(G)$ and $\Delta(G)$) are used in many theorems about graph connectivity and structure — see [[theorem - dirac]] and [[theorem - minimum degree & path-cycle length]] for illustrative results.
> - These concepts relate to the degree definition and connect to properties of paths, cycles, and connectivity (see [[walk, trail, path, cycle]] and [[connectedness]]).
> - They also link to order and size of a graph and to extremal properties (see [[order, size]] and [[handshake lemma]]).

> [!remark]
> When $G$ is finite, degrees are non-negative integers. In multigraphs the degree counts incident edges with multiplicity; in directed graphs one distinguishes in‑degree and out‑degree.
### Examples
- In a complete graph $K_n$, every vertex has degree $n-1$.
- In a tree on $n$ vertices the degree sequence sums to $2(n-1)$ by the Handshake Lemma.
### Relations
- The Handshake Lemma: see [[handshake lemma]].
- Degree parameters $\delta(G),\Delta(G)$ appear in existence and structure theorems (e.g., Dirac-type results; see [[theorem - minimum degree & path-cycle length]]).
- Degree and neighborhood concepts connect to [[walk, trail, path, cycle]] (paths and walks), [[order, size]] (graph size), and [[components (graph)]] (connectivity).
- Algorithmic note: many graph algorithms (BFS, DFS, matching, centrality measures) rely on iterating over neighborhoods and degrees.
- Later topics that build on degree-related concepts include cycle decompositions and Eulerian characterizations ([[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)]], [[theorem - eulerian circuit condition]]), Hamiltonicity remarks and Dirac-style theorems ([[theorem - dirac (hamiltonian)]], [[theorem - minimum degree & path-cycle length]]), and connectivity/edge-connectivity bounds ([[separating set, connectivity]], [[disconnecting set, edge-connectivity]]).
