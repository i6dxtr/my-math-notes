#ch2 
### Outline
- Bolzano-Weirstrass Theorem
##### Relations
- [[Epsilon-neighborhood]]
- [[interior point]]
- [[Convergent sequence]]
- [[subsequence]]

### Bolzano-Weirstrass Theorem
> [!theorem]
> ##### *Bolzano-Weirstrass theorem:*
> Every [[bound|bounded]] infinite subset of $\mathbb{R}$ has a limit point.
> [!proof]
> - Let $S$ be a bounded infinite set.
> 	- Since $S$ is bounded, $S\subset\left[ a, b \right]$ for some $-\infty < a < b < \infty$.
> 	- Let $I_{1}=\left[ a,b \right]$
> 	- So $S\subset (S\cap \left[ a_{1} , \frac{a+b}{2}\right]\cup S\cap \left[ \frac{a+b}{2}, b \right])$
> - Since $S$ is infinite, one of these two sets is also infinite
> 	- Call the infinite half $I_{2}$
> 	- So $I_{2}\subset I_{1}$ where $\lvert I_{2} \rvert<\frac{b-a}{2}$
> - Inductively, construct intervals
> 	- $\cdots I_{3}\subset I_{2}\subset I_{1}$
> 	- $S\cap I_{n}$ is infinite
> 	- $\lvert I_{n} \rvert\le \frac{b-a}{2n-1}$
> - We now have $\bigcap_{n=1}^{\infty}I_{n}\ne \emptyset$
> - Let $p\in \bigcap_{n=1}^{\infty}I_{n}$
> - We verify $p$ is a limit point of $S$
> 	- Let $\varepsilon > 0$
> 	- Since $\lim_{n \to \infty}\frac{b-a}{2^{n-1}}=0$, there exists $n_{0}$ such that $$n\ge n_{0}\longrightarrow \frac{b-a}{2^{n-1}}<\varepsilon$$
> 	- Let $x\in I_{n}$ where $\lvert p-x \rvert<\frac{b-a}{2^{n-1}}$
> 	- So $x\in N_{\varepsilon}( p )$
> 	- Therefore $I_{n} \subseteq N_{\varepsilon}( p )$
> 		- $\longrightarrow I_{n} \cap (S \subseteq ( N_{\varepsilon}( p )\cap S ) )$
> 		- $N_{\varepsilon}( p )\cap S$ contains (infinitely many) points $S$ different from $p$
> - Thus, $p$ is a limit point of $s$. **qed**
> [!corollary]
> Every [[bound|bounded]] [[sequence]] has a [[Convergent sequence|convergent]] [[subsequence]].
> [!proof]
> - Let $\left\{ p_{n} \right\}$ be a bounded sequence in $\mathbb{R}$
> - Let $E=\left\{ p_{n}:n\ge 1 \right\}$
> - Assume $E$ is infinite
> - By the previous theorem, $E$ has limit points
> - Let $p$ be a limit point of $E$
> 	- $\varepsilon>0\longrightarrow ( N_{\varepsilon}( p )-\left\{ p \right\} )\cap E$ is infinite.
> 	- $\varepsilon=1\longrightarrow\exists p_{n_1} \in E \cap N_{1}( p )\left\{ p \right\}$.
> 	- $\varepsilon=\frac{1}{2}\longrightarrow \exists p_{n_{2}}$ ... $\left(  N_{\frac{1}{2}}( p )-\left\{ p \right\}  \right)\cap ( E - \left\{ p_{1}, p_{2}, ..., p_{n_{1}} \right\} )$
> 		- $n_{2}>n_{1}$
> 	- $\varepsilon=\frac{1}{k}\longrightarrow \exists p_{n_{k}}\in \left(  N_{\frac{1}{k}}( p - \left\{ p \right\}\cap E )  \right)-\left\{ p_{1}, p_{2}, ..., p_{n_{k-1}} \right\}$
> - So $\left\{ p_{n_{k}} \right\}$ is a subsequence and $\lvert p_{n_{k}}-p \rvert<\frac{1}{k}$. $$\lim_{k \to \infty}p_{n_{k}}=p.$$**qed**