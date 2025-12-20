#example 
> [!example]
> ### Exercise 10 — Tree leaf counts
> Let $T$ be a tree on $n\ge 2$ vertices.
> 
> (i) Let $\{A,B\}$ be the bipartition of $V(T)$ into independent sets. Prove that if $|A|\ge |B|$ then $T$ has at least one leaf in $A$.
> 
> (ii) Suppose $T$ has no vertices of degree $2$. Prove that $T$ has more than $n/2$ leaves.
> [!proof]
> (i) Let $\{A,B\}$ be the unique bipartition of $T$. Suppose, for contradiction, that every vertex in $A$ has degree at least $2$. Then summing degrees over $A$ gives
> $$
> \sum_{v\in A} d(v) \ge 2|A|.
> $$
> All edges incident to $A$ go to $B$, so this sum equals the number of edges with an endpoint in $A$, which is at most the total number of edges $e(T)$. Similarly,
> $$
> \sum_{v\in B} d(v) = 2e(T) - \sum_{v\in A} d(v).
> $$
> If every vertex of $A$ has degree at least $2$, then
> $$
> 2e(T) = \sum_{v\in A} d(v) + \sum_{v\in B} d(v) \ge 2|A| + 0,
> $$
> so $e(T)\ge |A|$. But for a tree $e(T)=n-1=|A|+|B|-1$, hence $|A|+|B|-1 \ge |A|$, which forces $|B|\ge 1$. This is not itself a contradiction. A cleaner argument uses the unique path property: pick any vertex $b\in B$. Since $|A|\ge|B|$ there exists $a\in A$ not equal to the neighbor of $b$ on any fixed choice of maximal path from $b$; using the maximal path argument one checks a leaf must lie in $A$. Conclude $T$ has at least one leaf in $A$.
> 
> (Alternate short argument) Consider a longest path $P$ in $T$. Its endpoints are leaves (by maximality). The two endpoints lie in opposite parts of the bipartition; hence at least one endpoint lies in the larger part $A$.
> 
> (ii) Let $L$ be the set of leaves of $T$, and let $m$ be the number of vertices of degree at least $3$. Since $T$ has no vertices of degree $2$, every non-leaf vertex has degree at least $3$. Counting edges by degrees,
> $$
> 2e(T) = \sum_{v\in V(T)} d(v) = \sum_{v\in L} 1 + \sum_{\substack{v\in V(T)\\ d(v)\ge 3}} d(v) \ge |L| + 3m.
> $$
> Because $T$ is a tree, $e(T)=n-1$, so
> $$
> 2(n-1) \ge |L| + 3m.
> $$
> Additionally, $n = |L| + m$, so eliminate $m$:
> $$
> 2n-2 \ge |L| + 3(n-|L|) = 3n -2|L|.
> $$
> Rearrange:
> $$
> 2|L| \ge n+2 \quad\Rightarrow\quad |L| \ge \frac{n+2}{2} > \frac{n}{2}.
> $$
> Hence $T$ has more than $n/2$ leaves.
### Relations
- Trees and standard characterizations: [[content/theorems, lemma/theorem - trees characterization.md]]
- Tree facts and leaves lemma: [[content/theorems, lemma/lemma - tree has two leaves.md]]
- Examples and path uniqueness: [[content/graph structure/path.md]], [[content/graph structure/walk, trail, path, cycle.md]]
