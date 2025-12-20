> [!example]
> ### Exercise 21.
> Proof of Exercise 21.
> 
> (i) Let $G$ be a graph on $n$ vertices and let $v \in V(G).$ If $G-v$ is complete, then $\kappa(G-v) = n-1-1 \ge \kappa(G)-1.$ So suppose $G-v$ is not complete and let $S'$ be a minimum vertex cut of $G-v.$ If $|S'| \le \kappa(G) - 2,$ then $S' \cup \{v\}$ is a vertex cut of size at most $\kappa(G) - 1$ in $G-v$ (sic), which is not possible, so $|S'| \ge \kappa(G) - 1$ which proves the first claim.
> 
> (ii) Let $e \in E(G)$ and let $F'$ be a minimum disconnecting set of $G-e.$ If $|F'| \le \kappa'(G)-2,$ then $F' \cup \{e\}$ is an disconnecting set of size at most $\kappa'(G)-1,$ which is not possible, so $|F'| \ge \kappa'(G)-1.$ Let $F$ be a minimum disconnecting set of $G,$ then clearly $F \setminus \{e\}$ (which may equal $F$) is an disconnecting set in $G-e,$ so $\kappa'(G) \ge \kappa'(G-e).$
> 
> _For the example, let $0 \le k < \ell$ and let $G$ be the graph consisting of a complete graph $K_{\ell+1}$ together with a vertex $v$ having $k$ neighbors in $K_{\ell+1}.$ We have $\kappa(G) = k,$ but $\kappa(G-v) = \kappa(K_{\ell+1}) = \ell.$_ $\square$
> 
> 
> Relations
> - [[separating set, connectivity]]
> - [[disconnecting set, edge-connectivity]]
> - [[lemma - minimal disconnecting set is edge cut]]