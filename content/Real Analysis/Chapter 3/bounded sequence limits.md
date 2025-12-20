#ch3
### Outline
- [Preface](#Preface)
- [Limit Superior / Inferior](#Limit Superior / Inferior)
##### Relations
- [[Sequence]]
- [[Epsilon-neighborhood|Limit]]
- 

#### Preface
Let $( s_{n} )_{n\ge 1}$ be a sequence in $\mathbb{R}$. Then, for $k\ge 1$, $$\begin{align} a_{k}&=\text{inf}\left\{ s_{n}:n\ge k \right\} \\ b_{k}&=\text{sup}\left\{ s_{n}:n\ge k \right\} \end{align}.$$ Suppose there's some sequence $E_{k}:$ $$E_{k}=\left\{ s_{n}:n\ge k \right\}=\left\{ s_{k}, s_{k+1}, s_{k+2}, \cdots \right\}$$... where $E_{k+1}\subseteq E_{k}\longrightarrow a_{k}\le a_{k+1}$.
**Why?**
- Take $a_{k}=\text{inf}E_{k}$
- Then $\forall x\in E_{x}, a_{k}\le x$
- Since $E_{k+1}\subseteq E_{k}$, it must be true that $a_{k}$ is a lower bound of $E_{k+1}$.
- Thus, $$a_{k}\le \text{inf }E_{k+1}=a_{k+1}.$$
---
### Limit Superior / Inferior
> [!definition]
> The **limit inferior** of $( S_{n} )_{n\ge 1}$ is given as $$\varliminf_{k \to \infty}a_{k}=\lim_{k \to \infty}\text{Inf}\left\{ s_{n}, n\ge k \right\}.$$
> - notation: $\lim_{n \to \infty}s_{n}$
> ---
> The **limit superior** of $( S_{n} )_{n\ge 1}$ is $$\overline{\lim_{k \to \infty}}b_{k}=\lim_{k \to \infty}\text{sup}\left\{ s_{n}, n\ge k \right\}.$$
> - notation: $\lim_{k \to \infty}s_{n}$ 
> 
> ---
> [!example]
> ##### 1.) $x_{n}=( -1 )^{n}.$
> - $E_{1}=\left\{ x_{1}, x_{2}, \cdots \right\}=\left\{ -1,1 \right\}$
> - $a_{1}=\text{inf}E_{1}=-1$
> - $E_{2}=\left\{ x_{2}, x_{3}, \cdots \right\}=\left\{ -1,1 \right\}$
> - $a_{2}=-1$
> - $\forall k\ge 1$, $a_{k}=-1$
> - $b_{k}=\text{sup }E_{k}=1$
> - $\longrightarrow \varliminf_{n \to \infty}( -1 )^{n}=-1$ and $\overline{\lim_{n \to \infty}}( -1 )^{n}=1$
> 
> ---
> ##### 2.) $s_{n}=\left\{ n( 1+( -1 )^{n} ) \right\}_{n\ge 1}.$
> - $s_{n}=\begin{cases} 0&&\text{if }n\text{ odd} \\ 2n&&\text{if }n\text{ even.}\end{cases}$
> - $a_{10}=\text{Inf}\left\{ 20, 0, 24, 0, 28 \right\}$
> 	- $=0$
> - $a_{11}=\text{Inf}\left\{ 0, 24, \cdots \right\}$
> 	- $=0$
> - $\lim_{n \to \infty} s_{n}=\lim_{k \to \infty}a_{k}=0.$
> - $b_{10}=\left\{ 20, 0, 24, 0, 28, 0,32,\cdots \right\}$
> 	- $=\infty$
> - so $\lim_{n \to \infty}s_{n}=\infty$
> 
> ---
> ##### 3.) $s_{n}=( -1 )^{n}+\frac{1}{n}$
> - $k$ is even: $E_{k}=\left\{ 1+\frac{1}{k}, -1+\frac{1}{k+1}, 1+\frac{1}{k+2},-1+\frac{1}{k+3} \right\}$
> - $a_{k}=-1$
> 	- $\lim_{n \to \infty}s_{n}=-1$ (up)
> - $b_{k}=1+\frac{1}{k}$
> 	- $\lim_{n \to \infty}s_{n}=1$ (ud)
> [!remark]
> If $( s_{n} )_{n\ge 1}$ is a sequence in $\mathbb{R}$, then the following is true: $$\varliminf_{n \to \infty}s_{n}\le \overline{\lim_{n \to \infty}}s_{n}$$
> [!theorem]
> Let $( s_{n} )$ be a sequence in $\mathbb{R}$.
> 1. Suppose $\overline{\lim_{n \to \infty}}(s_{n})\in \mathbb{R}$
> 2. Then $\beta=\overline{\lim_{n \to \infty}}(s_{n})$ if and only if $\forall\varepsilon>0,$
> 	1. $\exists n_{0}$ such that for $n\ge n_{0}$, $$s_{n}<\beta+\varepsilon.$$
> 	2. Given $n\in \mathbb{N}$, $\exists k\ge n$ such that $$\beta-\varepsilon<s_{k.}$$
> 3. $\overline{\lim_{n \to \infty}}(s_{n})=\infty$ *iff* given $M>0$ and $n\in \mathbb{N}$, there exists a $k\ge n$ such that $S_{k}>M$.
> 4. $\overline{\lim_{n \to \infty}}(s_{n})=\infty$ *iff* $s_{n}\longrightarrow -\infty$
==fig 1==

> [!proof]
> - Let $\beta=\overline{\lim_{n \to \infty}}( s_{n} )$
> - Fix $\varepsilon>0$
> - Then $\exists n_{0}$ such that $\forall n\ge n_{0}$, $\beta-\varepsilon<b_{n}<\beta+\varepsilon$
> 	- but $s_{n}\le b_{n}$,
> 		- implying $s_{n}<\beta+\varepsilon$
> - take $n\ge n_{0}$
> 	- so $\beta-\varepsilon<b_{n}$
> 	- $\beta-\varepsilon$ cannot be an upper bound of $E_{m}=\left\{ s_{n}, s_{n}+1, \cdots \right\}$
> 	- so $\exists x\in E_{n}$ with $\beta-\varepsilon<x<b_{n}$
> [!theorem]
> Let $( s_{n} )_{n\ge 1}$ be a sequence in $\mathbb{R}$.
> 1. Suppose $\alpha=\varliminf_{n \to \infty}( s_{n} )$ *iff* $\forall \varepsilon>0,$ there exists $n_{0}\in \mathbb{N}$ such that for all $n\ge n_{0}$, $$\alpha-\varepsilon<s_{n}$$
> 2. Given $n\in\mathbb{N}$, there exists a $k\ge n$ such that $s_{k}<\alpha+\varepsilon$
> 3. Then $\varliminf_{n \to \infty}( s_{n} )=\infty \longleftrightarrow s_{n}\rightarrow \infty$
> 4. $\varliminf_{n \to \infty}( s_{n} )=-\infty$ $\longleftrightarrow$ given $M<0$ and $n\in \mathbb{N}$, there exists $k\ge n$ such that $s_{k}\le M$.
> [!corollary]
> $$\begin{align} \lim_{n \to \infty}s_{n}\text{ exists}\ \longleftrightarrow \overline{\lim}_{n \to \infty}s_n \end{align}=\varliminf_{n \to \infty}s_{n}$$
> [!theorem]
> $$\begin{align} \varliminf_{n \to \infty}\alpha_{n}+\varliminf_{n \to \infty}\beta_{n}&\le \varliminf_{n \to \infty}( \alpha_{n}+\beta_{n} ) \\ &\le \varliminf_{n \to \infty}\alpha_{n}+\overline{\lim}_{n \to \infty}\beta_{n} \\ &\le \overline{\lim}_{n \to \infty}\alpha_{n} + \overline{\lim}_{n \to \infty}\beta_{n}. \end{align}$$
> [!proof]
> - Let $\alpha_{k}=\text{Inf}\left\{ a_{n}, n\ge k \right\}$
> - Let $\beta_{k}=\text{Inf}\left\{ b_{n}, n\ge k \right\}$
> - Fix $n\ge k$ such that:
> 	- $\alpha_{k}\le a_{n}$
> 	- $\beta_{k}\le b_{n}$
> 	- $\alpha_{k}+\beta_{k}\le a_{n}+b_{n}$
> - $\alpha_{k}+\beta_{k}$ is a lower bound for $\left\{ a_{n}+b_{n}, n\ge k \right\}$: $$\alpha_{k}+\beta_{k}\le \text{Inf}\left\{ a_{n}+b_{n}, n\ge 1 \right\}$$
> - Take limits: $$\begin{align} \lim_{k \to \infty}( \alpha_{k}+\beta_{k} )&\le \varliminf_{n \to \infty}( a_{n}+b_{n} ) \\ &= \lim_{k \to \infty}\alpha_{k}+\lim_{k \to \infty}\beta_{k} \\ &= \varliminf_{n \to \infty}a_{n}+\varliminf b_{n} .\end{align}$$... **qed**
> [!example]
> $$\begin{align} a_{n}=( -1 )^{n} &&\varliminf_{n \to \infty}a_{n}=-1 && a_{n}+b_{n}=0 \\ b_{n}=( -1 )^{n+1} && \varliminf_{n \to \infty}b_{n}=-1 \end{align}$$
> [!theorem]
> Let $( s_{n} )$ be a sequence of real numbers and let $E$ be a set equal to all subsequential limits of $( s_{n} )$ in $\mathbb{R}\cup \left\{ -\infty, \infty \right\}$. Then $\varliminf_{n \to \infty}s_{n}$ and $\overline{\lim_{n \to \infty}}s_{n}$ are in $E$ and the following hold: 
> 1. $\varliminf_{n \to \infty}s_{n}=\text{Inf }E$
> 2. $\overline{\lim_{n \to \infty}}s_{n}=\text{sup }E$
> [!proof]
> - Let $\beta=\overline{\lim_{n \to \infty}}s_{n}$
> - Assume $\beta\in \mathbb{R}$.
> - WTS some sequence converges to $\beta$
> 	- Take $m=N$
> 	- Then $\exists n_{1}\ge N$ st. $\beta-1<s_{n_{1}}$, so $$\beta-1<s_{n_{1}}<\beta+1$$
> 	- Suppose that $n_{1}<n_{2}<\cdots<n_{k}$ with $$\beta-\frac{1}{j}<s_{n_{j}}<\beta+\frac{1}{j}$$... where $j=1, ..., k$
> 	- Let $\varepsilon=\frac{1}{k+1}$
> 	- Then $\exists N_{k+1}$ such that $\forall n\ge N_{k+1}$, $$s_{n}<\beta+\frac{1}{k+1}$$
> 	- where $m=\text{max}( N_{k+1}, n_{k}+1 )$, $\exists n_{k+1}\ge m$, with $$\beta-\frac{1}{k+1}<s_{n_{k+1}}<\beta+\frac{1}{k+1}$$
> - The sequence $( s_{n_{j}} )_{j\ge 1}$ satisfies $$\beta-\frac{1}{j}<s_{n_{j}}<\beta+\frac{1}{j}$$.. $\forall j\ge 1$
> 	- Implying $\lim_{j \to \infty}s_{n_{j}}=\beta$.
> 
> ##### Proving $\beta=\text{sup }E$
> - By definition, $\beta\le \text{sup }E$
> - Assume $\beta<\text{sup }E$
> - Then $\exists e\in E$ with $\beta<e\le \text{sup }E$
> - So there exists a subsequence $( s_{k_{j}} )_{j\ge 1}$ that converges to $e$
> 	- $b_{k}=\text{sup}\left\{ s_{n}, n\ge k \right\}$
> 	- $b_{k_{j}}=\text{sup}\left\{ s_{n}, n\ge k_{j} \right\}$ ... $\ge s_{k_{j}}$
> 	- contradiction: $b_{k_{j}}\rightarrow\beta$, $s_{k_{j}}\rightarrow e$