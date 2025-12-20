#ch4
#### Relations
- [[Continuity]]
- [[compact sets|Compact sets]]
- [[function|Functions]]

---

> [!definition]
> A [[function]] $f:E\rightarrow \mathbb{R}$ is **Lipschitz** if $\exists c>0$ such that $\lvert f( x )-f( y ) \rvert<c\lvert x-y \rvert$ for all $x,y\in E.$ $$\lvert f( x )-f( y ) \rvert<c\lvert x-y \rvert  $$
---

> [!theorem]
> Lipschitz functions are *[[Continuity|uniformly continuous]].*
> [!proof]
> - Take $\lvert f( x )-f( y ) \rvert\le c\lvert x-y \rvert$
> - $\forall\varepsilon>0$, we can take $\delta=\frac{\varepsilon}{c}$
> - ==Remark.== $f:[0,\infty)\rightarrow \mathbb{R}$ where $f( x )=\sqrt{x}$ is uniformly continuous but *not* Lipschitz.
> [!theorem]
> If $K$ is [[compact sets|compact]] and $f:K\rightarrow \mathbb{R}$ is continuous, then it is uniformly continuous.
> [!proof]
> - Let $\varepsilon>0.$
> - For $p\in K,$ there exists $\delta_{p}>0$ such that if $x\in N_{\delta_{p}}( p )$ then $\lvert f( x )-f( p ) \rvert<\varepsilon.$
> - Take $$K\subseteq \bigcup_{p\in K}^{}N_{\delta_{p} / 2}( p )$$... an open cover
> - Since $K$ is compact, $\exists p_{1}, p_{2}, ..., p_{N}$ such that: $$K\subset \bigcup_{i=1}^{N}N_{\delta_{p_{i}}/2}( p_{i} )$$
> - Take $\delta=\text{min}\left\{ \delta_{p_{1}/2}, \delta_{p_{2} / 2}, ..., \delta_{p_{N} / 2} \right\}$
> - Let $x,y$ such that $\lvert x-y \rvert<\delta$
> - Then $x\in N_{\delta_{p_{j}} / 2}( p_{j} )$ for $j\in \left\{ 1,2,...,N \right\}$
> - We say $\lvert x-p_{j} \rvert<\delta_{p_{j} / 2}$
> - Then: $$\lvert y-p_{j} \rvert\le \lvert y-x \rvert+\lvert x-p_{j} \rvert < \delta+ \delta_{p_{j} / 2}<\delta_{p_{j}}$$
> - Therefore: $$\begin{align} \lvert f( x )-f( y ) \rvert &\le \lvert f( x )-f( p_{j} ) \rvert + \lvert f( p_{j} )-f( y ) \rvert \\&\le \frac{\varepsilon}{2}+\frac{\varepsilon}{2} \end{align}$$