#graph-property
> [!definition]
> ### Definition: Independent Set
> Let $G$ be a [[graph]] and $A \subseteq V(G)$.  
> $A$ is an **independent set** if no two vertices of $A$ are adjacent in $G$. Equivalently, the induced subgraph $G[A]$ has no edges.

> [!remark]
> The independence number $\alpha(G)$ denotes the size of a largest independent set in $G$.

### Relations
- Complementary to [[content/foundational/clique.md|clique]]: independent sets in $G$ are cliques in $\overline{G}$ ([[content/foundational/graph complement.md|graph complement]]).
- Color classes in a proper coloring are independent sets (see [[content/foundational/chromatic number.md|chromatic number]]).
- Appears in extremal bounds and matching/covering dualities (see [[content/foundational/matching.md|matching]]).
- Useful in algorithmic and combinatorial arguments (Turán-type results, greedy approximations).
- Independence number is related to vertex covers and matchings via inequalities and equalities in bipartite graphs (see [[content/foundational/vertex cover.md|vertex cover]], [[content/theorems, lemma/theorem - KÃ¶nigâ€“EgervÃ¡ry (1931).md|KÃ¶nigâ€“EgervÃ¡ry theorem]]).
- Independent sets are referenced in connectivity/Hamiltonicity conditions that use $\,\alpha(G)$ (see [[content/theorems, lemma/theorem - Chv\'atal-Erd\'os Hamiltonicity condition.md|Chvátal–Erdős Hamiltonicity condition]]).
