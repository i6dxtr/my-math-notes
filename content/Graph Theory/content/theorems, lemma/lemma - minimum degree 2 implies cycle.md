#lemma

> [!corollary]
> ### Lemma 1.2.25
> Every (simple) graph $G$ with minimum degree $\delta(G)\ge 2$ contains a cycle.

> [!proof]
> If $G$ is not simple (has a loop or a parallel edge), then there is immediately a cycle (a loop or a 2-cycle). So assume $G$ is simple.
> 
> Let $P=v_1v_2\cdots v_k$ be a maximal path in $G$ (maximal with respect to inclusion of vertices). Since $P$ is maximal, every neighbour of $v_1$ lies in $V(P)$. Because $d(v_1)\ge 2$, vertex $v_1$ has some neighbour $v_i$ with $i\ge 3$; otherwise $v_1$ would have at most one neighbour on $P$. But then $v_1v_2\cdots v_i v_1$ is a cycle in $G$, as required.
### Relations
- Used in the inductive proof of the Eulerian circuit characterization ([[theorem - eulerian circuit condition|theorem - eulerian circuit condition]]).
- Relies on maximal path arguments; see [[path|path]] and [[proposition - maximal paths & cycles|proposition - maximal paths & cycles]].
- Provides a simple degree-based existence condition for cycles; complements other degree-arguments in the notes.
- Serves as a stepping stone to Dirac-style minimum degree results about long paths and cycles ([[theorem - minimum degree & path-cycle length|theorem - minimum degree & path-cycle length]]).
