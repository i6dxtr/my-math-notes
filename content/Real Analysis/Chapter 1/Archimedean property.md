#ch1 
### Outline/Relations
- [[Least Upper Bound Property]]
- **Intervals**
- **Existence of positive real roots**
	- also in LUBP
- **Nonexistence of some rational roots**
### Definition
> [!definition]
> If $x,y\in \mathbb{R}$ and $x>0$, then there exists $n \in \mathbb{N}$ such that $nx>y$.
> [!proof]
> 1. Assume $y>0$; then: $$A=\left\{ nx: n\in  \mathbb{Z} \right\}$$
> 2. Assume that the property is not true; then: $$\forall n\in  \mathbb{N},\ nx\leq y$$... where $y$ is an upper bound of $A$.
> 3. Let $x=\text{sup }A$
> 4. Then $x-x$ is not an upper bound of $A$:
> 	1. Let $n_{0}\in \mathbb{N}$ and $\alpha=\text{sup }A$
> 	2. $n_{0}x> x-x$
> 	3. $( n_{1}+1 )x>\alpha$
> 	4. ... but $( n_{0}+1 )x\in A$, *a contradiction.*
> [!remark]
> Given $\epsilon>0$, there exists a positive integer $n_{o}$ such that $n_{o}\epsilon>1$. Therefore, $$\frac{1}{n}<\epsilon$$... for all integers $n, n\ge n_{o}$.
### Connection with [[Least Upper Bound Property|the supremum]]
> [!theorem]
> Let $E$ be a non-empty [[sets|subset]] of $\mathbb{R}$ that is bounded above and $x$ is an upper bound. We say that $x$ is a supremum *if and only if:* $$\forall\epsilon>0,\ \exists x\in E \ \ \ \text{ s.t. }\ \ \ x-\epsilon<x\le x.$$
### Defining intervals
> [!definition]
> A subset $J$ of $\mathbb{R}$ is an **interval** if whenever $x,y\in J$ with $x<y$, then every $t$ satisfying $x<t<y$ is in $J$.
> [!theorem]
> If $x,y\in \mathbb{R}$ and $x<y$, then there exists $r\in \mathbb{Q}$ such that $x<r<y$.
> - "$\mathbb{Q}$ is dense in $\mathbb{R}$"
> [!proof]
> 1. Assume $y-x>0$
> 2. Then the Archimedean property implies that there exists $n\in \mathbb{N}$ such that $n( y-x )>1$.
> 3. Therefore, $ny>1+nx$.
> 4. Consider $\left\{ k\in \mathbb{N}: k>nx \right\}\subseteq \mathbb{N}$ (non-empty)
> 	1. Observe that it has a smallest element, which we'll call $m$:
> 	2. $\underline{m>nx}>m-1\Longrightarrow nx+1>m$
> 		1. $\frac{m}{n}>x$
> 	3. $m<nx+1<ny$
> 		1. $\frac{m}{n}<y$
> 	4. $\frac{m}{n}\in \mathbb{Q}$
> 	5. $x<\frac{m}{n}<y$
### Real roots
> [!theorem]
> If $y>0$, there exists $x\in \mathbb{R}$ such that $x^{2}=y$.
> [!proof]
> - Case $y>1$
> 	- Let $C=\left\{ x\in \mathbb{R}: x>0, x^{2}<y \right\}$
> 		- $C\ne \emptyset$, $1\in C$
> 		- $C$ is bounded above
> 	- $y$ is the upper bound of $C$
> - Assume $z>y$
> 	- then $z^{2}>y^{2}>y$ (since $y>1$)
> 	- so $z\notin C$
> 	- i.e. if $x\in C$ then $x\leq y$
> - Let $\alpha=\text{sup }C$
> - We prove $x^{2}=y$
> 	- Consider the following:  $$\begin{align} \beta=&\ \alpha+\frac{y-x^{2}}{x+y}&=\frac{y( x+1 )}{x+y} \\ b-y=&\frac{y( y-1 )( x^{2}-y )}{( x+y )^{2}} \end{align}$$
> - Assume that $x^{2}<y$; then: $$\beta=x+\frac{y-\alpha^{2}}{\alpha+y},\ \ \beta>\alpha$$... on the other hand: $$\beta^{2}-y<0\text{ where }  \beta^{2}<y , \ \beta\in  C,\text{ and }\beta>x$$... a contradiction.
> - Assume that $\alpha^{2}>y$; then: $$\begin{align} \beta^{2}-y>0&&\Longrightarrow \beta^{2}>y \end{align}$$
> - ==Claim==: $\beta$ is an upper bound of $C$: $$\begin{align} & \text{If } z\geq \beta \Longrightarrow z^{2}\geq \beta^{2} > y \Longrightarrow z\notin C \\ &\text{If } z\in  C\longrightarrow z<\beta \\ &\text{But, }\beta=\alpha+\frac{y-\alpha^{2}}{x+y}<\alpha. \end{align}$$... $\beta < \alpha$, so $\beta$ is an upper bound, and $\alpha=\text{sup }C$, *a contradiction.*
### Rational root nonexistence
> [!remark]
> $$\sqrt{2}\notin \mathbb{Q}.$$
> - $\mathbb{Q}$ *does not* have the least upper bound property.
> [!proof]
> - Assume $\sqrt{2}=\frac{p}{q}$, where $p,q$ have no common multiple
> - Then: $$\begin{align} 2=\frac{p^{2}}{q^{2}} &\Longrightarrow 2q^{2}=p^{2} \\ &\Longrightarrow p^{2}\text{ is an even number} \\ &\Longrightarrow p \text{ is even. } (\text{assume }p=2k+1) \end{align}$$
> - Rewrite: $$\begin{align} p=2l &\Leftrightarrow p^{2}=4l^{2} \\2q^{2}=p^{2}=4l^{2} &\Leftrightarrow q^{2}=2l^{2}. &&\text{ (even)} \end{align}$$
link [[sets]] 