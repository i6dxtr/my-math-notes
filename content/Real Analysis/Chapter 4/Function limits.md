#ch4
##### Relations
- [[limit point|Limit points]]
- [[Epsilon-neighborhood]]
- [[function|Function]]
- [[Sequence]]

---
#### Functions
> [!definition]
> Let $E\subseteq \mathbb{R}$ and $f:E\longrightarrow \mathbb{R}$. Suppose $p$ is a [[limit point]] of the domain $E$. A number $L\in \mathbb{R}$ is called the **limit** of $f$ as $x$ approaches a limit point $p$ of $E$ if: $$\begin{gathered} \forall \varepsilon>0,\ \exists \delta>0\\ \text{such that:}\\ 0<\lvert x-p \rvert <\delta \Longrightarrow \lvert f( x )-L \rvert <\varepsilon. \end{gathered}$$ ==fg1==
> In other words, for any [[Epsilon-neighborhood|$\varepsilon-$neighborhood]] of $L$, there exists $\delta-$neighborhood of $p$ such that if $x\in E\cap (N_{\delta}( p )-\left\{ p \right\})$, then $f( x )\in N_{\varepsilon}( L )$.
> In this case, $\lim_{x \to p}f( x )=L.$

> [!remark]
> 1. $p$ does *not* have to be in the domain $E$.
> 2. $\delta$ depends on both $\varepsilon$ *and* $p$.
#### Examples
> [!example]
> ##### $f( x )=x+2,\ E=\mathbb{R}.$
> - Calculus: $\lim_{x \to 2}f( x )=4$
> 	- observe $\lvert f( x )-4 \rvert=\lvert x-2 \rvert$
> 	- for $\varepsilon>0$, $\delta=\varepsilon$
> 	- if $0<\lvert x-2<\delta \rvert$ then $\lvert f( x )-4 \rvert<\varepsilon$
> 
> ---
> ##### $f( x )-\frac{x^{2}}{x-2}$
> - $E=( -\infty, 2 )\cup ( 2, \infty )$
> - $2$ is a limit point of $E$
> 	- $\lim_{x \to 2}g( x )=4$
> 	- so
> 		$$
> 		\begin{align} \lvert g( x )-4 \rvert&=\left\lvert  \frac{x^{2}-2}{x-2}-4  \right\rvert \\ &=\left\lvert  \frac{x^{2}-4-4x+8}{x-2}  \right\rvert\\ &=\left\lvert  \frac{x^{2}-4x+4}{x-2}  \right\rvert\\ &=\left\lvert  \frac{( x-2 )^{2}}{( x-2 )}  \right\rvert \end{align}
> 		$$
> 	- where $x\ne 2$:
> 		- $\left\lvert  \frac{x^{2}-4}{x-2}-4  \right\rvert=\lvert x-2 \rvert$
> 		- for $\varepsilon>0$, $\delta=\varepsilon$
> 
> ---
> 
> ##### $f( x )=\frac{1}{x},\ E=( 0,\infty )$
> - If $p\in E$ then $\lim_{x \to p}f( x )=\frac{1}{p}$.
> - Assuming $x\in \left(  \frac{p}{2}, \infty  \right)$
> 	$$
> 	\begin{align} \left\lvert  \frac{1}{x}-\frac{1}{p}  \right\rvert &=\left\lvert  \frac{x-p}{xp}  \right\rvert \\ &\le \frac{\lvert x-p \rvert }{\left(  \frac{p}{2}  \right)p} \\ &\le \frac{2\lvert x-p \rvert }{p^{2}} \end{align}
> 	$$
> - We need $\frac{2\lvert x-p \rvert}{p^{2}}<\varepsilon$
> 	- so $\lvert x-p \rvert\le \frac{\varepsilon p^{2}}{2}$
> 	- For $\varepsilon > 0$, $\delta=\text{min}\left(  \frac{p}{2}, \frac{\varepsilon p^{2}}{2}  \right)$
> - Assume $\varepsilon =1$ and $\delta$ is independent of $p$.
> 	- ie. $0<\lvert x-p \rvert<\delta \longrightarrow \left\lvert  \frac{1}{x}-\frac{1}{p}  \right\rvert<1$
> 	- we can assume $\delta<1$
> 	- take $p=\delta$, and let $x=\frac{1}{2}\delta$
> 	- then $\lvert x-p \rvert=\frac{1}{2}\delta<\delta$
> 		- but, $\left\lvert  \frac{1}{x}-\frac{1}{p}  \right\rvert=\left\lvert  \frac{2}{\delta}-\frac{1}{\delta}  \right\rvert=\frac{1}{\delta}$
> 		- **qed**

