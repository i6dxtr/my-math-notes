#theorem
> [!theorem]
> ### Theorem 1.2.14
> An edge is a cut-edge **if and only if** it belongs to no cycle.

> [!proof]
> Let $e$ be an edge in the graph and suppose $G$ is connected (otherwise restrict attention to the component containing $e$).
> 
> (⇒) Suppose $e$ belongs to a cycle $C$. Removing $e$ leaves the remainder of $C$ as an alternate path between the two endpoints of $e$, so every pair of vertices that were connected in $G$ remain connected in $G-e$. Hence $G-e$ has the same number of components as $G$, so $e$ is not a cut-edge.
> 
> (⇐) Conversely, suppose $G-e$ is connected. Let $e=xy$. Since $G-e$ is connected there exists an $x,y$-path $P$ in $G-e$. Adding the edge $e$ to $P$ produces a cycle in $G$ that contains $e$. Thus if $e$ is a cut-edge, no such cycle can exist.
### Relations
- Uses [[lemma - walk contains path|Lemma 1.2.5]] (walk→path) in the standard connectivity argument.
- Directly characterizes [[cut-vertex, cut-edge|cut-edges]].
- Connects to cycle-based structural results and to bridge/block decompositions.
- Related to decomposition and Eulerian/cycle covering results (see [[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)|proposition - decomposition into cycles iff even degree]] and [[theorem - eulerian circuit condition|theorem - eulerian circuit condition]]).
- Also used in proofs about matching corollaries that require absence of cut-edges (Petersen corollary): [[corollary - Petersen 3-regular perfect matching (3.3.8)|Petersen 3-regular perfect matching (3.3.8)]].
