#graph-metric #definition 
> [!definition]
> ### Definition: Distance
> For vertices $u,v\in V(G)$, the **distance** $d(u,v)$ is the length (number of edges) of a shortest path between $u$ and $v$. If no $u,v$-path exists then $d(u,v)=\infty$.

> [!definition]
> ### Definition: Diameter and Radius
> - The **diameter** of $G$, denoted $\mathrm{diam}(G)$, is $\max_{u,v\in V(G)} d(u,v)$.  If $G$ is disconnected, $\mathrm{diam}(G)=\infty$.
> - The **eccentricity** of a vertex $v$ is $\mathrm{ecc}(v)=\max_{u\in V(G)} d(v,u)$.
> - The **radius** of $G$ is $\mathrm{rad}(G)=\min_{v\in V(G)} \mathrm{ecc}(v)$.

> [!remark]
> Distances give a metric on each connected component. Diameter and radius measure global and center-based compactness of a graph, respectively.

### Relations
- Defined using [[content/graph structure/path.md|paths]] and the lemma [[content/theorems, lemma/lemma - walk contains path.md|lemma - walk contains path]].
- Useful when comparing a graph with its complement (see [[content/foundational/graph complement.md|graph complement]]); several exercises relate diameters of $G$ and $\overline{G}$.
- Diameter and radius connect to algorithmic topics (shortest‑path algorithms) and to structural bounds (e.g., trees, eccentricity center).
- Diameter and distance metrics are preserved/approximated by BFS trees (see [[content/graph structure/definition - breadth-first search tree (BFST).md|definition - breadth-first search tree (BFST)]], [[content/theorems, lemma/theorem - BFS preserves distances (Theorem 2.3.8).md|theorem - BFS preserves distances]]).
- Distance/diameter considerations also interact with connectivity, cycles, and Hamiltonicity remarks in later lectures (see [[content/graph structure/connectedness.md|connectedness]], [[content/theorems, lemma/theorem - minimum degree & path-cycle length.md|theorem - minimum degree & path-cycle length]]).
