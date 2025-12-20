#definition 
> [!definition]
> ### Definition — Directed graph (digraph), in-degree, out-degree
> A directed graph (or digraph) is an ordered pair $D=(V,A)$ where $A\subseteq V\times V$ and $(v,v)\notin A$ for all $v\in V$ (no loops). Elements of $V$ are called vertices and elements of $A$ are called directed edges or arcs. We often write $uv$ for the arc $(u,v)$ and treat the order as significant.
> 
> Given a vertex $v\in V(D)$:
> - The out-neighborhood of $v$ is $N^+(v)=\{w\in V : (v,w)\in A\}$ and the out-degree is $d^+(v)=|N^+(v)|$.
> - The in-neighborhood of $v$ is $N^-(v)=\{u\in V : (u,v)\in A\}$ and the in-degree is $d^-(v)=|N^-(v)|$.
> - The total degree (for comparison with undirected graphs) can be written $d(v)=d^+(v)+d^-(v)$.

> [!remark]
> - Many undirected graph concepts have directed analogues (paths, cycles, connectivity), but one must be careful with orientations: e.g. a directed path requires arcs that respect direction.
> - We typically reserve the term "graph" for simple undirected graphs in these notes; use this file when directed structures are relevant.
>   
> ![[Pasted image 20250920193203.png]]*A directed graph.*

> [!proof]
> This file records the definition and standard notation for directed graphs used in lectures. No proof is required.

### Relations
- Basic graph definitions and comparisons: [[graph]]
- Degree conventions and parity: [[degree]]
- Directed variants of paths and cycles: [[walk, trail, path, cycle]]
