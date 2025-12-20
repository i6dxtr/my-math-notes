> [!theorem]
> ### Theorem (Min-degree implies connectivity vs independence)
> Let $G$ be a graph on $n\ge 2$ vertices. If $\delta(G)\ge \dfrac{n}{2}$ then $\kappa(G)\ge\alpha(G)$.
> [!proof]
> If $G$ is complete then $\kappa(G)=n-1\ge 1=\alpha(G)$, so the claim holds. Assume $G$ is not complete.
> 
> Let $S$ be a minimum vertex cut of $G$, so $|S|=\kappa(G)$. Let $I$ be a maximum independent set with $|I|=\alpha(G)$ and suppose, for contradiction, that
> $$\alpha(G)>\kappa(G)=|S|. $$
> Partition $V(G)$ as $V_1\cup V_2\cup S$ where every path from $V_1$ to $V_2$ meets $S$. Let
> $$a_1=|V_1\cap I|,\quad a_2=|V_2\cap I|,\quad b=|I\cap S|.$$
> Since $|I|>|S|$ we have $a_1>0$ or $a_2>0$; without loss of generality $a_1>0$. Pick $x\in V_1\cap I$.
> 
> If there exists $y\in V_2\cap I$ then every neighbor of $x$ lies in $V_1\cup S$ but cannot be in $I\cap V_1$, so
> $$d(x)\le |V_1|-a_1+|S|-b.$$ Similarly,
> $$d(y)\le |V_2|-a_2+|S|-b.$$ Adding these gives
> \begin{align*}
>  n &\le d(x)+d(y) \\
>    &\le (|V_1|-a_1+|S|-b)+(|V_2|-a_2+|S|-b) \\
>    &= |V_1|+|V_2|+2|S|-(a_1+a_2+b) \\
>    &= n+|S|-|I| \\
>    &< n,
> \end{align*}
> a contradiction.
> 
> If $V_2\cap I=\varnothing$, pick any $y\in V_2$. Then
> $$d(x)\le |V_1|-a_1+|S|-b,\qquad d(y)\le |V_2|-1+|S|,$$
> and hence
> \begin{align*}
>  n &\le d(x)+d(y) \\
>    &\le (|V_1|-a_1+|S|-b)+(|V_2|-1+|S|) \\
>    &= n+|S|-|I|-1 \\
>    &< n,
> \end{align*}
> again a contradiction. Therefore $\alpha(G)\le\kappa(G)$, as required.
Relations
- See [[separating set, k-connectivity]] for definitions of $\kappa(G)$ and vertex cuts.
- Related: [[content/theorems, lemma/theorem - Chvátal-Erdős Hamiltonicity condition.md]] (uses $\kappa(G)\ge\alpha(G)$ as a hypothesis).
- See [[content/foundational/independent set.md]] for the independence number $\alpha(G)$.
