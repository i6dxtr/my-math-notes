> [!definition]
> ### Separating set (vertex cut) and connectivity
> A **separating set** (or vertex cut) of a graph $G$ is a set $S\subseteq V(G)$ such that $G-S$ has more than one component.
> 
> The **connectivity** of $G$, denoted $\kappa(G)$, is the minimum size of a separating set; by convention $\kappa(K_1)=0$. We say $G$ is $k$‑connected if $\kappa(G)\ge k$.

> [!remark]
> For all $n\in\mathbb{Z}^+$ we have $\kappa(K_n)=n-1$, since removing any $n-2$ vertices leaves at least two vertices joined by an edge, while removing $n-1$ leaves a single vertex.

> [!proof]
> $K_n$ has no separating set of size $<n-1$ (it remains connected after deleting fewer than $n-1$ vertices), and deleting $n-1$ vertices leaves a single vertex, so the minimum separating set size is $n-1$.

### Relations
- [[cut-vertex, cut-edge]] — Cut-vertex is a separating set of size $1$; the definitions are compatible.
- [[remark - connectivity of K_n]] — Short remark/proof that $\kappa(K_n)=n-1$ (this file provides a compact remark; keep both for navigation).
- [[theorem - Whitney inequality (4.1.7)]] — Connectivity is compared with edge‑connectivity and minimum degree in Whitney's inequality.
- [[disconnecting set, edge-connectivity]]
- [[connectedness]]

