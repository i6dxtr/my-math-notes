#ch3 
#### Relations
- [[Sequence|Sequences]]
- [[Cauchy sequences]]
- [[Convergent sequence|Convergent sequences]]
- [[series|Series]]
---
#### Contractive Sequences
> [!definition]
> A [[sequence]] $( a_{n} )$ is **contractive** if there exists a number $b$ where $0<b<1$ such that $$\lvert a_{n+1}-a_{n} \rvert \le b\lvert a_{n}-a_{n-1} \rvert .$$
> [!example]
> ##### $\begin{cases} a_{1}=2\\ a_{2}=1 \\ \end{cases}$ : $a_{n}=\frac{1}{2}( a_{n-1}+a_{n-2} )$ where $n\ge 3$.
> - $a_{3}=\frac{1}{2}( 2+1 )=\frac{3}{2}$
> - $a_{4}=\frac{1}{2}\left(  \frac{3}{2}+1  \right)=\frac{1}{2}\left(  \frac{5}{2}  \right)=\frac{5}{4}, \cdots$
> *Proof it's contractive:*
> $$\begin{align} \lvert a_{n+1}-a_{n} \rvert&=\left\lvert  \frac{1}{2}( a_{n}+a_{n-1} )  -a_{n}\right\rvert    \\&=\left\lvert  \frac{1}{2}( a_{n-1}-a_{n} )  \right\rvert\\&=\frac{1}{2}\lvert a_{n}-a_{n-1} \rvert. \end{align}$$
#### Theorems
> [!corollary]
> ##### Contractive sequences are convergent.
> [!proof]
> - We show that a contractive sequence $a_{n}$ is Cauchy
> - Pick $m,n$ with $m>m$.
> 	- say, $m=n+k$
> - $( a_{n} )$ is contractive, so $\lvert a_{n+1}-a_{n} \rvert\le b\lvert a_{n}-a_{n+1} \rvert$
> - take $$\begin{align} \lvert a_{n+k}-a_{n} \rvert&=\lvert a_{n+k} -a_{n+k-1}+( a_{n+k-1}-a_{n+k-2} )+( a_{n+k-2}-a_{n+k-3} )+\cdots+( a_{n+1}-a_{n} )\rvert \\ &\le \lvert a_{n+k}-a_{n+k-1} \rvert +\lvert a_{n+k-1} \rvert +\cdots+ \lvert a_{n+1}-a_{n} \rvert  \end{align}$$
> - fix $k$ such that: $$ \begin{align} \lvert a_{k+1}-a_{k} \rvert&\le b\lvert a_{k}-a_{k-1}\lvert\\ &\le b^{2} \lvert a_{k-1}-a_{k-2} \rvert \\ &\le b^{3}\lvert a_{k-2}-a_{k-3} \rvert \\ &\le \cdots \\ &\le b^{k}\lvert a_{2}-a_{1} \rvert \\ \lvert a_{n+k}-a_{n} \rvert &\le b^{n+k-2}\lvert a_{2}-a_{1} \rvert + b^{n+k-3}\lvert a_{2}-a_{1} \rvert +\cdots+ b^{n-1}\lvert a_{2}-a_{1} \rvert \\ &= ( b^{n+k-2}+b^{n+k-3}+\cdots+b^{n-1} )\lvert a_{2}-a_{1} \rvert \\ &=b^{n-1}( b^{k-1}+b^{k-1}+\cdots+1 )\lvert a_{2}-a_{1} \rvert \\ &= b^{n-1}\left(  \frac{1-b^{k}}{1-b}  \right)\le \frac{b^{n-1}}{1-b} \end{align}$$
> - Following, $$\begin{align} \lvert a_{n+k}-a_{n} \rvert\le \frac{b^{n-1}}{1-b} \\ \lim_{n \to \infty}b^{n-1}=0\ \  \end{align}$$
> 	- $\exists n_{0}\in\mathbb{N}$ if $n\ge n_{0}$ then $b^{n-1}<\frac{\varepsilon( 1-b )}{\lvert a_{2}-a_{1} \rvert}$
> 	- implying $\forall n,m \ge n_{0}, \lvert a_{m}-a_{n} \rvert<\varepsilon$
> [!remark]
> ##### Proving $( a_{n} )$ is not Cauchy
> If a series is not Cauchy, it is equivalent to state the following:$$\exists \varepsilon>0\  \forall n_{0}\ \exists n,m\ge n_{0}\Longrightarrow\lvert a_{n}-a_{m} \rvert\ge \varepsilon.$$
> [!example]
> ##### $( s_{n} )=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}$.
> - $( s_{n} )$ is not Cauchy:
> 	- $\begin{align} \lvert s_{m}-s_{n} \rvert&=\frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{m} \\ &\ge \frac{1}{m}( \text{number of terms} ) \end{align}$
> 	- Take $m=2n$, then: $$\begin{align} \lvert s_{2n}-s_{n} \rvert &\ge \frac{1}{2n}( n ) \\&= \frac{1}{2} \end{align}$$... so where $\varepsilon>0$, $\forall n_{0}$, $n\ge n_{0}$, $$\lvert s_{2n}-s_{n} \rvert \ge \frac{1}{2}.$$