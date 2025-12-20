#foundational
> [!definition]
> ### Definition: Graph Isomorphism
> Let $G=(V,E)$ and $H=(V',E')$ be graphs. We say $G$ and $H$ are **isomorphic** (write $G\cong H$) if there exists a bijection $\varphi:V\to V'$ such that for every $u,v\in V$,
> $$uv\in E \iff \varphi(u)\varphi(v)\in E'.$$
> In words, $G$ and $H$ have the same adjacency structure up to relabelling of vertices.

> [!remark]
> Isomorphism is the standard notion of equality for graphs: two graphs that are isomorphic are indistinguishable by properties depending only on adjacency (degree sequence, connectivity, presence of cycles, etc.), though vertex labels may differ.

### Relations
- Base definition: [[graph|graph]] — isomorphism compares graphs at the level of vertex/edge sets.
- Substructures: [[(induced) subgraphs|subgraphs and induced subgraphs]] — isomorphism often used to compare subgraphs.
- Components & connectivity: [[components (graph)|components (graph)]] and [[connectedness|connectedness]] — isomorphism preserves component structure.
- Examples and uses: compare with [[graph complement|graph complement]] (complements of isomorphic graphs are isomorphic), and with canonical families like complete graphs $K_n$, cycles $C_k$, and paths $P_k$.
- See also: [[order, size|order & size]] (isomorphic graphs have same order and size), [[degree|degree]] (degree sequences are preserved under isomorphism).
