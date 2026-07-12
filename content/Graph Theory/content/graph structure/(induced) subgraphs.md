#definition 
> [!definition]
> ### Subgraphs and Induced Subgraphs
> Given graphs $G = (V, E)$ and $H = (V', E')$, we say that $H$ is a **subgraph** of $G$ if $V' \subseteq V$ and $E' \subseteq E$.
> 
> Given $U \subseteq V(G)$, the subgraph induced by $U$ is the graph
> $$
> (U, \{ e \in E(G) : e \subseteq U \}).
> $$
> We denote this by $G[U]$.
> 
> Example:
> - $U = \{ v_2, v_3, v_4 \}$
> - $G[U] = (\{ v_2, v_3, v_4 \}, \{ v_2 v_3, v_3 v_4 \})$
> ![[Pasted image 20250827140554.png|400]]

> [!remark]
> #### Relations
> - Induced subgraphs are used to form components and to study connectivity; see [[components (graph)]] and [[connectedness]].
> - Induced subgraphs interact with isomorphisms and minor-related constructions; see [[isomorphic graphs]].
> - Important in algorithms and structural theorems about cycles, paths, and coloring; see [[path]], [[walk, trail, path, cycle]], and [[chromatic number]].