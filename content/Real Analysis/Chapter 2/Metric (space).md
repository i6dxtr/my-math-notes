#ch2
### Outline
- [Metric space](#metric space)
- [Theorems](#theorems)
##### Relations
- [[Epsilon-neighborhood]]
- [[open sets]]


### Metric space
> [!definition]
> Let $X$ be a nonempty [[sets|set]]. A real valued [[function]] $d:X \times X\rightarrow \mathbb{R}$ is a **metric** if the following hold:
> 1. $d( x,y )\ge 0$, for all $x,y\in X$
> 2. $d( x,y )=0$ iff $x=y$
> 3. $d( x,y )=d( y,x )$, for all $x,y\in X$
> 4. $d( x,y )\le d( x,z )+d( z,y )$, for all $x,y,z \in X$
> ... and we call $( X, d )$ a **metric space**.
> [!example]
> $$\mathbb{R}^{2}: ( a,b )\  \&\ ( c,d )$$... see 1
> 
> $$\mathbb{R}^{2}: d^{2}=\lvert a-c \rvert +\lvert b-d \rvert $$... per the previous
> $$\mathbb{R}:d( x,y )=\lvert x-y \rvert $$... the most relevant for real analysis
### Theorems
> [!theorem]
> $$\begin{align} &( X, d )\text{ is a metric space.} \\ \\ & \ \ \ d:X \times  X\longrightarrow \mathbb{R}. \end{align}$$
> 1. $d( x,y )\ge 0$ for all $x,y\in X$
> 2. $d( x,y)=0$ iff $x=y$
> 3. $d( x,y )=d( y,x )$
> 4. $x( x,y )\le d( ,z )+d( z,y )$ for $x,y,z\in X$
> [!example]
> $$\mathbb{R}^{2}.$$
> - $x=( a,b )$
> - $y=( c,d )$
> - $d( x,y )=\sqrt{\lvert a-c \rvert^{2}+\lvert b-d \rvert^{2}}$ **qed**
> $$X=\mathbb{R}.$$
> - $d( x,y )=\lvert x-y \rvert$
> - $\lvert x-y \rvert\le\lvert x-z \rvert+\lvert z-y \rvert$
> - ==Fact.== $\lvert a+b \rvert\le \lvert a \rvert+\lvert b \rvert$
> 	- $a=x-z$
> 	- $b=z-y$
> 	- ... implies $\lvert a+b \rvert=x-y$