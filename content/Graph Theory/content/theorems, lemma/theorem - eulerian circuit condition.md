#theorem
> [!theorem]
> ### Theorem 1.2.26 — Eulerian Circuit Characterization
> A (not necessarily simple) graph $G$ has an Eulerian circuit (a closed trail that uses every edge of $G$ exactly once) if and only if
> 1. $G$ has at most one nontrivial component (i.e., at most one component contains an edge), and  
> 2. every vertex of $G$ has even degree.

> [!proof]
> (⇒) If $G$ has an Eulerian circuit then the circuit lies entirely inside a single nontrivial component, so there is at most one nontrivial component. Traversing the Eulerian circuit enters and leaves every vertex the same number of times, so each vertex is incident with an even number of traversed edges; hence every vertex has even degree.
> 
> (⇐) Conversely, suppose every vertex of $G$ has even degree and $G$ has at most one nontrivial component. If $G$ has no edges the statement is trivial. Otherwise, let $C$ be a cycle in the nontrivial component (existence of a cycle follows from Lemma 1.2.25 when needed). Remove the edges of $C$ from $G$; every vertex still has even degree in the remaining graph. Each component of the remaining graph has fewer edges, and by induction on the number of edges each such component has an Eulerian circuit. Splicing the circuit(s) of those components into $C$ at the appropriate vertices produces an Eulerian circuit for $G$.
### Relations
- Uses Lemma 1.2.25 ([[lemma - minimum degree 2 implies cycle|minimum degree ⇒ cycle]]) in the inductive existence of a starting cycle.
- Connects parity of degrees ([[degree|degree]]) to global traversal properties of graphs.
- Related to decomposition results into cycles when all degrees are even ([[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)|decomposition into cycles iff even degree]]).
- Eulerian conditions are used in algorithmic contexts and relate to matching/covering parity observations; see [[handshake lemma|handshake lemma]] and [[theorem - matching + edge cover = n|theorem - matching + edge cover = n]].
