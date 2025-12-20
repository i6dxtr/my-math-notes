> [!definition]
> ### Definition 4.2.15 — $X,Y$-barrier
> For $X,Y\subseteq V(G)$, an $X,Y$-barrier is a set $Z\subseteq V(G)$ such that there are no $X,Y$-paths in $G-Z$.
> 
> Notes:
> - $X$ and $Y$ are not required to be disjoint.
> - In particular, $X$ or $Y$ themselves are $X,Y$-barriers.
> 
> Define:
> - $\lambda(X,Y)$ = the maximum number of pairwise vertex-disjoint $X,Y$-paths in $G$.
> - $\kappa(X,Y)$ = the minimum size of an $X,Y$-barrier.

> [!remark]
> By definition $\lambda(X,Y)\le\kappa(X,Y)$: each $X,Y$-path must meet a barrier, so a barrier has to contain at least one vertex from each path in a maximum family of disjoint $X,Y$-paths.

Relations
- See [[X,Y-paths and fans]] for the definition of an $X,Y$-path and fans.
- Related theorem: [[theorem - Menger local sets (Pym 1969)]] (states $\lambda(X,Y)=\kappa(X,Y)$).
- Use in connectivity statements: [[separating set, k-connectivity]] and [[ Menger-type equivalences]].
