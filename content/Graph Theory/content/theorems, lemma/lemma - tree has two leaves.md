#lemma
> [!theorem]
> ### Lemma — Every tree with at least two vertices has at least two leaves (Lemma 2.1.3)
> Let $T$ be a tree with at least $2$ vertices. Then $T$ has at least two leaves (vertices of degree $1$). Moreover, deleting a leaf from an $n$-vertex tree produces a tree on $n-1$ vertices.
> [!proof]
> Let $P=v_1v_2\ldots v_k$ be a maximal path in $T$. Since $T$ is connected and has at least two vertices we have $k\ge 2$. By maximality every neighbor of $v_1$ lies in $V(P)$, and similarly every neighbor of $v_k$ lies in $V(P)$. If $v_1$ had degree $\ge 2$ then there would be some neighbor of $v_1$ outside $\{v_2\}$ which would allow extending $P$, contradicting maximality. Hence $d(v_1)=1$, and by the same argument $d(v_k)=1$. Thus $T$ has at least two leaves.
> 
> If we delete a leaf $v$ from $T$ then removing $v$ (and its incident edge) cannot create a cycle and cannot disconnect any remaining vertices that were previously connected by paths not using $v$. Therefore $T-v$ is acyclic and, since $T$ was connected, $T-v$ remains connected on $n-1$ vertices; hence $T-v$ is a tree.
### Relations
- Definition and examples of trees: [[content/foundational/tree.md]]
- Maximal vs maximum path discussion: [[content/theorems, lemma/proposition - maximal paths & cycles.md]]
- Paths and walk containment lemma: [[content/graph structure/walk, trail, path, cycle.md]]
