#definition 
> [!definition]
> A **graph** is a pair $ (V, E) $ where $E \subseteq \binom{V}{2}$, the set of 2-element subsets of $V$:
> ![[Pasted image 20250825140803.png]]

> [!remark]
> *Note that $E$ is a symmetric anti-reflexive relation on $V$.*

> [!definition]
> Given a [[graph]] $G = (V, E)$ and a vertex $v \in V$, the **degree** of $v$ is
> $$
> d(v) = \lvert \{ u \in V : \{u, v\} \in E \} \rvert.
> $$

> [!definition]
> Given a graph $G = (V, E)$ and vertices $u, v \in V$:
> - $v$ is a **neighbor** of $u$ if $\{u, v\} \in E(G)$.
> - The *neighborhood* of $u$, denoted $N(u)$, is the set $\{ v : \{u, v\} \in E(G) \}$.
> - $u$ and $v$ are **adjacent** if $\{u, v\} \in E(G)$.
> 
> Given an edge $e \in E(G)$ and a vertex $v \in V(G)$, $e$ and $v$ are **incident** if $v \in e$.
> 
> The **degree** of a vertex $v \in V(G)$ (denoted $d(v)$) is $\lvert N(v) \rvert = \lvert \{ e \in E(G) : v \in e \} \rvert$.
> 
> The **minimum degree** of $G$ (denoted $\delta(G)$) is $\min \{ d(v) : v \in V(G) \}$ and the **maximum degree** of $G$ (denoted $\Delta(G)$) is $\max \{ d(v) : v \in V(G) \}$.

> [!theorem]
> #### Handshake Lemma
> Given any graph $G = (V, E)$,
> $$
> \sum_{v \in V} d(v) = 2 \lvert E(G) \rvert.
> $$

> [!corollary]
> In every graph, the number of vertices with an odd degree is even.
#### Relations
- Degree, adjacency, and incidence are core definitions used throughout the notes; see [[neighbor, adjacent]], [[degree]], and [[handshake lemma]].
- Degree parameters $\delta(G),\Delta(G)$ appear in existence and structure theorems (e.g. [[theorem - dirac (hamiltonian)]], [[theorem - minimum degree & path-cycle length]]).
- Adjacency and neighborhoods underpin paths, walks, cycles, and connectivity; see [[path]], [[walk, trail, path, cycle]], and [[connectedness]].
- These notions connect to order and size ([[order, size]]), components ([[components (graph)]]), and subgraph/complement perspectives ([[(induced) subgraphs]], [[graph complement]]).
- Foundational graph notions also support algorithmic and structural topics introduced later in the course: search trees and distance results ([[algorithm - breadth-first search (BFS)]], [[definition - breadth-first search tree (BFST)]], [[algorithm - depth-first search (DFS)]], [[definition - depth-first search tree (DFST)]]), trees and spanning trees ([[tree]]), and connectivity concepts ([[separating set, connectivity]], [[disconnecting set, edge-connectivity]]).
- Further relations to matching and covering theory (matchings, augmenting paths, Tutte's theorem, edge covers): [[matching]], [[maximal matching, maximum matching]], [[M-alternating path, M-augmenting path]], [[odd components]], [[Tutte's theorem]], [[edge cover]], [[theorem - matching + edge cover = n]].
- Advanced connectivity/structure theorems and their corollaries also build on basic graph concepts: 2‑connectivity and Menger‑type results ([[theorem - equivalent conditions for 2-connected graphs]], [[theorem - 2-connected via internally disjoint paths]]), Hamiltonicity criteria (Chvátal–Erdős sketch, Dirac remarks), and decompositions into cycles ([[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)]]).
