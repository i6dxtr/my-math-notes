#ch2 
### Outline
- [Monotone sequences](#Monotone sequences)
- [Theorems](#Theorems)
##### Relations
- [[Sequence]]
- [[nested intervals property]]
- [[Convergent sequence]]

### Monotone sequences
> [!definition]
> A sequence $\left\{ a_{n} \right\}$ is **monotone increasing** if $$a_{n}\le a_{n+1}$$... for all $n\in \mathbb{N}$.
> 
> ---
> 
> A sequence $\left\{ a_{n} \right\}$ is **monotone decreasing** if $$a_{n}\ge a_{n+1}$$... for all $n\in \mathbb{N}$.
### Theorems
> [!theorem]
> If $\left\{ a_{n} \right\}$ is monotone and [[bound|bounded]], then it is [[Convergent sequence|convergent]].

> [!proof]
> - Assume that $\left\{ a_{n} \right\}$ is *monotone increasing* and *bounded*.
> - The set $E=\left\{ a_{n}: n\in \mathbb{N} \right\}$ is bounded.
> - Let $s=\text{sup }E$
> - We show $\lim_{n \to \infty}a_{n}=s$
> 	- fg2
> 	- Let $\varepsilon > 0$
> 	- There exists $x\in E$ with $s-\varepsilon < x \le s$
> 	- Since $x\in E$, there exists $n_{0}$ such that $x=a_{n_{0}}$. $$s-\varepsilon < a_{n_{0}}$$
> 	- $\left\{ a_{n} \right\}$ is increasing
> 		- So for $n\ge n_{0}$, $a_{n_{0}}\le a_{n}$
> 		- Implying $s-\varepsilon < a_{n}\le s$
> 		- Implying $a_{n}\in N_{\varepsilon}( S )$. **qed**
> 			- ie. $\lim_{n \to \infty}a_{n}=s$