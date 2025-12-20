#ch1 
#### Outline/Relations
- [[positive real numbers|Positive Real Numbers]]
- [[bound|Bounds]]
- **Least Upper Bound (supremum)**
- [[Archimedean property|Archimedean Property]]
- **Theorems**
- **Perturbation Strategy**

==recall==: $\mathbb{Q}$ and $\mathbb{R}$ are [[Fields]]
### Least Upper Bound
> [!definition]
> Let $E$ be a non-empty subset of $\mathbb{R}$. Given some $x\in \mathbb{R}$, we call $x$ a **least upper bound** (supremum of $E$) if the following hold:
> 1. $x$ is an upper [[bound]] of $E$
> 2. If $\beta \in \mathbb{R}$ satisfies $\beta < x$, then $\beta$ *is not* an upper bound of $E$.
> 3. ==Notation==: $x=\text{sup }E$
> [!remark]
> - Every non-empty subset of $\mathbb{R}$ that is bounded above *must have a supremum.*
> - Conversely, every non-empty subset of $\mathbb{R}$ that is bounded below *must have an infimum.*
> [!corollary]
> 4. If $E$ is *not* bounded above, then $\text{sup }E=\infty$
> 5. If $E$ is *not* bounded below, then $\text{inf }E=-\infty$
- This theorem derives the [[Archimedean property]].

> [!theorem]
> Let $A$ be a nonempty subset of $\mathbb{R}$ that is bounded above. An upper bound $\alpha$ of $A$ is the supremum of $A$ *if and only if* for every $\beta<\alpha$, there exists an element $x\in A$ such that: $$\beta<x\le \alpha.$$
> [!example]
> ##### Proving existence of a least upper bound
> ![[Pasted image 20250216003055.png]]
### Perturbation
Strategy:
1. Create expression $\beta$ as a small positive adjustment to $\alpha$ for contradiction
2. Term $\frac{y-\alpha^{2}}{\alpha+y}$ a controlled way of doing this
	1. Ensures $\beta>\alpha$
	2. Helps contradiction
	3. Easy algebraic manipulation
> [!example]
> ##### Prove $\forall y>0, y\in \mathbb{R}$, $\exists \alpha\in \mathbb{R}$ s.t. $\alpha^{2}=y$
> $$\begin{align} \text{Given }y>1, \text{ define }C:&&C&=\left\{ x\in  \mathbb{R}: x>0\text{ and }x^{2}<y \right\} \\ \text{Let }\alpha=\text{sup }C\text{, and define }\beta:&& \beta&= \alpha+\left(  \frac{y-\alpha^{2}}{\alpha+y}  \right) = \frac{y( \alpha+1 )}{\alpha+y} \\ \text{Then}:&&\beta^{2}-y&=\frac{y( y-1 )( \alpha^{2}-y )}{( \alpha+y )^{2}} \end{align}$$... now observe:
> - If $\alpha^{2}<y$, then:
> 	- $\beta>\alpha$
> 	- $\beta^{2}<y$
> 	- which contradicts $\alpha$ being an upper bound of $C$.
> - If $\alpha^{2}>y$, then:
> 	- $\beta<\alpha$
> 	- $\beta^{2}>y$
> 	- another contradiction
> - Thus $\alpha^{2}=y$.
link [[sets]] 