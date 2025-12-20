> [!example]
> ### Exercise 27 — Greedy coloring orderings
> 1. Prove that every graph has a vertex ordering such that the greedy coloring algorithm uses $\chi(G)$ colors with respect to the ordering. Furthermore, there exists a graph $G$ and a vertex ordering of $G$ so that the greedy coloring algorithm uses more than $\chi(G)$ colors.
> 
> 2. Let $k$ be a positive integer and let $G$ be a graph with $\chi(G)=k$. Prove that for every proper $k$-coloring of $G$ and every color $i\in[k]$, there is a vertex of color $i$ which is adjacent to at least one vertex of every other color.
> [!proof]
> Proof of (1): Let $G$ have chromatic number $k$ and fix a proper $k$-coloring $c:V(G)\to [k]$. Order the vertices by color classes: list all vertices of color 1 first, then color 2, and so on. When coloring greedily according to this ordering, every vertex in color class $i$ sees only colors in $\{1,\dots,i-1\}$ among earlier vertices, so it can be assigned a color at most $i$. Hence the greedy algorithm uses at most $k$ colors and therefore exactly $k$.
> 
> For the second part, construct a tree recursively that forces a bad ordering. (Sketch) Start with a single vertex for $k=1$. Given a tree $T_{k-1}$ where a chosen ordering causes greedy to use $k$ colors and maximum degree $k-1$, take $k-1$ copies of $T_{k-1}$, order their vertices so greedy uses $k-1$ colors on each copy, and attach a new vertex adjacent to one vertex of each copy chosen to have distinct colors; place this new vertex last in the ordering so it receives a new color $k+1$.
> 
> Proof of (2): Let $c$ be a proper $k$-coloring and for each color $i$ let $V_i=c^{-1}(\{i\})$. Suppose, towards contradiction, there is some color (say $k$) such that every vertex of color $k$ is missing a neighbor of some other color (i.e., for each $v\in V_k$ there is a color $f(v)\in[k-1]$ with no neighbor of $v$ in $V_{f(v)}$). Then one can recolor all vertices of $V_k$ using colors in $[k-1]$ (choosing a color $f(v)$ for each $v$), producing a proper $(k-1)$-coloring of $G$, contradicting $\chi(G)=k$. Therefore the claimed vertex exists for each color class.
Relations
- See [[chromatic number]] for basic chromatic definitions.
- Related: [[theorem - Mycielski construction]] (provides graphs with large chromatic number and small clique number).
- Example used in class notes: [[11-19-25]].
