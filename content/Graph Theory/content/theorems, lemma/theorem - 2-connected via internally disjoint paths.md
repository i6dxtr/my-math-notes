> [!theorem]
> ### Characterization of 2-connected graphs via internally disjoint paths
> Let $G$ be a graph on at least $3$ vertices. Then $G$ is $2$-connected (connected and has no cut-vertex) if and only if for every pair of distinct vertices $u,v\in V(G)$ there exist two internally disjoint $u,v$-paths in $G$.

> [!proof]
> (⇒) Contrapositive. If $\kappa(G)\le 1$ then either $G$ is disconnected (so pick $u,v$ in different components and there are no $u,v$-paths) or $G$ has a cut-vertex $x$. If $x$ is a cut-vertex, choose $u,v$ in distinct components of $G-x$; every $u,v$-path must pass through $x$, so there cannot be two internally disjoint $u,v$-paths.
> 
> (⇐) Suppose for every distinct $u,v$ there are two internally disjoint $u,v$-paths. Then $G$ is connected. If $G$ had a cut-vertex $x$, pick vertices $u,v$ lying in different components of $G-x$. Any $u,v$-path must use $x$, contradicting the existence of two internally disjoint $u,v$-paths. Hence $G$ has no cut-vertex and is $2$-connected.
> 
> A constructive proof of (⇐) proceeds by induction on the distance $d(u,v)$ between $u$ and $v$ (see lecture notes): for adjacent vertices remove the edge $uv$ and find a $u,v$-path in the remainder, producing two internally disjoint paths; for larger distances use an inductive argument by shortening paths and patching as needed.
### Relations
- [[internally disjoint paths]] — Definition of internally disjoint paths.
- [[theorem - equivalent conditions for 2-connected graphs]] — This characterization is one of the equivalent conditions for 2-connectivity.
- [[ Menger-type equivalences]] — Strengthened versions of this statement appear in Menger/Mängel theorems for general $k$.
  
