#foundational #definition 
> [!definition]
> ### Definition: Graph Complement
> Given a [[graph]] $G = (V, E)$, the **complement** of $G$ is the graph
> $$\overline{G} = \bigl(V,\; \tbinom{V}{2}\setminus E\bigr).$$
> Equivalently, for distinct vertices $u,v\in V$,
> $$uv\in E(\overline{G}) \iff uv\notin E(G).$$

> [!example]
> ![[Pasted image 20250827135230.png|400]]

### Relations
- Complements preserve the same [[order, size|order]] but alter the [[order, size|size]].
- Independent sets in $G$ correspond to cliques in $\overline{G}$ (see [[independent set|independent set]] and [[clique|clique]]).
- Useful when proving structural statements by switching to $\overline{G}$ (e.g., bounds involving independence or clique numbers).
- Appears in exercises such as diameter vs complement and complement-connectivity arguments.
- Complement arguments are sometimes used alongside connectivity and Hamiltonicity remarks (see [[distance, diameter|distance, diameter]], [[theorem - minimum degree & path-cycle length|theorem - minimum degree & path-cycle length]], [[lemma - odd walk contains odd cycle|lemma - odd walk contains odd cycle]]).
