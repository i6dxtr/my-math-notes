> [!example]
> ### Example — Prove Hall's theorem using Kőnig–Egerváry (Exercise 16ii)
> Prove Hall's theorem using Kőnig–Egerváry. (Contrapositive statement: If there is no matching saturating $X$, then there exists a set $S'\subseteq X$ with $\lvert N(S')\rvert < \lvert S'\rvert$.)
> [!proof]
> Let $G=(X\cup Y,E)$ be bipartite and let $M$ be a maximum matching in $G$. Suppose $M$ does not saturate $X$. Let $Q$ be a minimum vertex cover of $G$. By Kőnig–Egerváry, $\lvert Q\rvert=\lvert M\rvert$. Since $M$ does not saturate $X$ we have $\lvert M\rvert<\lvert X\rvert$.
> 
> Partition $Q$ as $Q_X=Q\cap X$ and $Q_Y=Q\cap Y$. Then
> $$\lvert Q_X\rvert+\lvert Q_Y\rvert=\lvert Q\rvert=\lvert M\rvert<\lvert X\rvert=\lvert Q_X\rvert + \lvert X\setminus Q\rvert.$$
> Hence $\lvert Q_Y\rvert < \lvert X\setminus Q\rvert$.
> 
> Because $Q$ is a vertex cover and $G$ is bipartite, every neighbor of $X\setminus Q$ lies in $Q_Y$, i.e. $N(X\setminus Q)\subseteq Q_Y$. Therefore
> $$\lvert N(X\setminus Q)\rvert \le \lvert Q_Y\rvert < \lvert X\setminus Q\rvert.$$
> Taking $S'=X\setminus Q$ produces the required subset of $X$ with strictly fewer neighbors than elements, proving the contrapositive of Hall's theorem.
Relations
- [[theorem - Hall's theorem (Theorem 3.1.11)]] — Hall's marriage theorem
- [[theorem - Cantor-Schroeder-Bernstein]] — Matching viewpoint and related constructions
- [[theorem - augmenting path characterization]] — Matching optimality and augmenting paths
- [[matching]] — Matching definitions and saturation
