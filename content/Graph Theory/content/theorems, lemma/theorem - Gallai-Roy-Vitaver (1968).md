> [!theorem]
> ### Theorem (Gallai–Roy–Vitaver 1968)
> Let $D$ be an orientation of a graph $G$ and let $l(D)$ be the length (number of edges) of a longest directed path in $D$. Then
> $$\chi(G)\le l(D)+1.$$ Moreover, equality holds for some orientation of $G$.

> [!proof]
> Let $D$ be any orientation of $G$ and let $D'$ be a maximal acyclic subdigraph of $D$ (i.e. $D'$ is acyclic and adding any edge from $E(D)\setminus E(D')$ creates a directed cycle). Note $l(D')\le l(D)$.
> 
> For each vertex $v\in V(G)$ let $f(v)$ be the length of a longest directed path in $D'$ that ends at $v$. We claim $f$ is a proper coloring of $G$ using at most $l(D')+1\le l(D)+1$ colors.
> 
> If $(u,v)\in E(D)$ and $f(u)=f(v)$, then two cases arise:
> - If $(u,v)\in E(D')$, the existence of a longest path ending at $u$ implies there is a path of length $f(u)+1$ ending at $v$, contradicting $f(v)=f(u)$ since $D'$ is acyclic.
> - If $(u,v)\in E(D)\setminus E(D')$, then by maximality of $D'$ adding $(u,v)$ creates a directed cycle, so there is a path from $v$ to $u$ in $D'$. Concatenating a longest path ending at $v$ with this path yields a path ending at $u$ of length at least $f(v)+2=f(u)+2$, contradicting the maximality of $f(u)$.
> 
> Thus adjacent vertices receive distinct values under $f$, so $f$ is a proper coloring with at most $l(D')+1\le l(D)+1$ colors.
> 
> For equality, let $k=\chi(G)$ and take a proper coloring of $G$ with color classes $V_1,\dots,V_k$. Orient every edge from $V_i$ to $V_j$ when $i<j$. This orientation has no directed path of length $k$; the longest path has length at most $k-1$, so $l(D)+1\le k$, giving equality for this orientation.
Relations
- See [[directed graph]] for orientation/digraph definitions.
- Related: [[theorem - Gallai-Roy-Vitaver (1968)]] (this file), and [[theorem - Mycielski construction]] for chromatic constructions.
- Corollary: Rédei's theorem on tournaments (Hamiltonian path) — see [[corollary - Rédei tournament Hamiltonian path]].
