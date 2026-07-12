> [!theorem]
> ### Theorem (Mycielski 1955)
> For every integer $k\ge 2$ there exists a graph $G$ with clique number $\omega(G)=2$ and chromatic number $\chi(G)=k$.

> [!proof]
> We describe the Mycielski construction $M(G)$ which given any graph $G$ produces a graph $M(G)$ with $\chi(M(G))=\chi(G)+1$ and $\omega(M(G))=\omega(G)$. Repeating the construction starting from a single edge (which has $\chi=2$, $\omega=2$) yields graphs with arbitrarily large chromatic number but triangle-free.
> 
> Construction: Let $G$ have vertices $v_1,\dots,v_n$. Form $M(G)$ with vertices
> $$\{v_1,\dots,v_n\}\cup\{u_1,\dots,u_n\}\cup\{w\}.$$
> Edges:
> - For each edge $v_iv_j\in E(G)$ include $v_iv_j$ in $E(M(G))$.
> - For each $i,j$ with $v_iv_j\in E(G)$ include $u_iv_j$ in $E(M(G))$.
> - Connect $w$ to every $u_i$.
> 
> One checks that $\omega(M(G))=\omega(G)$ and that $\chi(M(G))=\chi(G)+1$. Iterating this starting from $K_2$ (or an edge) produces for every $k\ge 2$ a graph with $\omega=2$ and $\chi=k$.
Relations
- See [[clique]] and [[chromatic number]].
- Related example: [[exercise - greedy coloring ordering]].
- 