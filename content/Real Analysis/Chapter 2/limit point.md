#ch2 
##### Relations
- [[Epsilon-neighborhood]]
- [[interior point]]

---
### Limit / Isolated point 
> [!definition]
> Let $E$ be a nonempty subset of $\mathbb{R}$.
> 1. A point $p\in \mathbb{R}$ is a **limit point** of $E$ if every [[Epsilon-neighborhood|$\varepsilon-$neighborhood]] of $p$ contains a point $q\in E$ where $q\ne p$ such that $$\forall \varepsilon>0,\ ( N_{\varepsilon}( p )-\left\{ p \right\} )\cap E \ne \emptyset.$$
> 2. A point $p\in E$ is an **isolated point** of $E$ if it is not a limit point.
> [!example]
> ##### $E=(0, 1].$
> 1. $p>1$, $p$ is not a limit point
> 2. Every $p\in \left[ 0,1 \right]$ is a limit point
> 	1. $p=1$: $\varepsilon>0, ( N_{\varepsilon}( 1 )-\left\{ 1 \right\} )\cap E=( 1-\varepsilon, 1 )$
> 	2. $p=0:$ $\varepsilon>0$, $( N_{\varepsilon}( 1 ) -\left\{ 1 \right\})\cap E=( 1-\varepsilon, 1 )$
> 
> 
> ![[Pasted image 20250223155143.png]]
> 
> ---
> 
> ##### $E=\left\{ \frac{1}{n}, n\ge 1 \right\}$
> - Every element of $E$ is an isolated point
> 	- $x\in E$
> 	- $x=\frac{1}{n}$ (for some $n$)
> 	- $p$ is a limit point of $E$ $\longleftrightarrow$ $\forall\varepsilon>0$, $( N_{\varepsilon}( p )-\left\{ p \right\}\cap E\ne  \emptyset)$
> 	- $p$ is an isolated point $\longleftrightarrow$ $\exists \varepsilon>0$, $(N_{\varepsilon}( p )-\left\{ p \right\}\cap E= \emptyset)$
> 	- Let $\varepsilon=\text{min}\left\{ \left\lvert  \frac{1}{n}-\frac{1}{n+1}  \right\rvert, \left\lvert  \frac{1}{n}-\frac{1}{n-1}  \right\rvert \right\}$
> 		- so $N_{\varepsilon}\left(  \frac{1}{n}  \right)-\left\{ \frac{1}{n} \right\}\cap E = \emptyset$
> - $0$ is a limit point of $E$ 
> 	- Fix $\varepsilon$
> 	- There exists $n$ such that $\frac{1}{n}<\varepsilon$
> 	- So $\frac{1}{n}\in N_{\varepsilon}( 0 )$
> 
> ![[Pasted image 20250223155023.png]]
### Theorems
> [!theorem]
> ##### 1.) If $p$ is a limit point of a set $E$, then every neighborhood of $p$ contains infinitely many points of $E$.
> - $\forall\varepsilon>0$, $N_{\varepsilon}\cap E$ is an infinite set.
> 
> ##### 2.) If $p$ is a limit point of a set $E$, then there exists a sequence $\left\{ P_{n} \right\}$ in $E$ where $P_{n}\ne p$ and $\lim_{n \to \infty}P_{n}=p.$
> [!proof]
> ##### of 1.)
> - Assume $\exists \varepsilon>0$ where $N_{\varepsilon}( P )- P\cap E$ is a finite set
> - Let $\left\{ P_{1}, P_{2}, ..., P_{m} \right\}$ where $P_{j}\ne P$ and $j=1, ..., ,$
> 	- Observe $$S=\frac{1}{2}\text{min}\left\{ \lvert P-P_{1} \rvert, \lvert P-P_{2} \rvert, ..., \lvert P-P_{m} \rvert \right\}>0$$
> 		- Then $N_{\delta}( p )\cap E= \emptyset$
> 		- and $\forall j=1, ..., m$, 
> 		- *Contradiction:* $\lvert P-P_{j} \rvert>\delta$ but $P_{j}\not\in N_{\delta}( p )$
> 			- since $p$ is a limit point
> ##### of 2.)
> - Assume $p$ is a limit point of $E$
> - Fix $\varepsilon>0$ where $N_{\varepsilon}( p )-\left\{ p \right\}\cap E\ne \emptyset$
> 	- ie. $\exists x\in E$ where $x\ne p$ and $\lvert x-p \rvert<\varepsilon$
> - Make it countable
> 	- $\varepsilon=\frac{1}{n}$
> 	- $\exists p_{n}\in E$
> 	- $p_{n}\ne p$
> 	- $\lvert p_{n}-p \rvert<\frac{1}{n}$
> - $\left\{ P_{n} \right\}$ is a sequence in $E$, and: $$\lim_{n \to \infty}p_{n}-p=0 \longleftrightarrow \lim_{n \to \infty}p_{n}=p.$$
> [!corollary]
> A finite set has no limit point.
#### Bolzano-Weirstrass