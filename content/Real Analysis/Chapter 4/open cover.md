#ch4 
##### Relations
- [[open sets]]
- [[compact sets]]

---
> [!definition]
> Let $E$ be a subset of $\mathbb{R}$. An **open cover** of $E$ is a family of [[open sets|open subsets]] of $\mathbb{R}$. $$\left\{ O_{\alpha} \right\}_{\alpha\in  A}\text{ where } E\subseteq \bigcup _{\alpha\in  A}O_{\alpha}$$

> [!example]
> $E=( 0,1 )$
> $O_{1}=\left(  -1,\frac{1}{2}  \right)$
> $O_{2}=\frac{1}{4}, \frac{3}{4}$
> $O_{3}=\left(  \frac{1}{2},1  \right)$
> 1. $O_{1}\cup O_{2}\cup O_{3}=( -1,1 )$
> 2. $E\subseteq O_{1}\cup O_{2}\cup O_{3}$
> 
> ---
> 
> $E=( 0,1 )$
> $O_{n}=\left(  -1, 1-\frac{1}{n}  \right)$
> 1. $( 0,1 )\subseteq \bigcup _{n=2}^{\infty}O_{n}$ 
> 2. $\left\{ O_{n} \right\}_{n=2}^{\infty}$ is an open cover for $( 0,1 )$
> 
> ---
> 
> $E=[1,\infty)$
> $O_{r}=( 0,r )$ where $r>1$
> 1. $\left\{ O_{r} \right\}_{r\in ( 1, \infty )}$
> 2. $E\subset \bigcup _{r\in ( 1, \infty )}O_{r}$