> [!example]
> ##### $f( x )=\begin{cases} 1&&x\in \mathbb{Q} \\ 0&&x\not\in \mathbb{Q}\end{cases},\ \ f:\mathbb{R}\rightarrow\mathbb{R}$
> - $\forall p$, $\lim_{x \to p}f( x )$ does not exist
> 	- Fix $L\in \mathbb{R}$
> 	- We show
> 		- $\forall \delta>0$, $\exists x\in \mathbb{R}$ st. $0<\lvert x-p \rvert<\delta$
> - *but,* $\lvert f( x )-L \rvert\ge \varepsilon$ $$\lvert f( x )-L \rvert =\begin{cases} \lvert L \rvert &&\text{if }x\not\in  \mathbb{Q} \\ \lvert 1-L \rvert &&\text{if }x\in  \mathbb{Q}. \end{cases}$$
> - Take $\varepsilon=\text{max}\left\{ \lvert L \rvert, \lvert 1-L \rvert \right\}$
> - For $\delta > 0$, $N_{\delta}( p )-\left\{ p \right\}$
> - Let $x\in N_{\delta}( p )-\left\{ p \right\}$
> - If $x\in \mathbb{Q}$ then $\lvert f( x )-L \rvert=\lvert 1-L \rvert$
> - If $x\notin \mathbb{Q}$ then $\lvert f( x )-L \rvert=\lvert L \rvert$
> - *Case 1.* 
> 	- Assume $\varepsilon=\lvert 1-L \rvert$
> 		- ie. $\lvert 1-L \rvert\ge L$
> 	- Take $x\in ( N_{\delta}( p )-\left\{ p \right\} )\cap ( \mathbb{R}-\mathbb{Q} )$
> 		- So $\lvert f( x )-L \rvert=\lvert 1-L \rvert\ge \varepsilon$
> - *Case 2.*
> 	- Assume $\varepsilon=\frac{\lvert L \rvert}{2}$
> 		- ie. $\lvert 1-L \rvert\le \lvert L \rvert$
> 	- Take $x\in N_{\varepsilon}( N_{\delta}( p )-\left\{ p \right\} )\cap ( \mathbb{Q} )$
> 		- So $\lvert f( x )-L \rvert=\lvert L \rvert\ge \varepsilon$
> 
> ---
> ##### Suppose $g( x )=\begin{cases} 0&&x\in \mathbb{Q} \\ x&&x\notin \mathbb{Q}. \end{cases}$
> ###### 1.) $\lim_{x \to 0}g( x )=0$
> - Note, $\lvert g( x )-0 \rvert=\lvert g( x ) \rvert\le \lvert x \rvert$
> - Let $\varepsilon>0$ for $\delta=\varepsilon$
> - If $0<\lvert x \rvert<\delta$ then $\lvert g( x ) \rvert<\varepsilon$
> ###### 2.) If $p\ne 0$, $\lim_{x \to p}g( x )$ *does not exist.*
> - Fix $L$
> - Suppose $p\in \mathbb{Q}$
> 	- So $p_{n}=p+\frac{1}{n}$
> 	- $p_{n}$ converges to $p$
> 	- then $f( p_{n} )=0$, implying $\lim_{n \to \infty}g( p_{n} )=0$
> 		- holds
> 	- Take $q_{n}=p+\frac{\sqrt{2}}{n}\notin \mathbb{Q}$
> 	- so $\lim_{n \to \infty}( q_{n} )=p+\frac{\sqrt{2}}{n}$
> 	- moreover, $\lim_{n \to \infty}g( q_{n} )=p$
> 		- holds
> - Suppose $p\notin \mathbb{Q}$
> 	- so $r_{n}$ converges to $p$
> 		- where $r_{n}$ the rationals
> 	- implies $f( r_{n} )=0$
> 	- also $\lim_{n \to \infty}f( r_{n} )=0$
> 	- let $q_{n}=r_{n}+\frac{\sqrt{2}}{n}\notin \mathbb{Q}$
> 	- then $q_{n}$ converges to $p$
> 	- so $g( q_{n} )=q_{n}=r_{n}+\frac{\sqrt{2}}{n}$
> 	- therefore $\lim_{n \to \infty}g( q_{n} )=p$
#### Theorems
> [!theorem]
> Let $E\subseteq \mathbb{R}$ and let $p$ be a [[limit point]] of $E$. Any [[function]] $f:E\rightarrow \mathbb{R}$ has the following hold: $$\lim_{x \to p}f( x )=L\Longleftrightarrow \lim_{m \to \infty}f( p_{n} )=L$$... for every [[sequence]] $\lvert p_{n} \rvert$ in $E$ with $p_{n}\ne p$ and $\lim_{n \to \infty}p_{n}=p$.

