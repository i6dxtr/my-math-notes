#ch17 

> [!definition]
> Let $A$ be a [[Rings|ring]]. Some $a,b\in A$ are called **zero divisors** if $ab=0$. 
> To say "$a$ is a zero divisor" means $ab=0$ where $a\ne 0$ for some $b\ne 0$.

> [!example]
> ##### In $\mathbb{Z}_{6}$
> 1. $2$ and $3$ are zero divisors, since $2\cdot_{6}3=0$
> 2. $4$ is a zero divisor since $4\cdot_{6}3=12\text{ mod }6=0$ also.
> ##### In $M_{2}( \mathbb{R} )$
> 1. $\begin{pmatrix} 1&0\\0&0 \end{pmatrix}\cdot\begin{pmatrix} 0&0\\0&1 \end{pmatrix}=\mathbf{0}$, where each matrix is a zero divisor
> 2. In $\mathcal{P}( \left\{ 1,2,3 \right\} )$, recall:
> 	1. $A+B$ means $( A / B )\cup ( B / A )$
> 	2. $AB$ means $A\cap B$
> 	3. ... so this ring has zero divisors $\left\{ 1 \right\}$ and $\left\{ 2 \right\}$.
> 		1. $\left\{ 1 \right\}\cap\left\{ 2 \right\}=\emptyset$, the zero element.
> ##### In $\mathscr{F}( \mathbb{R} )-\left\{ f\ |\ f:\mathbb{R}\rightarrow\mathbb{R} \right\}$ with pointwise addition & multiplication
> 1. The zero element is the constant *zero function* $f$ defined by $f( 0 )=0$
> 2. This ring has zero divisors:
> 	1. Let $f( x )=\begin{cases} 0&\text{if }x<0 \\1&\text{if }x\ge0\\ \end{cases}$
> 	2. Let $g( x )=\begin{cases} 1&\text{if }x<0 \\0&\text{if }x\ge0 \end{cases}$
> 	3. Then $( fg )( x )=f( x )g( x )=\begin{cases} 0\cdot1&\text{if }x<0 \\1\cdot0&\text{if }x\ge 0 \end{cases}$
> 		1. ... $=0$ for all $x$.
> 	4. So $f,g$ are zero divisors

link [[Rings]]