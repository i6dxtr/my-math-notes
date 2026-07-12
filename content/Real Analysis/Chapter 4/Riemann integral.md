#ch4
#### Relations
- [[function|Functions]]
- [[partition|Partitions]]
- [[Upper & lower integrals]]
- [[Continuity]]
---

> [!definition]
> Let $f:\left[ a,b \right]\rightarrow \mathbb{R}$ be a bounded [[function]]. If $\underline{\int_{a}^{b}}f=\overline{\int_{a}^{b}}f,$ then $f$ is said to be **Riemann integrable.** In this case, the integral of $f$ is:$$\int_{a}^{b}f=\underline{\int _{a}^{b}}f=\overline{\int_{a}^{b}}f.$$
> We say $R\left[ a,b \right]$ is the set of all Riemann integrable functions.
---
#### Criterion for Integrality
> [!theorem]
> A function $f$ is **integrable** ($f\in R[a,b]$) *if and only if* $\forall\varepsilon>0$ there exists a [[partition]] $\mathscr{P}$ such that $$\mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P}, f )<\varepsilon.$$

> [!proof]
> $( \Longrightarrow )$
> - Assume that $f$ is integrable.
> - For $\varepsilon>0,$ there exists a partition $\mathscr{P}_{1}$ such that $$\mathscr{U}( \mathscr{P}, f )\le \int_{a}^{b}f+\frac{\varepsilon}{2}$$
> - Moreover, $\exists \mathscr{P}_{2}$ such that $$\int_{a}^{b}f-\frac{\varepsilon}{2}\le \mathscr{L}( \mathscr{P}_{2}, f )$$
> - Let $\mathscr{P}=\mathscr{P}_{1}\cup \mathscr{P}_{2}$
> - So
> 	$$
> 	\begin{align} \mathscr{U}( \mathscr{P}, f )&\le \mathscr{U}( \mathscr{P}_{1}, f ) \\ &\le \int_{a}^{b} f+\frac{\varepsilon}{2}\\ &\le \mathscr{L}( \mathscr{P}_{2}, f )+ \frac{\varepsilon}{2}+ \frac{\varepsilon}{2} \\&\le \mathscr{P}( \mathscr{P}, f )+\varepsilon. \end{align}
> 	$$
> $( \Longleftarrow )$
> - Assume that $\varepsilon>0.$
> - Then $\mathscr{U}( \mathscr{P}_{3}, f )\le \mathscr{L}( \mathscr{P}_{\varepsilon}, f )+\varepsilon.$
> 	- the first term on RHS is smaller than $\underline{\int_{a}^{b}}f$
> - Therefore, $\mathscr{U}( \mathscr{P}, f )\le \underline{\int_{a}^{b}}f+\varepsilon$
> 	- LHS larger than $\overline{\int_{a}^{b}}f$
> - Implying $\overline{\int_{a}^{b}}f\le \underline{\int_{a}^{b}}f+\varepsilon$
> - Since $\varepsilon$ is arbitrary, $\overline{\int_{a}^{b}}f \le \underline{\int_{a}^{b}}f$
> - Thus, $\overline{\int_{a}^{b}}f=\underline{\int_{a}^{b}}f.$ **qed**

> [!theorem]
> Let $f:\left[ a,b \right]\rightarrow \mathbb{R}$ be a bounded function.
> 1. If $f$ is [[Continuity|continuous]], then $f\in R\left[ a,b \right].$
> 2. If $f$ is [[Monotone function|monotone]], then $f\in R\left[ a,b \right].$

