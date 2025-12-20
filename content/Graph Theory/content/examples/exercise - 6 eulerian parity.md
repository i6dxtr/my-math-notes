#example 
> [!example]
> ### Exercise 6 — Eulerian graphs and parity of edges
> Prove or disprove:
> 1. If $G$ is bipartite and Eulerian, then $G$ has an even number of edges.
> 2. If $G$ is Eulerian and has an even number of edges, then $G$ is bipartite.> [!proof]
> (1) True. Let $G=(A\cup B,E)$ be bipartite and Eulerian. Eulerian means every vertex has even degree. Summing degrees over $A$ gives
> $$\sum_{v\in A} d(v)=\sum_{v\in A}\text{(even)}=\text{even},$$
> and summing over $B$ likewise yields an even integer. But by double counting (Handshake Lemma) both sums equal $e(G)$, the number of edges. Hence $e(G)$ is even.
> 
> (2) False. Provide a counterexample. Take two triangles $C_3$ sharing a single vertex (a "bow-tie" with central shared vertex). Concretely, let the vertex set be $\{v_0,v_1,v_2,v_3,v_4\}$ and edges
> $$\{v_0v_1,v_1v_2,v_2v_0\}\cup\{v_0v_3,v_3v_4,v_4v_0\}.$$
> Degrees are $d(v_0)=4$ and $d(v_i)=2$ for $i=1,2,3,4$, so every degree is even and the graph is Eulerian; the number of edges is $6$, which is even. However the graph contains a triangle (odd cycle), so it is not bipartite. Therefore the implication (Eulerian + even number of edges $\implies$ bipartite) is false.
### Remarks
- Alternative (1) viewpoint: Eulerian bipartite graphs decompose into edge-disjoint even cycles, so the total edge count is a sum of even numbers and hence even.
- The counterexample in (2) shows parity of $e(G)$ alone does not force the absence of odd cycles.

### Relations
- Eulerian characterization: [[content/theorems, lemma/theorem - eulerian circuit condition.md]].
- Parity and degree counting: [[content/foundational/handshake lemma.md]], [[content/foundational/degree.md]].
- Bipartiteness and odd-cycle obstruction: [[content/theorems, lemma/theorem - bipartite characterization.md]].
