> [!corollary]
> ### Erdős–Szekeres subsequence (1935)
> Let $r,s$ be non-negative integers. In every sequence of distinct real numbers of length $rs+1$, there exists an increasing subsequence of length $r+1$ or a decreasing subsequence of length $s+1$.

> [!proof]
> Label the sequence $a_1,a_2,\dots,a_{rs+1}$ and construct a tournament on these $rs+1$ elements by orienting $(a_i,a_j)$ if $a_i<a_j$. Call an oriented edge $(a_i,a_j)$ forward if $i<j$ and backward otherwise. Let $D_F$ be the digraph of forward edges and $D_B$ be that of backward edges.
> 
> A directed path of length $r$ in $D_F$ corresponds to an increasing subsequence of length $r+1$, and a directed path of length $s$ in $D_B$ corresponds to a decreasing subsequence of length $s+1$. If neither exists, by Gallai–Roy–Vitaver each of $D_F$ and $D_B$ has chromatic number at most $r$ and $s$ respectively. Since $E(T)=E(D_F)\cup E(D_B)$ partitions the tournament edges, this gives a partition of the vertex set into at most $rs$ independent sets, contradicting that the tournament has chromatic number $rs+1$. Hence one of the desired subsequences exists.
Relations
- Uses [[theorem - Gallai-Roy-Vitaver (1968)]].
- See also combinatorial applications in [[example - chromatic bound by edges]].
- 