> [!proof]
> ##### of 1.
> - Since $\left[ a,b \right]$ is [[compact sets|compact]], $f$ is uniformly continuous.
> 	- $\forall\varepsilon>0, \exists \delta$ st. $s,t\in \left[ a,b \right]\longrightarrow \lvert f( s )-f( t ) \rvert<\varepsilon$
> - Fix a partition $\mathscr{P}=\left\{ x_{0}, x_{1}, ..., x_{n} \right\}$ st. $\Delta x_{i}<\delta.$
> - Suppose $M_{i}=\text{sup}\left\{ f( t ), t\in \left[ x_{i-1}, x_{i} \right] \right\}$ and $m_{i}=\text{Inf}\left\{ f( t ), t\in \left[ x_{i-1}, x_{i} \right] \right\}.$
> - So $M_{i}-m_{i}=f( c_{i} )-f( d_{i} ).$
> 	- $f( c_{i} )$ the absolute max, other term absolute min
> 	- we know $c_{i}, d_{i}\in \left[ x_{i-1}, x_{i} \right]$
> - Since $\Delta x_{i}<\delta,$ $\lvert c_{i}-d_{i} \rvert<\delta.$
> - Therefore $M_{i}-m_{i}<\varepsilon.$
> - Observe the upper sum:
> 	$$
> 	\begin{align} \mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P}, f )&=\sum_{i=1}^{n}( M_{i}-m_{i} )\Delta x_{i}& \\ &<\sum_{i=1}^{n}\varepsilon\Delta x_{i}... &=\varepsilon( b-a ) \\ \mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P},f ) &<\varepsilon( b-1 )... &=\varepsilon \end{align}
> 	$$
> - implying $f\in R\left[ a,b \right]$
> 
> ##### of 2.
> - Assume $f$ is monotone increasing
> - Suppose $\varepsilon>0,$ then $\mathscr{P}=\left\{ x_{0}, x_{1},...,x_{n} \right\}$
> - Limits:
> 	$$
> 	\begin{align} \mathscr{U}( \mathscr{P}, f )&= \sum_{i-1}^{n}f( x_{i} )\Delta x_{i} \\ \mathscr{L}( \mathscr{P}, f )&= \sum_{i-1}^{n}f( x_{i-1} )\Delta x_{i} \\ \mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P},f )&= \sum_{i=1}^{n}( f(  x_{i}) )-f( x_{i-1} ) )\Delta x_{i} \end{align}
> 	$$
> - Choose $\mathscr{P}$ such that $\Delta x_{i}=\frac{b-a}{n}$:
> 	$$
> 	\begin{align} \mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P},f )&=\frac{b-a}{n}\sum_{i=1}^{n}f( x_{i} )-f( x_{i-1} ) \\ &=  \frac{b-a}{n}( f( b )-f( a ) ). \end{align}
> 	$$
> - Choose $n$ such that $\frac{b-a}{n}( f( b )-f( a ))<\varepsilon.$

> [!theorem]
> Suppose $f:\left[ a,b \right]$ is integrable, and $\text{range}f \subset \left[ c,d \right].$ If $\varphi$ is continuous at $\left[  c,d \right]$, then $\varphi o f\in R( \left[ a,b \right] ).$

