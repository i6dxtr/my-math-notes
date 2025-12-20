#graph-property #definition 
> [!definition]
> ### Definition: Clique
> Let $G$ be a [[graph]] and $Z \subseteq V(G)$.  
> $Z$ is a **clique** if every pair of distinct vertices in $Z$ are adjacent in $G$. Equivalently, the induced subgraph $G[Z]$ is a complete graph.

> [!remark]
> The clique number $\omega(G)$ denotes the size of a largest clique in $G$.

### Relations
- Complementary to [[content/foundational/independent set.md|independent set]]: cliques in $G$ are independent sets in $\overline{G}$ ([[content/foundational/graph complement.md|graph complement]]).
- Cliques provide lower bounds on the chromatic number: $\chi(G) \ge \omega(G)$ (every clique requires distinct colors).
- Appears in extremal problems and is central to Turán-type results and Ramsey theory.
- Related concept: complete graphs, see [[content/foundational/graph.md|graph]].
- Cliques and independence/clique bounds appear in Hamiltonicity/connectivity bounds (Chvátal–Erdős) and in constructions like Mycielski that separate these parameters (see [[content/theorems, lemma/theorem - Chv\'atal-Erd\'os Hamiltonicity condition.md|Chvátal–Erdős Hamiltonicity condition]], [[content/theorems, lemma/theorem - Mycielski construction.md|Mycielski construction]]).
