#definition 
> [!definition]
> Given a graph $G = (V, E)$ and vertices $u, v \in V$, we say:
> - $v$ is a **neighbor** of $u$ if $\{u, v\} \in E(G)$.
> - The *neighborhood* of $u$, denoted $N(u)$, is the set $\{ v : \{u, v\} \in E(G) \}$.
> - $u$ and $v$ are **adjacent** if $\{u, v\} \in E(G)$.
> 
> Given an edge $e \in E(G)$ and a vertex $v \in V(G)$, $e$ and $v$ are **incident** if $v \in e$.

#### Relations
- The concepts of neighbor, adjacency, and incidence are fundamental to understanding graph connectivity and structure — see [[degree]] for the formal relation between neighborhoods and degrees, and [[order, size]] for how vertex/edge counts interact with local structure.
- Neighborhoods are used in defining paths, walks, and connectivity; see [[path]], [[walk, trail, path, cycle]], and [[connectedness]] for related constructions and properties.
- These definitions connect directly to theorems about walks and paths (see [[lemma - walk contains path]]), and to counting relations such as the [[handshake lemma]].
- For local/subgraph perspectives, also see [[(induced) subgraphs]] and [[graph complement]].
- Neighborhood and adjacency concepts later support algorithmic structures and search trees (BFS/DFS): [[algorithm - breadth-first search (BFS)]], [[definition - breadth-first search tree (BFST)]], [[algorithm - depth-first search (DFS)]], [[definition - depth-first search tree (DFST)]].
- They also underpin matching notions where alternating/augmenting paths traverse neighborhoods ([[M-alternating path, M-augmenting path]], [[matching]], [[maximal matching, maximum matching]]).
