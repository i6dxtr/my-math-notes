#graph-property
> [!definition]
> ### Definition: Independent Set
> Let $G$ be a [[graph]] and $A \subseteq V(G)$.  
> $A$ is an **independent set** if no two vertices of $A$ are adjacent in $G$. Equivalently, the induced subgraph $G[A]$ has no edges.

> [!remark]
> The independence number $\alpha(G)$ denotes the size of a largest independent set in $G$.

### Relations
- Complementary to [[clique|clique]]: independent sets in $G$ are cliques in $\overline{G}$ ([[graph complement|graph complement]]).
- Color classes in a proper coloring are independent sets (see [[chromatic number|chromatic number]]).
- Appears in extremal bounds and matching/covering dualities (see [[matching|matching]]).
- Useful in algorithmic and combinatorial arguments (Turán-type results, greedy approximations).
- Independence number is related to vertex covers and matchings via inequalities and equalities in bipartite graphs (see [[vertex cover|vertex cover]], [[theorem - KÃ¶nigâ€“EgervÃ¡ry (1931)|KÃ¶nigâ€“EgervÃ¡ry theorem]]).
- Independent sets are referenced in connectivity/Hamiltonicity conditions that use $\,\alpha(G)$ (see [['os Hamiltonicity condition|Chvátal–Erdős Hamiltonicity condition]]).
