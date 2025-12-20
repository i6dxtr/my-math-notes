#foundational
> [!definition]
> ### Definition: Graph Isomorphism
> Let $G=(V,E)$ and $H=(V',E')$ be graphs. We say $G$ and $H$ are **isomorphic** (write $G\cong H$) if there exists a bijection $\varphi:V\to V'$ such that for every $u,v\in V$,
> $$uv\in E \iff \varphi(u)\varphi(v)\in E'.$$
> In words, $G$ and $H$ have the same adjacency structure up to relabelling of vertices.

> [!remark]
> Isomorphism is the standard notion of equality for graphs: two graphs that are isomorphic are indistinguishable by properties depending only on adjacency (degree sequence, connectivity, presence of cycles, etc.), though vertex labels may differ.

### Relations
- Base definition: [[content/foundational/graph.md|graph]] — isomorphism compares graphs at the level of vertex/edge sets.
- Substructures: [[content/graph structure/(induced) subgraphs.md|subgraphs and induced subgraphs]] — isomorphism often used to compare subgraphs.
- Components & connectivity: [[content/foundational/components (graph).md|components (graph)]] and [[content/graph structure/connectedness.md|connectedness]] — isomorphism preserves component structure.
- Examples and uses: compare with [[content/foundational/graph complement.md|graph complement]] (complements of isomorphic graphs are isomorphic), and with canonical families like complete graphs $K_n$, cycles $C_k$, and paths $P_k$.
- See also: [[content/foundational/order, size.md|order & size]] (isomorphic graphs have same order and size), [[content/foundational/degree.md|degree]] (degree sequences are preserved under isomorphism).
