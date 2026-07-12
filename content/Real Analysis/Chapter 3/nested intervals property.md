#ch2 
### Outline
- [Nested intervals property](#Nested intervals property)
##### Relations
- [[Sequence]]
- [[Monotone sequence]]
- [[Convergent sequence]]

---

### Nested intervals property
> [!corollary]
> ##### Nested Intervals Property
> If $\left\{ I_{n} \right\}$ is a sequence of closed and bounded intervals with $I_{2}\subset I_{1}, I_{3}\subset I _{2}, \cdots$, then the following is true: $$\bigcap_{m=1}^{\infty}I_{n}\neq \emptyset.$$

> [!proof]
> $$I_{n}=\left[ a_{n}, b_{n} \right]$$
> 	- fg3
> - $\left\{ a_{n} \right\}$ is *monotone increasing*
> 	- $a_{n}\le b_{2}$ for all $n\ge 2$
> 	- $a_{n}\le b_{m}$ for all $n\ge m$
> - Since $\left\{ a_{n} \right\}$ is monotone increasing and bounded, it is *convergent*.
> 	- Let $a=\lim_{n \to \infty}a_{n}$
> 	- ==recall.== $a=\text{sup}\left\{ a_{n}, n\ge 1 \right\}$ where $b_{m}$ is an upper bound of $\left\{ a_{n}, n\ge 1 \right\}$
> 	- So $a\le b_{m}$, 
> 		- Implying $a\in I_{m}$ for all $m\ge 1$
> 	- So $a\in \bigcap_{m=1}^{\infty}I_{m}$ **qed**

> [!remark]
> $$1.)\ I_{n}=\left(  0, \frac{1}{n}  \right]\text{ is not closed.}$$
> - $I_{n+1}\subset I_{n}$
> - $\bigcup_{m=1}^{\infty}I_{n}=\emptyset$
> 
> $$2.)\ I_{n}=[ n, \infty )\text{ is closed.}$$
> - $I_{n+2}\subset I_{n}$
> - $\bigcap_{m=1}^{\infty}I_{n}=\emptyset$