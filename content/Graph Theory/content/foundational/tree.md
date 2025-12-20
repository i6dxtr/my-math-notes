#definition
> [!definition]
> ### Definition — Tree, Forest, Leaf, Spanning Tree
> Let $G=(V,E)$ be a graph.
> 
> - $G$ is **acyclic** if $G$ contains no cycles.
> - A **forest** is an acyclic graph.
> - A **tree** is a connected acyclic graph.
> - A **leaf** is a vertex of degree $1$.
> - A **spanning subgraph** of $G$ is a subgraph with vertex set $V(G)$.
> - A **spanning tree** of $G$ is a spanning subgraph of $G$ which is a tree.

> [!example]
> ![[Pasted image 20250920195850.png]]*A tree, ie. an acyclic graph.*

> [!remark]
> Every tree is bipartite and every forest is a disjoint union of trees (components). Many standard characterizations of trees are equivalent (for a finite graph $T$ with $n$ vertices):
> - $T$ is connected and acyclic.
> - $T$ is acyclic and has $n-1$ edges.
> - $T$ is connected and has $n-1$ edges.
> - Any two vertices of $T$ are connected by a unique path.
> Use the characterization most convenient for your proof or construction.

### Basic facts / examples
- A single vertex is a tree (with $0$ edges); an edge is a tree on $2$ vertices.
- Every tree with at least $2$ vertices has at least two leaves (see Lemma 2.1.3 in the lecture notes).
- Removing a leaf from an $n$‑vertex tree produces a tree on $n-1$ vertices.
- A spanning tree of a connected graph $G$ is a tree subgraph of $G$ containing all vertices of $G$. Spanning trees are fundamental in algorithms (BFS/DFS, minimum spanning tree problems) and structural proofs.

### Relations
- Core definition: [[content/foundational/graph.md]] (graph, degree, adjacency).
- Connectedness and uniqueness of paths: [[content/graph structure/connectedness.md]], [[content/graph structure/walk, trail, path, cycle.md]].
- Components and forests: [[content/foundational/components (graph).md]].
- Degree facts and parity: [[content/foundational/degree.md]], [[content/foundational/handshake lemma.md]].
- Results about cycles used in tree arguments: [[content/theorems, lemma/lemma - minimum degree 2 implies cycle.md]], [[content/theorems, lemma/lemma - walk contains path.md]].
- Global metrics where trees appear as extremal examples: [[content/foundational/distance, diameter.md]].
- As stated, every tree is [[theorem - bipartite characterization|bipartite]].
- Examples and exercises referencing lecture material: `content/examples` (Definition 2.1.1; Lemma 2.1.3).
