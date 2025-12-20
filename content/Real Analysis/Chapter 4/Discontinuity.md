#ch4
#### Relations
- [[function|Functions]]
- [[function limits|Function limits]]
- [[Continuity]]
- [[limit point|Limit points]]

---

> [!definition]
> Let $f:E\rightarrow \mathbb{R}$ where $E\subset\mathbb{R}$ & let $p$ be a [[limit point]] of $E\cap ( p, \infty ).$ The [[function]] $f$ has a **right limit** at $p$ if there exists $L\in \mathbb{R}$ such that$$\begin{gathered} \forall \varepsilon>0, \exists \delta>0 \\ \text{for which} \\ \lvert f( x )-L \rvert <\varepsilon\end{gathered}$$... *for all $x\in E$ where $p<x<p+\delta.$*
> For a **left limit**, instead take the limit point $p$ of $E\cap ( -\infty, p ).$
> 
> ---
> - **Right Limit:** $( x>p )$ $$f( p^{+} )=\lim_{x \to p^{+}}f( x )=\lim_{x \to p}f( x ).$$
> - **Left Limit:** $( x<p )$ $$f( p^{-} )=\lim_{x \to p^{-}}f( x )=\lim_{x \to p}f( x ).$$
---
#### Types of discontinuities
Let $f:I\rightarrow \mathbb{R}$ where $I$ is some interval.
1. If $a<p<b:$
	1. $f$ has a *jump discontinuity* at $p$ *if and only if* $f( p^{+} )$ and $f( p^{-} )$ exist, but $f$ is *not* continuous.
2. If $p=a$ :
3. $f$ is a *jump discontinuity* if: $$f( p^{+} )\ne f( p )$$... for some $p=b.$
> [!remark]
> Jump discontinuities can be referred to as a *discontinuity of the first kind.* 
> 
> ---
> We can express a *removeable discontinuity* as follows: $$f( p^{+} )=f( p^{-} )\ne f( p ).$$