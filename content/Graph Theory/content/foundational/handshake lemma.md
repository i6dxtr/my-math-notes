#lemma
> [!theorem]
> ### Handshake Lemma (Proposition 1.3.3)
> For every finite graph $G$,
> $$\sum_{v\in V(G)} d(v) \;=\; 2\,|E(G)|.$$

> [!proof]
> Each edge $uv\in E(G)$ contributes $1$ to $d(u)$ and $1$ to $d(v)$. Therefore every edge is counted exactly twice in $\sum_{v\in V(G)} d(v)$, which yields the claimed equality.

> [!corollary]
> In every finite graph, the number of vertices of odd degree is even.

> [!proof]
> Reduce the Handshake Lemma modulo $2$. The left-hand side equals the parity sum of vertex degrees; since the right-hand side $2|E(G)|$ is even, the parity sum is $0$, so an even number of vertices have odd degree.

### Remarks
- This proposition is frequently used in parity arguments and in proofs about Eulerian trails and circuits.
- It also provides a quick check for feasibility of degree sequences (parity condition).

### Relations
- Relies on the definition of [[degree]].
- Applied in proofs about Eulerian circuits (see [[theorem - eulerian circuit condition]]) and in parity/connectivity arguments (see [[components (graph)]]).
- Used throughout counting and matching arguments: degree-sum arguments appear in matching/edge-cover identities ([[theorem - matching + edge cover = n]], [[edge cover]], [[maximal matching, maximum matching]]), and in cycle decompositions ([[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)]]).
- Important in algorithmic analysis when summing work over adjacency lists (BFS/DFS) and in degree-based extremal results (Dirac-type bounds; see [[theorem - minimum degree & path-cycle length]]).
