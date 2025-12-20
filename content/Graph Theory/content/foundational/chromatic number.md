#graph-property
> [!definition]
> ### Definition: Chromatic Number
> The **chromatic number** of a [[graph]] $G$, denoted $\chi(G)$, is the smallest positive integer $k$ for which there exists a partition
> $$V(G)=V_1\cup V_2\cup\cdots\cup V_k$$
> such that each $V_i$ is an independent set (i.e., no two vertices in any $V_i$ are adjacent).
### Alternate Definition
> [!definition]
> ### Definition 5.1.1, 5.1.4.
> *A proper $k-$coloring of a graph $G$ is a function $c:V( G )\rightarrow \left[ k \right]$ such that if $uv\in E( G ),$ then $c( u )\neq c( v ).$ The smallest $k$ for which $G$ has a proper $k-$coloring is called the **chromatic number** of $G,$ and is denoted $\chi( G ).$*

> [!remark]
> Note that $\left\{ c^{-1}( \left\{ 1 \right\} ), c^{-1}( \left\{ 2 \right\} ),...,c^{-1}( \left\{ k \right\} ) \right\}$ is a partition of $V( G )$ into independent sets, so $\chi( G )$ is the minimum number of independent sets $G$ can be partitioned into.

> [!remark]
> Equivalently, $\chi(G)$ is the minimum number of colors needed to color the vertices of $G$ so that adjacent vertices receive different colors.

### Lemma Z.
> [!corollary]
> ### Lemma $Z.$
> Let $k$ be a positive integer and let $G$ be a graph with $\chi ( G )=k.$ For every proper $k-$coloring of $G$ and every color $i\in \left[ k \right],$ there exists a vertex of color $i$ that is adjacent to at least one other vertex of every other color.


### Basic facts
- For any graph $G$, $\chi(G)\ge 1$, and $\chi(G)=1$ iff $G$ has no edges.
- Clique bound: $\chi(G)\ge \omega(G)$, where $\omega(G)$ is the clique number (size of a largest clique).
- Trivial upper bound: $\chi(G)\le n(G)$ (color each vertex differently).

### Relations
- Defined in terms of [[content/foundational/independent set.md|independent sets]].
- Lower-bounded by [[content/foundational/clique.md|clique number $\omega(G)$]].
- Bipartite graphs satisfy $\chi(G)\le 2$; see [[content/bipartite graph.md|bipartite graph]] and [[content/theorems, lemma/theorem - bipartite characterization.md|theorem - bipartite characterization]].
- Useful in extremal combinatorics, algorithmic graph coloring, and complexity theory (NP-completeness of computing $\chi(G)$).
- Appears in advanced constructions and bounds: Mycielski construction produces triangle-free graphs with large chromatic number ([[content/theorems, lemma/theorem - Mycielski construction.md|Mycielski construction]]), and the Gallai–Roy–Vitaver theorem connects orientations to chromatic bounds ([[content/theorems, lemma/theorem - Gallai-Roy-Vitaver (1968).md|Gallai–Roy–Vitaver]]).
