#theorem
> [!theorem]
> ### Theorem 1.2.14
> An edge is a cut-edge **if and only if** it belongs to no cycle.
> [!proof]
> Let $e$ be an edge in the graph and suppose $G$ is connected (otherwise restrict attention to the component containing $e$).
> 
> (⇒) Suppose $e$ belongs to a cycle $C$. Removing $e$ leaves the remainder of $C$ as an alternate path between the two endpoints of $e$, so every pair of vertices that were connected in $G$ remain connected in $G-e$. Hence $G-e$ has the same number of components as $G$, so $e$ is not a cut-edge.
> 
> (⇐) Conversely, suppose $G-e$ is connected. Let $e=xy$. Since $G-e$ is connected there exists an $x,y$‑path $P$ in $G-e$. Adding the edge $e$ to $P$ produces a cycle in $G$ that contains $e$. Thus if $e$ is a cut-edge, no such cycle can exist.
### Relations
- Uses [[content/theorems, lemma/lemma - walk contains path.md|Lemma 1.2.5]] (walk→path) in the standard connectivity argument.
- Directly characterizes [[content/graph structure/cut-vertex, cut-edge.md|cut-edges]].
- Connects to cycle-based structural results and to bridge/block decompositions.
- Related to decomposition and Eulerian/cycle covering results (see [[content/theorems, lemma/proposition - decomposition into cycles iff even degree (Proposition 1.2.27).md|proposition - decomposition into cycles iff even degree]] and [[content/theorems, lemma/theorem - eulerian circuit condition.md|theorem - eulerian circuit condition]]).
- Also used in proofs about matching corollaries that require absence of cut-edges (Petersen corollary): [[content/theorems, lemma/corollary - Petersen 3-regular perfect matching (3.3.8).md|Petersen 3-regular perfect matching (3.3.8)]].