> [!example]
> ##### $\lim_{x \to 0}\cos\left(  \frac{\pi}{x}  \right)$ does not exist.
> - $f( x )=\cos\left(  \frac{\pi}{x}  \right)$
> 	- $p_{n}=\frac{1}{2n}$ converges to 0
> 	- $q_{n}=\frac{1}{2n+1}$ converges to 0
> 	- $\lim_{f \to \infty}f( p_{n} )=1$
> 	- $\lim_{n \to \infty}f( q_{n} )$
> 		- $\cos\left(  \frac{\pi}{p_{n}}  \right)=\cos( ( 2n+1 )\pi )=-1$
> 		- as $p_{n}\rightarrow0$, $\lim_{n \to \infty}f( p_{n} )=1$
> 		- as $q_{n}\rightarrow0$, $\lim_{n \to \infty}f( q_{n} )=-1$
> 			- both above imply $\lim_{x \to 0}f( x )$ does not exist.
> ad-proof
> - $\lim_{x \to p}f( x )=L$
> 	- $p_{n}\rightarrow p$
> 	- wts $f( p_{n} )\rightarrow L$ ie. $\forall \varepsilon>0,\ \exists n_{0}$ st. if $n\ge n_{0}$, $\lvert f( p_{n}-L ) \rvert<\varepsilon$
> 	- so  $\forall \varepsilon>0,\ \exists n_{0}$ st. $0<\lvert x-p \rvert<\delta\longrightarrow \lvert f( x )-L \rvert<\varepsilon$
> 	- for $\delta>0$, since $\lim_{n \to \infty}p_{n}=p$, $\exists n_{0}$ st. if $n\ge n_{0}$ then $\lvert p_{n}-p \rvert<\delta$
> 	- for $n\ge n_{0}$, $0<\lvert p_{n}-p \rvert<\delta$ implies $\lvert f( p_{n} )-L \rvert<\varepsilon$
> 		- ie. $\lim_{n \to \infty}f( p_{n} )=L$
> ~~~~~ad-theorem
> Let $f:E\rightarrow\mathbb{R}$ be a function, and $p$ be a limit point of $E$. 
> - $\lim_{x \to p}f( x )=L$ *if and only if*:
> 	- For any sequence $\left\{ p_{n} \right\}$ in $E$, if:
> 		- $p_{n}\ne p$ 
> 		- $\lim_{n \to \infty}p_{n}=p$,
> 	- ... then $\lim_{n \to \infty}f( p_{n} )=L$.

> [!proof]
> ##### $( \Longrightarrow )$ $\lim_{x \to p}f( x )=L$ and $\left\{ p_{n} \right\}\subset E$ with $\lim_{n \to \infty}p_{n}=p$
> - $\forall \varepsilon > 0$, $\exists \delta>0$
> - if $0<\lvert x-p \rvert<\delta$ then $\lvert f( x )-L \rvert<\varepsilon$
> - For $\delta>0$, $\exists n_{0}\in \mathbb{N}$ such that for $n\ge n_{0}$,
> 	- $\lvert p_{n}-p \rvert<\delta.$
> - $( \forall\varepsilon>0, \exists n_{0}\in \mathbb{N}, n\ge n_{0}, \lvert f( p_{n} ) -L\rvert<\varepsilon )$
> 	- ie. $\lim_{n \to \infty}f( p_{n}=L )$.
> ##### $( \Longrightarrow )$ Assume that $\lim_{x \to p}f( x )\ne L$.
> - Let:
> 	- $\forall \varepsilon>0$
> 	- $\mathbf{\forall\delta>0}$,
> 	- $\exists x\in E$ st. $0<\lvert x-p \rvert<\delta$
> 	- but $\lvert f( x )-L \rvert\ge \varepsilon$
> - where:
> 	- $\delta=\frac{1}{n}$,
> 	- $\exists p_{n}\in E$
> 	- $0<\lvert p_{n}-p \rvert<\frac{1}{n}$ 
> 	- such that $\lvert f( p_{n}-L )\lvert\ge\varepsilon$
> - So: 
> 	- $\left\{ p_{n} \right\}\subseteq E$, $p_{n}\ne p$, 
> 	- $\lim_{n \to \infty}p_{n}=p$,
> - but,
> 	- $\lim_{n \to \infty}f( p_{n} )\ne L$
> 	- a contradiction. **qed**