> [!proof]
> - Let $\varepsilon>0.$
> - $\varphi$ is uniformly continuous on $\left[ c,d \right]$
> - For $\varepsilon'$, $\exists \delta$ and $t,s \in \left[ c,d \right]$ such that $$\lvert t-s \rvert<\delta\longrightarrow\lvert \varphi( t )-\varphi ( s ) \rvert<\varepsilon.$$
> - For $\delta>0, \exists \mathscr{P}$ such that $$\mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P}, f ) < \delta^{2}$$
> - We want to estimate $$\mathscr{U}( \mathscr{P}, fof )-\mathscr{L}( \mathscr{P}, f o \varphi )$$
> - Let $\mathscr{P}=\left\{ x_{0}, x_{1}, ..., x_{n} \right\}$ be a partition
> - Take the following:
> 	- $M_{i}=\text{sup}\left\{ f( t ):t\in \left[ x_{i-1}, x_{i} \right] \right\}$
> 	- $m_{i}=\text{Inf}\left\{ f( t ):t\in \left[ x_{i-1}, x_{i} \right] \right\}$
> 	- $M_{i}^{*}=\text{sup}\left\{ \varphi( t ):t\in \left[ x_{i-1}, x_{i} \right] \right\}$
> 	- $m_{i}^{*}=\text{Inf}\left\{ \varphi( t ):t\in \left[ x_{i-1}, x_{i} \right] \right\}$
> - Then $$\sum_{i=1}^{n}( M_{i}^{*}-m_{i}^{*} )\Delta x_{i}\ \ ?$$
> - So $A=\left\{ i: M_{i}-m_{i}<\delta \right\}$
> - Also, $B=\left\{ i:M_{i}-m_{i}\ge \delta \right\}.$
> - For any $i\in A$, $\forall t, s\in \left[ x_{i-1}, x_{i} \right], \lvert f( t )-f( s ) \rvert<\delta$
> - So $\lvert \varphi( f( t ) )-\varphi ( f( s ) ) \rvert<\varepsilon$
> - So
> 	$$
> 	\begin{align} M_{i}^{*}-m_{i}^{*}&\le \text{sup}\left\{ \lvert \varphi o f( t )-\varphi o f( s ) \rvert : s,t \in \left[ x_{i-1}, x_{i} \right] \right\}\\&<\varepsilon. \end{align}
> 	$$
> - So
> 	$$
> 	\begin{align} \mathscr{U}( \mathscr{P}, \varphi o f )-\mathscr{L}( \mathscr{P}, \varphi o f )&=\sum_{i\in  A}^{}( M_{i}^{*}-m_{i}^{*} )\Delta x_{i}+\sum_{i\in  B}^{}( M_{i}^{*}-m_{i}^{*} )\Delta x_{i} \\ &\le \varepsilon'( b-a ) + \left[ M_{i}^{*}\le k ; m_{i}^{*}\le k \right] \end{align}
> 	$$
> 	... where $k$ is the maximum of $\lvert \varphi \rvert$ in $\left[ c, d \right]$
> - Note that for $i\in B$, $M_{i}-m_{i}\ge \delta\longrightarrow \frac{M_{i}-m_{i}}{\delta}\ge 1$
> 	- $\le \varepsilon'( b-a )+\frac{2k}{\delta}\sum_{i\in B}^{}( M_{i}-m_{i} )\Delta x_{i}$
> 	- $\le\varepsilon'( b-a )+\frac{2k}{\delta}\sum_{i=1}^{m}( M_{i}-m_{i} )\Delta$
> 	- $\le \varepsilon'( b-a )+\frac{2k}{\delta}\left[ \mathscr{U}( \mathscr{P}, f )-\mathscr{L}( \mathscr{P}, f ) \right].$
> 	- $\le \varepsilon'( b-a )+2k\delta$
> 	- $\le \varepsilon'(  b-a )+2k\varepsilon'$
> 	- $= \varepsilon.$

> [!corollary]
> The following hold for some integrable functions $f, g$
> 1. $f+g\in R[a,b]$ with $\int_{a}^{b} f+g=\int_{a}^{b}f+\int_{a}^{b}g$
> 2. $cf\in R[a,b], c\int_{a}^{b}f=\int_{a}^{b}cf$
> 3. $fg\in R\left[ a,b \right]$

