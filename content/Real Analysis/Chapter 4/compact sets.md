#ch4 
#### Relations
- [[open cover]]
- [[open sets]]

---
> [!definition]
> A subset $K$ of $\mathbb{R}$ is called **compact** if every open cover of $k$ has a finite subcover.
> 
> Let $( O_{\alpha} )_{\alpha\in A}$ be an [[open cover]] of $k$ where $$K\subseteq \bigcup _{\alpha\in  A}O_{\alpha}$$... then $\exists \alpha_{1}, \alpha_{2}, \cdots, \alpha_{N}\in A$ such that: $$K\subseteq O_{\alpha}\cup O_{\alpha_{2}}\cup\cdots\cup O_{\alpha}.$$
> [!example]
> 1. Finite sets are compact
> 2. $( 0,1 )$ is *not* compact
> 	1. $O_{n}=\left(  0, 1-\frac{1}{n}  \right)$
> 	2. $( 0,1 )\subseteq \bigcup_{n=2}^{\infty}O_{n}$
> 	3. $O_{n_{1}}\cdots O_{n_{N}}$
> 	4. $n=\text{max}\left\{ n_{1},\cdots,n_{N} \right\}$
> 	5. $\bigcup_{n=1}^{\infty} O_{N}=\left(  0, 1-\frac{1}{n}  \right)$
> [!theorem]
> Every compact set is *closed.*
> [!proof]
> 1. Assume that $k$ is compact.
> 2. We will show that $\mathbb{R} - K$ is open.
> 3. Let $p\in \mathbb{R} - K.$
> 4. For each $x\in K$, take $\varepsilon_{x}>0$ such that $N_{\varepsilon_{x}}( x )\cap N_{\varepsilon_{x}}( p )\ne \emptyset.$
> 5. Then $$\left\{ N_{\varepsilon_{x}}( x ) \right\}_{x\in  K}\text{ is an open cover for }K.$$
> 6. $K$ is compact, so there exists $x_{1}, ..., x_{m}$ such that $$K\subseteq N_{\varepsilon_{x_{1}}}( x_{1} )\cup N_{\varepsilon_{x_{2}}}( x_{2} )\cup\cdots\cup N_{\varepsilon_{x_{m}}}( x_{m} ).$$
> 7. Suppose $\varepsilon=\text{min}\left\{ \varepsilon_{x_{1}}, ..., \varepsilon_{x_{m}} \right\}>0.$
> 8. Recall that $N_{\varepsilon_{j}}( x_{j} )\cap N_{\varepsilon_{j}}( p )=0.$
> 9. This implies $N_{\varepsilon_{j}}( x_{j} )\cap N_{\varepsilon}( p )\ne \emptyset.$ ie. $(N_{\varepsilon_{x_{1}}}( x_{1} )\cup N_{\varepsilon_{x_{2}}}( x_{2} )\cup\cdots\cup N_{\varepsilon_{x_{m}}}( x_{m} ))\cap N_{\varepsilon}( p )\ne \emptyset.$
> 10. So $K\cap N_{\varepsilon}( p )=\emptyset$
> 11. ie. $N_{\varepsilon}( p )\subseteq \mathbb{R} - K$.
> 12. So $p$ is an interior point of $\mathbb{R} - K.$
> 13. Thus, $\mathbb{R}-K$ is open.