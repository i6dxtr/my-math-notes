#ch4
#### Relations
- [[function|Functions]]
- [[Monotone sequence]]

---

> [!definition]
> 1. $f$ is **monotone increasing** if $f( x )\le f( y )$ for all $x,y\in I$ where $x<y.$
> 2. $f$ is **monotone decreasing** if $f( x )\le f( y )$ for all $x,y\in I$ where $y<x.$
---

> [!theorem]
> If a [[function]] $f:I\rightarrow \mathbb{R}$ is [[monotone increasing]], then $f( p^{+} )$ and $f( p^{-} )$ exist, and the following holds:
> $$
> \begin{align} \text{sup}_{x<p}f( x )&=f( p^{-} ) \\ &\le f( p ) \\ &\le f( p^{+} ) &=\text{Inf}_{x>p}f( x ). \end{align}
> $$

> [!theorem]
> If a function $f:I\rightarrow \mathbb{R}$ is monotone, then the set of [[Discontinuity|discontinuities]] is *at most [[cardinality|countable]].*

> [!proof]
> - Assume that $f$ is monotone increasing.
> - For $p\in E,$ $f( p^{-} )<f( p^{+} ).$
> - For $p\in E,$ fix $r_{p}\in \mathbb{Q}$ such that $f( p^{-} )< r_{p}<f( p^{+} ).$
> - Note that $p\ne q\longrightarrow r_{p}\ne r_{q}.$
> - Let $\varphi:E\rightarrow \mathbb{Q}$ be a one-to-one function as $p\rightarrow r_{p}.$
> - We can then say $\varphi( E )$ is equivalent to $E.$
> - Since $\varphi( E )$ is countable, $E$ is also countable. **qed**