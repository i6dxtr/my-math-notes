> [!example]
> ### Exercise 20.
> _Let $n \ge 2.$ Prove that if $G$ is a graph on $n$ vertices with $\delta(G) \ge n-2,$ then $\kappa(G) = \delta(G).$_
> 
> ad-proof
> If $\delta(G) = n-1,$ then $G$ is complete and we have $\kappa(G) = n-1 = \delta(G).$ So suppose $\delta(G) = n-2.$
> - Let $x$ be a vertex with $d(x) = n-2$ and let $y$ be the vertex such that $xy \notin E(G).$ Note that $V(G) \setminus \{x,y\}$ is a vertex cut, so $\kappa(G) \le n-2.$ * Note that for all $u, v \in V(G)$ with $uv \notin E(G),$ we have $|N(u) \cap N(v)| = d(u) + d(v) - (n-2) \ge 2(n-2) - (n-2) = n-2.$
> - Let $S \subseteq V(G)$ with $|S| \le n-3$ and let $u, v \in V(G) \setminus S.$ We have $|N(u) \cap N(v)| \ge n-2$ and thus $u$ and $v$ have a common neighbor in $V(G) \setminus S$ which means $G-S$ is connected. $\square$
> 
> 
> Relations
> - [[separating set, connectivity]]
> - [[degree]]
> - [[lemma - connectivity equivalence relation]]