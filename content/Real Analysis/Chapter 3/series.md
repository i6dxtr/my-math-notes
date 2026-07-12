#ch3 
> [!theorem]
> ### Theorem: Cauchy Criteria
> The series $\sum_{k=1}^{\infty}a_{k}$ converges *if and only if* $\forall\varepsilon>0\ \exists n_{0}$ such that $$\left\lvert \sum_{k=n+1}^{m}a_{k} \right\rvert <\varepsilon$$... for all $m>n\ge n_{0}$.

> [!corollary]
> If a series $\sum_{k=1}^{\infty}a_{k}$ is [[Convergent sequence|convergent]], then $$\lim_{k \to \infty}a_{k}=0.$$

> [!proof]
> - $\forall\varepsilon>0\ \exists n_{0}$ such that for $m>n\ge n_{0}$, $\left\lvert  \sum_{k=n+1}^{m}a_{k}  \right\rvert<\varepsilon$
> - Take $m=n+1$ so $\lvert a_{n+1}<\varepsilon \rvert.$