> [!proof]
> ##### of 1.
> $\mathscr{P}$ is a partition:
> - $M_{i}( f )=\text{sup}\left\{ f( + ):t\in \left[ x_{i-1}, x_{i} \right] \right\}$
> - $M_{i}( g )=\text{sup}\left\{ g( t ):t\in \left[ x_{i-1}, x_{i} \right] \right\}$
> - See $f( t )+g( t )\le M_{i}( f )+M_{i}( g )$ for all $t\in \left[ x_{i-1}, x_{i} \right]$
> - implies $\text{sup}\left\{ f( t )+g( t ):t\in \left[ x_{i-1}, x_{i} \right] \right\}\le M_{i}( f )+M_{i}( g )$
> 	- so $\mathscr{U}( \mathscr{P}, f+g )\le \mathscr{U}( \mathscr{P}, f )+\mathscr{U}( \mathscr{P}, g )$
> - so $\overline{\int_{a}^{b}}f+g\le \mathscr{U}( \mathscr{P}, f )+\mathscr{U}( \mathscr{P}, g )$
> 	- true $\forall \mathscr{P}$
> - for $f,$ $\exists \mathscr{P}_{f}$ for which $\mathscr{U}( \mathscr{P}_{f}, f )\le \int_{a}^{b}f+\varepsilon$
> - for $g,$ $\exists \mathscr{P}_{g}$ for which $\mathscr{U}( \mathscr{P}_{f}, g )\le \int_{a}^{b}g+\varepsilon$
> - take $Q=\mathscr{P}_{f}\cup \mathscr{P}_{g},$
> 	- then $\mathscr{U}( \mathscr{Q}, f )\le \mathscr{U}( \mathscr{P}_{f}, f )\le \int_{a}^{b}f+\varepsilon$
> 	- moreover, $\mathscr{U}( \mathscr{Q}, f )\le \mathscr{U}( \mathscr{P}_{g}, f )\le \int_{a}^{b}g+\varepsilon$
> - implying $\overline{\int_{a}^{b}}f+g\le \mathscr{U}( \mathscr{Q}, f )+\mathscr{U}( \mathscr{Q}, g )\le \int_{a}^{b}f+\int_{a}^{b}q+2\varepsilon$
> - since $\varepsilon$ is arbitrary, $$\overline{\int_{a}^{b}}f+g\le \int_{a}^{b}f+\int_{a}^{b}g$$
> - repeat the proof to get $$\int_{a}^{b}f+\underline{\int_{a}}^{b}g\le \underline{\int_{a}^{b}}$$
> - conclusion: $$\overline{\int_{a}^{b}}f+g\le \int_{a}^{b}f+\int_{a}^{b}g\le \underline{\int_{a}^{b}}f+g$$
> 
> ---
> 
> ##### of 2.
> - if $\mathscr{P}$ is a partition, take two cases
> 	- if $c>0$
> 		- then $cM_{i}( f )=M_{i}( cf )$
> 		- moreover, $c\mathscr{U}( \mathscr{P}, f )=\mathscr{U}( \mathscr{P}, cf )$
> 	- if $c<0$
> 		- then $cM_{i}( f )=m_{i}( cf )$
> 		- moreover, $c\mathscr{U}( \mathscr{P}, f )=\mathscr{L}( \mathscr{P}, cf )$
> ###### of 3.
> - observe:
> 	- $f+g\in R\left[ a,b \right]\longrightarrow ( f+g )^{2}\in R\left[ a, b \right]$
> 	- $f-g\in R\left[ a, b \right]\longrightarrow ( f-g )^{2}\in R\left[ a, b \right]$
> - so $( f+g )^{2}-( f-g )^{2}=4fg\in R\left[ a,b \right]$

> [!theorem]
> Let $a<c<b.$ Assume $f\in R\left[ a, c \right]$ and $f\in R\left[ c,b \right].$ If $f$ is integrable on $\left[ a,b \right],$ then the following holds: $$\int_{a}^{b}f=\int_{a}^{c}f+\int_{c}^bf$$

