#ch2 
#### Outline
- [Open sets](#Open sets)
	- [Ch4 Definition](#Ch4 Definition)
- [Closed sets](#Closed sets)
- [Theorems](#Theorems)
##### Relations
- [[interior point]]
- [[Metric (space)]]
- [[Index Family of Subsets]]
---
### Open sets
> [!definition]
> A subset $\vartheta$ of $X$ is an **open set** if every $x\in \vartheta$ is an [[interior point]] of $\vartheta$.
> 
> ![[Pasted image 20250223154214.png]]
> [!example]
> - Open intervals are open sets of $\mathbb{R}$
> - For $x\in ( a,b )$:
> 	- Take $\varepsilon=\text{min}\left\{ \lvert x-a \rvert, \lvert x-b \rvert \right\}$
> 	- So $N_{\varepsilon}( x )\subseteq ( a,b )$
### Closed sets
> [!definition]
> A subset $F\subseteq X$ is called **closed** if $X-F$ is *open*.
> [!example]
> ##### $F=\left[ a,b \right]\longrightarrow R - \left[ a,b \right]=( -\infty, a )\cup ( b, \infty )$
> - Fix $x\in \mathbb{R}-\left[ a,b \right]$
> - Either $x\in ( -\infty, a )$ or $x\in ( b,\infty )$.
> 	- If $x\in ( -\infty, a )$
> 		- For $\varepsilon=\lvert x-a \rvert \longrightarrow N_{\varepsilon}( x )\subset ( -\infty, a )$
> 		- $y\in N_{\varepsilon}( x )\longrightarrow \lvert x-y \rvert<\varepsilon = \lvert x-a \rvert$
> 	- If $x\in ( b, \infty )$
> 		- Take $\varepsilon=\lvert x-b \rvert$
> 		- Then $N_{\varepsilon}( x )\subset( b, \infty )$
> 
> ![[Pasted image 20250223154214.png]]
> [!example]
> ##### $E=( 1,2 ]$ is *not* open.
> - $2$ is not an interior point of $E$
> ##### $R - E=(-\infty, 1]\cup (2,\infty)$ is *not* open.
> - $1$ is not an interior point of $\mathbb{R} - E$
> ##### $E$ is *not* closed.
### Theorems
> [!theorem]
> Let $( X, d )$ be a [[Metric (space)|metric space]].
> 1. For any collection $\left(  O_{\alpha}  \right)_{\alpha\in A}$ of *open subsets* of $X$, $$\bigcup_{\alpha\in  A}^{}O_{\alpha}\text{ is open.}$$
> 2. For a finite collection $O_{1}, O_{2}, ..., O_{n}$ of open subsets of $X$, $$O_{1}\cap O_{2} \cap \cdots \cap O_{n}\text{ is open.}$$
> [!proof]
> ##### $\bigcup_{\alpha\in A}^{}O_{\alpha}$ is open
> - Let $x\in \bigcup_{\alpha\in A}^{}O_{\alpha}$
> - There exists $\alpha_{0}\in A$ such that $x\in O_{\alpha_{0}}$
> - $O_{\alpha_{0}}$ is open (given)
> - So there exists $\varepsilon>0$ such that $$N_{\varepsilon}( x )\subset O_{\alpha_{0}}\longrightarrow N_{\varepsilon}( x )\subset\bigcup_{\alpha\in A}^{}O_{\alpha}.$$
> ##### $O_{1}\cap O_{2} \cap \cdots \cap O_{n}$ is open.
> - Let $x\in O_{1} \cap O_{2} \cap \cdots \cap O_{N}$
> - For every $1\le j\le N$, $x\in O_{j}$
> - For a given $1\le J \le N$, there exists $\varepsilon_{j}>0$ such that $N_{\varepsilon_{j}}( x )\subset O_{j}$
> 	- $\varepsilon=\text{min}\left\{ \varepsilon_{1}, \varepsilon_{2}, ..., \varepsilon_{N} \right\}$
> 	- $N_{\varepsilon}( x )\subset N_{\varepsilon_{j}}( x )\subset O_{j}$
> 	- $\longrightarrow N_{\varepsilon}( x )\subset O_{1} \cap O_{2} \cap \cdots \cap O_{n}$
> - $X$ is an interior: $O_{1} \cap O_{2} \cap \cdots \cap O_{N}$.
> [!example]
> - $O_{n}=\left(  -\frac{1}{n}, \frac{1}{n}  \right)$ is open.
> - $\bigcap_{n=1}^{\infty}O_{n}=\left\{ O \right\}$ is *not* open.
> [!theorem]
> 1. If $\left\{ C_{\alpha} \right\}_{\alpha\in A}$ is a collection of closed sets, then $\bigcap_{\alpha\in A}^{}C_{\alpha}$ is closed.
> 2. If $c_{1}, c_{2}, ..., c_{N}$ are closed, then $c_{1}\cup c_{2}\cup \cdots\cup c_{N}$ is closed.
> [!proof]
> - Let $C=\bigcap_{\alpha\in A}^{}C_{\alpha}$
> - Then $X-C=\bigcup_{\alpha\in A}^{}( X - C_{\alpha} )$ where $X-C_{\alpha}$ is open
> 	- $\longrightarrow$ $X - C$ is open
> 		- $\longleftrightarrow$ $C$ is closed.
### Ch4 Definition
> [!definition]
> Let $E\subseteq \mathbb{R}$. A subset of $E$ is *open in $E$* if $\forall x\in E\ \ \exists\delta>0$ such that: $$N_{\delta}( x )\cap E\subseteq E.$$
> [!example]
> Let $E=[0,1)$ and $U=[0, \frac{1}{2})$.
> $U$ is open in $E$.
> 
> ---
> 
> If $V=E\cap \mathbb{Q}$ and $r\in E\cap \mathbb{Q}$
> $\mathbb{Q}$ is not open in $E$.