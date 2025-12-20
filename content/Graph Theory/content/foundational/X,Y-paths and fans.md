> [!definition]
> ### Definition — $X,Y$‑paths and $x$‑$Y$ fans
> Let $G$ be a graph and let $X,Y\subseteq V(G)$ be (not necessarily disjoint) vertex sets.
> 
> - An $X,Y$‑path is a path $P$ with one endpoint in $X$ and the other endpoint in $Y$ such that
>   $$
>   \lvert V(P)\cap X\rvert = 1 = \lvert V(P)\cap Y\rvert.
>   $$
>   In other words, $P$ meets $X$ and $Y$ exactly at its endpoints.
> 
> - Given a vertex $x\in V(G)$ and a set $Y\subseteq V(G)\setminus\{x\}$, an $x$‑$Y$‑fan is a collection of paths
>   $$
>   \mathcal{F}=\{P_1,P_2,\dots,P_k\}
>   $$
>   such that
>   1. each $P_i$ has one endpoint $x$ and the other endpoint in $Y$,
>   2. for every $i\neq j$ we have
>      $$
>      \bigl(V(P_i)\setminus\{x\}\bigr)\cap\bigl(V(P_j)\setminus\{x\}\bigr)=\varnothing,
>      $$
>      i.e. the paths are internally disjoint except for the common endpoint $x$,
>   3. each path meets $Y$ in exactly one vertex.
> 
> When $|\mathcal{F}|=k$ we say there is an $x$‑$Y$ fan of size $k$.

> [!remark]
> Fans are a convenient way to package multiple internally disjoint paths from a single root to a target set; they appear in statements equivalent to $k$‑connectivity (Menger / Mängel type theorems).

### Examples
- A simple example: in a tree rooted at $x$, the collection of root‑to‑leaf paths to distinct leaves forms an $x$‑$Y$ fan.
- In a $k$‑connected graph, for any vertex $x$ and any $Y\subseteq V(G)\setminus\{x\}$ with $|Y|\ge k$, there exists an $x$‑$Y$ fan of size $k$ (this is one of the equivalent formulations of connectivity used in lecture notes).

### Relations
- [[ Menger-type equivalences]] — Fans are used in one of the equivalent statements in Menger/Mängel theorems.
- [[theorem - 2-connected via internally disjoint paths]] — The fan notion generalizes the two internally disjoint paths condition to a rooted setting.
- [[internally disjoint paths]] — Internal disjointness is the key constraint in fan definitions.

