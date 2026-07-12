#definition
> [!definition]
> A **component** $C$ in a graph $G$ is a maximally connected induced subgraph of $G$; there is no $S \subseteq V(G)$ such that $V(C)$ is a proper subset of $S$ and the subgraph induced by $S$ is connected.

> [!corollary]
> ### Lemma 0.1.
> Given a graph $G$, let $\sim$ be a relation on $V(G)$ where $u \sim v$ *if and only if* there is a $u,v$-path in $G$. We have that $\sim$ is an equivalence relation and the equivalence classes are the components of $G$.
#### Relations
- Connectedness partitions a graph into [[components (graph)]].
- Components are equivalence classes under the connectivity relation; see [[lemma - connectivity equivalence relation]].
- Foundational for results about paths and cycles; see [[path]] and [[walk, trail, path, cycle]].
- Connects to subgraph notions ([[(induced) subgraphs]]), Eulerian circuit conditions ([[theorem - eulerian circuit condition]]), and bipartiteness ([[theorem - bipartite characterization]]).
- Later algorithms and tree results build on connectedness: BFS/DFST distance preservation and spanning tree constructions ([[algorithm - breadth-first search (BFS)]], [[definition - breadth-first search tree (BFST)]], [[definition - rooted tree and branch]]), and tree characterizations/lemmata (see [[tree]], [[lemma - tree has two leaves]]).
- Connectedness is also used in matching/Tutte arguments where odd components and vertex deletions play a central role ([[odd components]], [[Tutte's theorem]], [[theorem - Tutte's theorem (detailed proof)]]).
