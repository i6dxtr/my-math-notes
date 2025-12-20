#definition 
> [!definition]
> ### Definition — Matching, saturated/unsaturated vertex, perfect matching
> Let $G$ be a graph. A **matching** $M$ in $G$ is a set of pairwise disjoint edges (i.e., all endpoints of edges in $M$ are distinct).
> 
> ---
> A vertex $v$ is **saturated** by $M$ if $v$ is incident with some edge of $M$; otherwise $v$ is unsaturated. We say $M$ saturates a set $U\subseteq V(G)$ if every vertex in $U$ is saturated by $M$.
> 
> ---
> A **perfect matching** is a matching that saturates every vertex of $G$ (i.e., every vertex is incident with exactly one edge of $M$).

### Source
- lecture/438Notes_f25.pdf — Definition 3.1.1 (Matchings)
- Notes by date/9-28-25.md

### Relations
- Extremal questions about $\alpha(G)$ vs matchings: [[content/foundational/independent set.md]]
- Maximal/maximum matchings: [[content/foundational/maximal matching, maximum matching.md]]
- Alternating and augmenting paths: [[content/foundational/M-alternating path, M-augmenting path.md]]
- Paths and trails background: [[content/graph structure/walk, trail, path, cycle.md]], [[content/graph structure/path.md]]
