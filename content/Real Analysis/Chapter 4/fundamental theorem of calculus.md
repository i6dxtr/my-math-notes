#ch4
> [!definition]
> Assume that $f$ has an antiderivative $F$ on $\left[ a,b \right],$ meaning $f\in R\left[ a,b \right].$ Then the following holds: $$\int_{a}^{b}f=F( b )-F( a )$$
> [!proof]
> - Let $\mathscr{P}=\left\{ x_{1}, x_{2},...,x_{n} \right\}$ be a partition of $\left[ a,b \right]$
> - Apply mean value theorem:
> 	- For $\left[ x_{i-1}, x_{i} \right]$, $\exists t_{i}\in \left[ x_{i-1}-x_{i} \right]$ such that $f( t_{i} )=F'( t_{i} )=\frac{F( x_{i} )-F( x_{i-1} )}{\Delta _{i}}$
> - So $f( t_{i} )\Delta x_{i}=F( x_{i} )-F( x_{i-1} )$
> - Moreover, $m_{i}\le f( t_{i} )\le M_{i}$
> - Furthermore, $m_{i}\Delta x_{i} \le f( t_{i} )\Delta x_{i} = F( x_{i} )-F( x_{i-1} )\le \sum_{}^{}M_{i} \Delta x_{i}$
> - implying $\mathscr{L}( \mathscr{P}, f )\le F( b )-F( a )\le \mathscr{U}( \mathscr{P}, f )$
> - thus, $F( b )-F( a )\le \overline{\int_{a}^{b}}f.$
> - Also, $\underline{\int_{a}^{b}}f\le F( b )-F( a )$