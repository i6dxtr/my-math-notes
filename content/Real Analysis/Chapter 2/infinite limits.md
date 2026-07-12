#ch2
### Outline
- [Infinite limits](#Infinite limits)
##### Relations
- [[Convergent sequence]]
- [[Monotone sequence]]
- [[subsequence]]
---

### Infinite limits
> [!definition]
> If $\left\{ a_{n} \right\}$ is [[Monotone sequence|monotone increasing]] and not [[bound|bounded above]], then $$\lim_{n \to \infty}a_{n}=\infty.$$

> [!proof]
> - Let $E=\left\{ a_{n}:n\ge 1 \right\}$
> - We say $E$ is *not* bounded above.
> - Fix $M>0$
> - Since $E$ not bounded above, there exists $x\in E$ s.t. $M<x$
> - Then there exists $n_{0}$ such that $x=a_{n_{0}}$
> 	- since $\left\{ a_{n} \right\}$ is monotone increasing
> - If $n\ge n_{0}$ then $a_{n}\ge a_{n_{0}}\ge M$. **qed**