> [!proof]
> ###### case 1.
> - Let $\mathscr{P}$ be a partition of $\left[ a,b \right]$ with $c\in \mathscr{P}.$
> - Let $\mathscr{P}_{1}=\left\{ x_{i}\in \mathscr{P}, x_{i}\le c \right\}$ and $\mathscr{P}_{2}=\left\{ x_{i}\in \mathscr{P}, c\le x_{i} \right\}$
> - $\mathscr{P}_{1}$ is a partition of $\left[ a, c \right]$ and $\mathscr{P}_{2}$ is a partition of $\left[ c, b \right]$
> 	- therefore $\mathscr{U}( \mathscr{P}, f )=\mathscr{U}( \mathscr{P}_{1}, f )+\mathscr{U}( \mathscr{P}_{2}, f )$
> 	- furthermore, $\mathscr{U}( \mathscr{P}, f )\ge \int_{a}^{c}f+\int_{c}^{b}f.$
> - for lower sum:
> 	- $\int_{a}^{c}f+\int_{c}^{b}f\ge \mathscr{L}( \mathscr{P}, f )$
> - if $c\in \mathscr{P}$ 
> 	- then $\mathscr{L}( \mathscr{P}, f )\le \int_{a}^{c}f+\int_{c}^{b}f\le \mathscr{U}( \mathscr{P}, f )$
> - if $c\notin \mathscr{P}$
> 	- take $Q=\mathscr{p}\cup \left\{ c \right\}$
> 	- then $\mathscr{L}( \mathscr{P}, f )\le \mathscr{L}( \mathscr{Q}, f )\le \int_{a}^{c}f+\int_{c}^{b}f\le \mathscr{U}( \mathscr{Q}, f )\le \mathscr{U}( \mathscr{P}, f )$
> 	- implying $\forall \mathscr{P},$ $\mathscr{L}( \mathscr{P}, f )\le \int_{a}^{c}f+\int_{c}^{b}f\le \mathscr{U}( \mathscr{P}, f )$
> 	- furthermore, $\underline{\int_{a}^{b}}f\le \int_{a}^{c}f+\int_{c}^{b}f\le \overline{\int_{a}^{b}}f$
> 
> integrability (?)
> - Fix $\mathscr{P}_{1}$ such that $\mathscr{U}( \mathscr{P}_{1}, f )\le \int_{a}^{c}f+\varepsilon$
> - Fix $\mathscr{P_{2}}$ such that $\mathscr{U}( \mathscr{P}_{2}, f )\le \int_{c}^{b}f+\varepsilon$
> - let $Q=\mathscr{P}_{1}\cup\mathscr{P_{2}}$
> - then $\mathscr{U}( \mathscr{P}, f )=\mathscr{U}( \mathscr{P}_{1}, f )+\mathscr{U}( \mathscr{P}_{2}, f )$
> - moreover, $.$
> - therefore $\overline{\int_{a}^{b}}f$
> - ==theres more==
---

> [!example]
> $$f( x )=\begin{cases} 0&\text{if }x\in  \mathbb{Q}\cap\left[ a,b \right] \\  1&\text{if }x\in  \left[ a,b \right]-\mathbb{Q}. \end{cases}$$
> - If $\mathscr{P}$ is a partition of $\left[ a,b \right],$ then:
> 	1. $\mathscr{L}( \mathscr{P}, f )=0$
> 	2. $\mathscr{U}( \mathscr{P}, f )=( b-a )$
> - Hence, $\underline{\int_{a}^{b}}f=0$ and $\overline{\int_{a}^{b}}f=( b-a ).$
> - Moreover, $f\notin R\left[ a,b \right].$
> 
> ---
> $$f( x )=\begin{cases} 0&\text{where }0\le x\le \frac{1}{2} \\ 1&\text{where }\frac{1}{2}\le x<1.  \end{cases}$$
> - $\mathscr{L}( \mathscr{P}, f )=\sum_{i=1}^{k-1}m_{i}\Delta x_{i} + m_{k}\Delta x_{k}+ \sum_{i=k+1}^{M}m_{i}\Delta x_{i}$
> 	- first term collapses to $0$
> 	- second term collapses to $1-x_{k}\le \frac{1}{2}$
> - $\mathscr{U}( \mathscr{P}, f )=\sum_{i=1}^{k-1}m_{i}\Delta x_{i}+1\Delta x_{k}+\cdots$
> 	- first term collapses to $0$
> 	- second term collapses to $1-x_{k-1}\ge \frac{1}{2}$
> - Thus, $$\underline{\int_{0}^{1}}f\le \frac{1}{2}\le \overline{\int _{0}^{1}}f.$$
> ---
> $$\mathscr{U}( \mathscr{P}, f )=\mathscr{L}( \mathscr{P}, f )+ ( x_{k}-x_{k-1} ).$$
> - Let $\varepsilon>0$
> - If $\Delta x_{i}<\varepsilon,$ then
> 	$$
> 	\begin{align} \overline{\int_{0}^{1}}f&\le \mathscr{U}( \mathscr{P}, f )\\ &\le \mathscr{L}( \mathscr{P}, f )+\varepsilon \\ &\le \underline{\int_{0}^{1}}f+\varepsilon \\ \longrightarrow \overline{\int_{0}^{1}}f&\le \underline{\int_{0}^{1}}f+\varepsilon \\ \longrightarrow \overline{\int_{0}^{1}}f &\le \underline{\int_{0}^{1}}f. \end{align}
> 	$$