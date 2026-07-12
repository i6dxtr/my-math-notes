#theorem
> [!theorem]
> ### Theorem — Characterizations of Trees (Theorem 2.1.4)
> Let $G$ be a graph on $n$ vertices. The following are equivalent:
> 1. $G$ is connected and acyclic (i.e. $G$ is a tree).
> 2. $G$ is connected and has $n-1$ edges.
> 3. $G$ is acyclic and has $n-1$ edges.
> 4. For all $u,v\in V(G)$ there is exactly one $u,v$-path in $G$.

> [!proof]
> We sketch the standard equivalences.
> 
> $(1)\Rightarrow(2)$: By induction on $n$. For $n=1$ the claim is trivial. For $n\ge 2$, let $G$ be a connected acyclic graph on $n$ vertices. A tree with at least two vertices has a leaf $v$ (vertex of degree $1$). Then $G-v$ is a tree on $n-1$ vertices, so by the inductive hypothesis $e(G-v)=n-2$. Adding the unique edge incident with $v$ gives $e(G)=n-1$.
> 
> $(2)\Rightarrow(3)$: Suppose $G$ is connected and $e(G)=n-1$. If $G$ had a cycle, we could delete an edge from a cycle and remain connected, producing a connected acyclic graph with fewer than $n-1$ edges, contradicting $(1)\Rightarrow(2)$ applied to that graph. Hence $G$ is acyclic.
> 
> $(3)\Rightarrow(1)$: Suppose $G$ is acyclic and $e(G)=n-1$. Let $H_1,\dots,H_k$ be the components of $G$ and let $n_i=|V(H_i)|$. Each component is an acyclic graph so by $(1)\Rightarrow(2)$ applied to each component we have $e(H_i)=n_i-1$. Summing,
> $$
> n-1=e(G)=\sum_{i=1}^k e(H_i)=\sum_{i=1}^k(n_i-1)=n-k,
> $$
> so $k=1$ and $G$ is connected.
> 
> $(4)\Rightarrow(1)$: If there is a unique $u,v$-path for every pair $u,v$, then in particular $G$ is connected. If a cycle existed, two distinct $u,v$-paths could be obtained for some $u,v$ on the cycle, a contradiction; hence $G$ is acyclic.
> 
> $(1)\Rightarrow(4)$: If $G$ is connected and acyclic, suppose for contradiction that some $u,v$ have two distinct $u,v$-paths $P$ and $Q$. Choose such a pair $u,v$ with $P,Q$ minimizing $|V(P)|+|V(Q)|$. If $P$ and $Q$ intersect at a vertex $w\not\in\{u,v\}$ then we obtain two shorter $w,v$-paths contradicting minimality. Thus $P$ and $Q$ are internally vertex-disjoint and together form a cycle, contradicting that $G$ is acyclic.
> 
> This completes the equivalences.
### Relations
- Core definition and examples of trees: [[tree]]
- Components and the equivalence-of-connectedness lemma: [[connectedness]], [[lemma - connectivity equivalence relation]]
- Paths and uniqueness arguments: [[walk, trail, path, cycle]], [[path]]
