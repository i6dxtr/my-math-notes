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
- Defined using [[path|paths]] and the lemma [[lemma - walk contains path|lemma - walk contains path]].
- Useful when comparing a graph with its complement (see [[graph complement|graph complement]]); several exercises relate diameters of $G$ and $\overline{G}$.
- Diameter and radius connect to algorithmic topics (shortest‑path algorithms) and to structural bounds (e.g., trees, eccentricity center).
- Diameter and distance metrics are preserved/approximated by BFS trees (see [[definition - breadth-first search tree (BFST)|definition - breadth-first search tree (BFST)]], [[theorem - BFS preserves distances (Theorem 2.3.8)|theorem - BFS preserves distances]]).
- Distance/diameter considerations also interact with connectivity, cycles, and Hamiltonicity remarks in later lectures (see [[connectedness|connectedness]], [[theorem - minimum degree & path-cycle length|theorem - minimum degree & path-cycle length]]).
