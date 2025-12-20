#example 
> [!example]
> ### Exercise 8 — Hamiltonicity bounds
> #### (i).
> For all $n\ge 3$, give a graph on $n$ vertices with $\delta(G)=\lceil n/2\rceil-1$ such that $G$ has no Hamiltonian cycle.  
> 
> ---
> #### (ii).
> Let $G$ be a graph on $n\ge 3$ vertices with $\delta(G)\ge (n+1)/2$. Prove that for all distinct $u,v\in V(G)$ there is a $u,v$‑path with $n$ vertices (a Hamiltonian $u$–$v$ path).> [!proof]
> (i) Construction. Let $n\ge 3$ and set
> $$a=\Big\lfloor\frac{n}{2}\Big\rfloor+1,\qquad b=n-a=\Big\lceil\frac{n}{2}\Big\rceil-1.$$
> Consider the complete bipartite graph $G=K_{a,b}$. Every vertex in the smaller part has degree $a$ and every vertex in the larger part has degree $b$, so
> $$\delta(G)=\min\{a,b\} = \Big\lceil\frac{n}{2}\Big\rceil-1.$$
> Complete bipartite graphs $K_{a,b}$ admit a Hamiltonian cycle only when $a=b$ (a necessary condition since a Hamiltonian cycle alternates parts). Here $a\ne b$, so $G$ has no Hamiltonian cycle, as required.
> 
> ---
> (ii) Let $G$ be as stated and fix distinct $u,v\in V(G)$. Remove $v$ to obtain the graph $G-v$ on $n-1$ vertices. For any vertex $w\in V(G-v)$ we have
> $$d_{G-v}(w)\ge d_G(w)-1 \ge \frac{n+1}{2}-1 = \frac{n-1}{2}.$$
> Thus $\delta(G-v)\ge (n-1)/2$. Since $n-1\ge 2$, Dirac's theorem applies to $G-v$: because $(n-1)\ge 3$ when $n\ge 4$ (the small cases $n=3$ can be checked directly), $G-v$ is Hamiltonian; it contains a Hamiltonian cycle $C$ visiting all vertices of $G-v$. Let $x,y$ be consecutive vertices on $C$ that are neighbours of $v$ in $G$ (such neighbors exist because $d_G(v)\ge (n+1)/2>0$). Breaking the cycle at the edge $xy$ and inserting $v$ between $x$ and $y$ yields a Hamiltonian $u$–$v$ path in $G$; by rotating the cycle if necessary we can ensure the resulting path has endpoints $u$ and $v$. For the small cases ($n=3$) the condition $\delta(G)\ge (n+1)/2$ forces $\delta(G)\ge 2$ so $G\cong K_3$ and the claim holds trivially.
> 
> Hence for all distinct $u,v$ there is a $u,v$‑path that visits every vertex of $G$.
> [!remark]
> - Part (i) shows the threshold $\delta(G)\ge n/2$ in Dirac's theorem is essentially tight: lowering the minimum degree by $1$ can destroy Hamiltonicity.
> - Part (ii) is a standard Dirac‑based argument: remove one endpoint and use Dirac on the remainder to produce a Hamiltonian cycle, then splice the removed vertex back to create a Hamiltonian path between prescribed vertices.
### Relations
- Dirac's theorem: [[theorem - dirac (hamiltonian)]].
- Path and cycle definitions: [[path]], [[walk, trail, path, cycle]]
