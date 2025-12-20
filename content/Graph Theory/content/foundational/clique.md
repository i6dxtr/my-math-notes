#graph-property #definition 
> [!definition]
> ### Definition: Clique
> Let $G$ be a [[graph]] and $Z \subseteq V(G)$.  
> $Z$ is a **clique** if every pair of distinct vertices in $Z$ are adjacent in $G$. Equivalently, the induced subgraph $G[Z]$ is a complete graph.

> [!remark]
> The clique number $\omega(G)$ denotes the size of a largest clique in $G$.

### Relations
- Complementary to [[independent set|independent set]]: cliques in $G$ are independent sets in $\overline{G}$ ([[graph complement|graph complement]]).
- Cliques provide lower bounds on the chromatic number: $\chi(G) \ge \omega(G)$ (every clique requires distinct colors).
- Appears in extremal problems and is central to Turán-type results and Ramsey theory.
- Related concept: complete graphs, see [[graph|graph]].
- Cliques and independence/clique bounds appear in Hamiltonicity/connectivity bounds (Chvátal–Erdős) and in constructions like Mycielski that separate these parameters (see [['os Hamiltonicity condition|Chvátal–Erdős Hamiltonicity condition]], [[theorem - Mycielski construction|Mycielski construction]]).
