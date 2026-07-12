#theorem
> [!theorem]
> ### Theorem — Minimum-degree connectivity bound (Theorem 1.3.15)
> Let $G$ be a graph on $n$ vertices. If $\delta(G)\ge \frac{n-1}{2}$ then $G$ is connected (in fact $G$ has diameter at most $2$).

> [!proof]
> Let $u,v\in V(G)$. If $uv\in E(G)$ we are done. Otherwise consider the neighborhoods $N(u)$ and $N(v)$. We have
> $$
> |N(u)\cap N(v)| = |N(u)| + |N(v)| - |N(u)\cup N(v)| \ge \delta(G)+\delta(G) - (n-2).
> $$
> Using $\delta(G)\ge \frac{n-1}{2}$ we obtain
> $$
> |N(u)\cap N(v)| \ge \frac{n-1}{2} + \frac{n-1}{2} - (n-2) = 1.
> $$
> Thus there exists $x\in N(u)\cap N(v)$, and $uxv$ is a path of length $2$ between $u$ and $v$. Since this holds for every pair $u,v$, $G$ is connected and every pair of vertices is at distance at most $2$, so the diameter of $G$ is at most $2$.
### Relations
- Neighborhood and degree definitions: [[degree]], [[graph]].
- Minimum-degree consequences and long path/cycle results: [[theorem - minimum degree & path-cycle length]], [[theorem - dirac (hamiltonian)]].
- Applications to diameter/centrality: [[distance, diameter]].
