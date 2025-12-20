#ch4
#### Relations
- [[function|Functions]]
- [[partition|Partitions]]

---

> [!definition]
> The **upper sum** for a [[partition]] $P$ is as follows: $$\mathscr{U}( \mathscr{P}, f )= \sum_{i=1}^{n}M_{i}\Delta x_{i}$$... where $M_{i}=\text{sup}\left\{ f( x ), x\in \left[ x_{i-1}, x_{i} \right] \right\}$ 
> 
> ---
> The **lower sum** for a partition $P$ is as follows: $$\mathscr{L}( \mathscr{P}, f )=\sum_{i=1}^{n}m_{i}\Delta x_{i}$$... where $m_{i}=\text{Inf}\left\{ f( x ), x\in \left[ x_{i-1}, x_{i} \right] \right\}.$
> [!remark]
> Suppose $m\le f( x )\le M$ and $x\in \left[ a,b \right].$ Then if $m\le m_{i}\le M_{i}\le M$, then $m( b-a ) \mathscr{L}( \mathscr{P}, f )\le \mathscr{U}( \mathscr{P}, f )\le M( b-a ).$
> [!definition]
> The **upper integral** is defined as follows: $$\overline{\int_{a}^{b}}f=\text{sup}\left\{ \mathscr{U}( \mathscr{P}, f ): \mathscr{P}\text{ is a partition.} \right\}$$
> 
> ---
> The **lower integral** is defined as follows: $$\underline{\int_{a}^{b}}f=\text{Inf}\left\{ \mathscr{U}( \mathscr{P}, f ) : \mathscr{P}\text{ is a partition.}\right\}$$
> [!remark]
> $$\underline{\int_{a}^{b}}f\le \overline{\int_{a}^{b}}f.$$
---

> [!corollary]
> We state that a partition $Q$ is a *refinement* of $\mathscr{P}$ if $\mathscr{P}\subset Q.$ Moreover, if $\mathscr{P}^{*}$ is a refinement of $\mathscr{P},$ then $$\mathscr{L}( \mathscr{P}, f )\le \mathscr{L}( \mathscr{P}^{*}, f )\le \mathscr{U}( \mathscr{P}^{*},f )\le \mathscr{U}( \mathscr{P}, f ).$$
> [!proof]
> - Assume that $\mathscr{P}^{*}=\mathscr{P}\cup \left\{ x^{*} \right\}.$ 
> - So $\mathscr{P}^{*}=\left\{ x_{0}, x_{1}, ..., x_{n} \right\}.$
> - Suppose there exists $k\in \left\{ 1,2,..., n \right\}$ such that $x_{k-1}<X^{*}<X_{k}$
> - Let $M_{i}=\text{sup}\left\{ f( x ):x\in \left[ x_{i-1}, x_{i} \right] \right\}.$
> - Let $$\begin{align} \mathscr{U}( \mathscr{P}^{*}, f )=&\sum_{i=1}^{k-1}M_{i}\Delta x_{i} \\ &+M_{k}'( x^{*}-x_{k-1} ) \\ &+M_{k}^{2}( x_{k}-x^{*} ) \\ &+ \sum_{i=k+1}^{n}M_{i}\Delta x_{i}. \end{align}$$... where $M_{k}'\le M_{k}$ and $M_{k}^{2}\le M_{k}.$
> - Then, $$\begin{align} \mathscr{U}( \mathscr{P}^{*}, f )&\le \sum_{i=1}^{k-1} M_{i}\Delta x_{i} \\ &+M_{k}( x^{*}-x_{k-1} )\\ &+M_{k}( x_{k}-x^{*} ) \\ &+ \sum_{i=k+1}^{n}M_{i}\Delta x_{i} &= \mathscr{U}( \mathscr{P}, f ). \end{align}$$... **qed.**