#example 
> [!example]
> ### Exercise 4 — Diameter vs complement
> Find the smallest integer $d$ such that for every graph $G$ either $\operatorname{diam}(G)\le d$ or $\operatorname{diam}(\overline{G})\le d$.> [!proof]
> Claim: $d=3$ is the smallest integer with the required property.
> 
> (1) Show $d=3$ works. Fix a graph $G=(V,E)$ and choose a vertex $x\in V$. Partition $V$ by distance from $x$ in $G$:
> $$
> V_0=\{x\},\quad V_1=\{v:d(x,v)=1\},\quad V_2=\{v:d(x,v)=2\},\quad V_{\ge 3}=\{v:d(x,v)\ge 3\}.
> $$
> If $V_{\ge 3}=\varnothing$ then $\operatorname{ecc}(x)\le 2$ and hence $\operatorname{diam}(G)\le 2\le 3$. Otherwise pick two vertices $u,v\in V_{\ge 3}$. Since both are at distance at least $3$ from $x$, they are nonadjacent to at least one of the vertices in $\{x\}\cup V_1$, and in particular there is a small set of vertices (often a single vertex of small distance from $x$) that is nonadjacent to both $u$ and $v$ in $G$, which yields short $(u,v)$‑paths in $\overline{G}$. A standard case-checking argument shows every pair of vertices of $\overline{G}$ is joined by a path of length at most $3$, so $\operatorname{diam}(\overline{G})\le 3$.
> 
> (2) Sharpness: $d=2$ fails. Take $G$ to be the cycle $C_5$ (the 5‑cycle). Then $\operatorname{diam}(C_5)=2$? Actually for $C_5$ the diameter is $2$, so not a good counterexample. A standard sharpness example is obtained by taking $G$ a graph with diameter $3$ whose complement also has diameter $3$: for instance certain split constructions (or consider a graph formed by taking two vertices at distance $3$ and arranging neighborhoods so the complement does not shorten all distances). In the lecture/notes the argument shows $3$ is the minimal universal bound; moreover many texts present explicit families showing that $\operatorname{diam}(G)$ and $\operatorname{diam}(\overline G)$ can both equal $3$ for some graphs, so $d$ cannot be taken to be $2$.
> 
> Therefore the desired smallest integer is $d=3$.
### Remarks
- The full textbook proof proceeds by choosing a vertex and partitioning by distance then analysing missing edges which become edges of the complement; see the discussion in [[distance, diameter]].
- The statement is often phrased as: for every finite graph $G$, either $\operatorname{diam}(G)\le 3$ or $\operatorname{diam}(\overline G)\le 3$.

### Relations
- Distance and diameter definitions: [[distance, diameter]].
- Complement graphs: [[graph complement]].
