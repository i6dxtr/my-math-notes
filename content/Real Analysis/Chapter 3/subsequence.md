#ch2 
### Outline
- [[subsequence]]
- [Subsequential limit](#Subsequential limit)
- [Theorems](#Theorems)
##### Relations
- [[Sequence]]
- [[Convergent sequence]]
- [[infinite limits]]


--- 

### Subsequence
> [!definition]
> Given a [[sequence]] $\left\{ P_{n} \right\}$ in $\mathbb{R}$, consider a sequence of integers where $m_{1}< n_{2} < n_3<\cdots$
> The sequence $\left\{ P_{n_{j}} \right\}_{j=1}^{\infty}$ is a **subsequence** of $\left\{ P_{n} \right\}$. 
> ![[Pasted image 20250219153904.png]]

> [!example]
> $$a_{n}=( -1 )^{n} $$
> - $\left\{ a_{4k} \right\}_{k=1}^{\infty}$ is a *subsequence*
> - $a_{4k}=1$
### Subsequential limit
> [!definition]
> Let $\left\{ P_{n} \right\}$ be a sequence. $\alpha$ is a **subsequential limit** of $\left\{ P_{n} \right\}$ if there is a *subsequence* of $\left\{ P_{n} \right\}$ whose limit is $\alpha$.
### Theorems
> [!theorem]
> If $\left\{ P_{n} \right\}$ converges to $p$, then every subsequence of $\left\{ P_{n} \right\}$ converges to the same limit $p$.

> [!proof]
> - Assume $\lim_{n \to \infty}P_{n}=P$
> - Let $P_{n_{j}}$ be a subsequence of $\left\{ P_{n} \right\}$
> 	- $n_{1}<n_{2}<n_{3}<\cdots< n_{j}<n_{j+1}<\cdots$
> - Let $\varepsilon>0$
> 	- Then $\exists N\in \mathbb{N}$ such that $\forall n\ge N$, $P_{n}\in N_{\varepsilon}( P )$.
> - $N\in \mathbb{N}$
> ![[Pasted image 20250219153446.png]]
> $$\lim_{j \to \infty}P_{n_{j}}=p.$$...**qed**

> [!example]
> $$0<p<1\ \longrightarrow\ \lim_{n \to \infty}p^{n}=0.$$
> - $\left\{ P^{2n} \right\}_{n=1}^{\infty}$ is a subsequence of $\left\{ P^{n} \right\}$
> 	- $\left\{ P_{n} \right\}$ is monotone decreasing & bounded
> 	- So the limit exists
> 	- Say $\alpha=\lim_{n \to \infty}p^{n}$
> - $\alpha=\lim_{n \to \infty}P^{2n}=\lim_{n \to \infty}P^{n}$
> - $P^{n}=( \lim_{n \to \infty}P^{n} )\cdot( \lim_{n \to \infty}P^{n} )$
> 	- $=\alpha^{2}$
> 	- $\longrightarrow \alpha=\alpha^{2}$
> 	- $\longrightarrow \alpha=0$.