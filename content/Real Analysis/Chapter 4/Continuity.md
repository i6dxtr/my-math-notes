#ch4 
##### Relations
- [[Function limits]]
- [[function|Functions]]
- [[Discontinuity]]
- [[open sets|Open sets]]
- [[compact sets|Compact sets]]

---

> [!definition]
> Let $f:E\rightarrow\mathbb{R}$ where $E\subseteq \mathbb{R}$. $f$ is said to be **uniformly continuous** if $\forall \varepsilon>0, \exists \delta$ (dependent on $\varepsilon$) such that if $x,y\in E$ and $\lvert x-y \rvert<\delta$, then $\lvert f( x )-f( y ) \rvert<\varepsilon.$ $$\begin{gathered} \forall \varepsilon>0, \exists \delta>0 \\ \text{ such that} \\ x,y\in  E\bigwedge\lvert x-y \rvert <\delta\Longrightarrow \lvert f( x )-f( y ) \rvert <\varepsilon \end{gathered}$$
> - $\delta$ depends on $\varepsilon$ and $p$

> [!definition]
> Let $f:E\rightarrow \mathbb{R}.$ $f$ is **right continuous** at $p\in E$ if: $$\begin{gathered} \forall \varepsilon>0, \exists\delta>0\\ \text{ for which} \\ \lvert f( x )-f( p ) \rvert <\varepsilon \end{gathered}$$... for all $x\in E$ where $p<x<p+\delta.$ *Left continuity* is similarly defined.

> [!theorem]
> Suppose $p\in E$ and $f( p^{+} )$. $f$ is right continuous *if and only if* $f( p^{+} )=f( p ).$
---

> [!theorem]
> $f:E\rightarrow \mathbb{R}$ is continuous *if and only if* for any [[open sets|open]] $\vartheta$ subset of $\mathbb{R},$ $f^{-1}( \vartheta )$ is open in $E.$
> *"There exists an open $U$ such that $f^{-1}( \vartheta )=U\cap E$."*

> [!remark]
> Every open subset of $\mathbb{R}$ is a countable union of open intervals. $$\vartheta=\bigcup_{n=1}^{\infty}I_{n}$$... implying $f:E\rightarrow\mathbb{R}$ is continuous if and only if for every open interval $I$ in $\mathbb{R}$, $f^{-1}( I )$ is open in $E$.

> [!theorem]
> Let $f:E\rightarrow \mathbb{R}$ where $E\subseteq \mathbb{R}$. $f$ is continuous if $f$ is continuous at every point of $E$.
> 
> ---
> 
> Let $f,g$ be functions such that $f:E\rightarrow \mathbb{R}$ and $g:E\rightarrow \mathbb{R}$. If $f, g$ are continuous, then $f+g$, $\lambda f$, $fg$, $\frac{f}{g}$ are also continuous.
> 
> ---
> 
> Let $f,g$ be functions where $f:E\rightarrow \mathbb{R}$ and $g:F\rightarrow\mathbb{R}$ and $f( E )\subseteq F.$ Let $p$ be a limit point of $E$. If $f$ is continuous at $p$ and $g$ is continuous at $f( p )$, then $g o f$ is continuous at $p$. 

> [!proof]
> 1. Let $\varepsilon>0$, since $g$ is continuous at $f( p )$. 
> 2. Then $\exists \delta>0$ such that $\forall y\in F$ $\lvert y-f( p ) \rvert<\delta$ implies $\lvert g( y )-f( p ) \rvert<\varepsilon$. 
> 3. With $\delta>0$, $\exists \delta'>0$ such that if $x\in E$ then $\lvert x-p \rvert<\delta'$
> 4. This implies $\lvert f( x )-f( p ) \rvert<\delta$.
> 5. Fix $x\in E$ with $\lvert x-p \rvert<\delta'$. 
> 6. Then, since $f( x )\in F$ and $\lvert f( x )-f( p ) \rvert<\delta$, we know $\lvert g( f( x ) )-g( f( p ) ) \rvert<\varepsilon.$

> [!corollary]
> Let $K$ be a [[compact sets|compact subset]] of $\mathbb{R}$ and $f:K\rightarrow \mathbb{R}$ where $f$ is continuous. Then, there exists $p, q\in K$ such that $f( p )\le f( x )\le f( q ),$ for all $x\in K.$

> [!proof]
> - Observe that $f( K )$ is compact.
> - In particular, it is bounded.
> - Let $M=\text{sup}\left\{ f( x ):x\in K \right\}$
> - If $M\notin f( K )$
> 	- $M$ is a limit point of $f( K )$
> 	- So $\exists ( y_{n} )\subseteq f( K )$ such that $y_{n}\rightarrow M$.
> 	- So $\forall n\ge 1, y_{n}=f( x_{n} )$ for $x_{n}\in K$
> 	- So $( x_{n} )\subset K$ (compact)
> 	- Therefore there exists a subsequence $x_{n_{k}}\rightarrow x\in K$
> 	- By continuity, $f( x_{n_{k}} )\rightarrow f( x )$
> 	- In other words, $f( x_{n_{k}} )\rightarrow f( x )$
> 	- Which implies $M=f( x )\in f( K )$, a contradiction
---

> [!proof]
> ### Proof: $f$ is continuous if some open set $V\in \mathbb{R}$ has $f^{-1}( V )$ open in $E$.
> 1. We'll show $f^{-1}( V )$ is open in $E$.
> 2. Let $p\in f^{-1}( V )$.
> 3. Then $f( p )\in V$ and $V$ is open.
> 4. So $\exists \varepsilon>0$ such that $N_{\varepsilon}( p )\subseteq V$.
> 5. For such $\varepsilon>0$, assume $\delta>0$ such that if $x\in E$ and $\lvert x-p \rvert<\delta$, then $\lvert f( x )-f( p ) \rvert<\varepsilon$.
> 6. In other words, if $x\in E\cap N_{\delta}( p )$ then $f( x )\in N_{\varepsilon}( f( p ) )$. 
> 7. Meaning,  $$x\in f^{-1}( N_{\varepsilon}( f( p ) ) )\subseteq f^{-1}( V ).$$
> 8. In other words, $$E\cap N_{\delta}( p )\subseteq f^{-1}( V )\subseteq E.$$

> [!proof]
> ### Proof: If some open set $V\in \mathbb{R}$ has $f^{-1}( V )$ open in $E$, then $f$ is continuous.
> 1. We'll show $f$ is continuous.
> 2. Fix $p\in E$.
> 3. Then $\forall \varepsilon>0$, take $V=N_{\varepsilon}( f( p ) )$.
> 4. So $f^{-1}( N_{\varepsilon}( f( p ) ) )$ is open in $E$ and $p$ is in $f^{-1}( N_{\varepsilon}( f( p ) ) )$
> 5. Then $\exists \delta>0$ such that $\forall x\in N_{\delta}( p )\cap E \subseteq f^{-1}( N_{\varepsilon}( f( p ) ) )$.
> 6. In other words, $$x\in  N_{\delta}( p )\cap E \longrightarrow x\in  f^{-1}( N_{\varepsilon}( f( p ) ) )$$
> 7. Therefore, if $\forall x\in E$, $\lvert x-p \rvert<\delta$ then $\lvert f( x )-f( x ) \rvert<\varepsilon$.
---

#### Applying the definition
> [!example]
> $$\begin{gathered} f:[1,\infty)\rightarrow \mathbb{R} \\ f( x )=\sqrt{x}\\ \text{Claim:} f \text{ is uniformly continuous.}\end{gathered}$$
> - Start with $\lvert f( x )-f( y ) \rvert=\lvert \sqrt{x}-\sqrt{y} \rvert$
> 	- $=\frac{\lvert x-y \rvert}{\sqrt{x}+\sqrt{y}}$
> - Since $x,y\ge 1,$ $\lvert f( x )-f( y ) \rvert\le \frac{\lvert x-y \rvert}{2}$
> - Take $\delta=2\varepsilon$
> - If $\lvert x-y \rvert<\delta,$ then $\frac{\lvert x-y \rvert}{2}<\varepsilon$ implies $\lvert \sqrt{x}-\sqrt{y} \rvert<\varepsilon$
> 
> ---
> $$\begin{gathered} g:( 0,1 )\rightarrow \mathbb{R} \\ g( x )=\frac{1}{x} \\ \text{Claim: }g \text{ is *not* uniformly continuous.}\end{gathered}$$
> - Take $\left\lvert \frac{1}{x}-\frac{1}{y}  \right\rvert=\frac{\lvert x-y \rvert}{xy}$
> 	- where $x,y\in ( 0,1 )$
> - Pick (any) $\delta > 0$
> - Choose $x,y$ with $\lvert x-y \rvert<\delta$ but $\frac{\lvert x-y \rvert}{xy}$ is *large*
> - Suppose $x=\frac{1}{n}$ and $y=\frac{2}{x}$
> - Then $\lvert x-y \rvert=\frac{2}{n}-\frac{1}{n}=\frac{1}{n}$
> - So $\lvert f( x )-f( y ) \rvert=\left\lvert  n-\frac{n}{2}  \right\rvert=\frac{n}{2}$
> - We can choose $n$ large enough such that $\lvert x-y \rvert=\frac{1}{n}<\delta$ but $\lvert f( x )-f( y ) \rvert=\frac{n}{2}\ge 1$
> ---
> $$\begin{gathered} h:( 1,2 )\rightarrow\mathbb{R} \\ h( x )=\frac{1}{x} \\ h \text{ is uniformly continuous.} \end{gathered}$$
> - Take $\lvert h( x )-h( y ) \rvert=\frac{\lvert x-y \rvert}{xy}\le \lvert x-y \rvert$ since $x,y > 1$
> - For $\varepsilon>0,$ take $\delta=\varepsilon.$
> - Then if $\lvert x-y \rvert<\delta$ then $\lvert h( x )-h( y ) \rvert<\varepsilon$
#### Applying the theorem
> [!example]
> ##### $f( x )=x+1$
> $$\begin{gathered} V=( 0,1 ) : \\ f^{-1}( V )=\left\{ x\in  \mathbb{R}:f( x )\in  ( 0,1 ) \right\} = ( -1,0 ) \\ g( x )=\begin{cases} \frac{1}{x-1}&x\ne 1 \\ 2&x=1 \end{cases} \\V=( 1,3 ): \\ f^{-1}( V )=\left\{ x\in  \mathbb{R}:g( x )\in  ( 1,3 ) \right\} \\ x\ne 1 \longrightarrow 1<\frac{1}{x-1} <\varepsilon \Longrightarrow  x-1<1 \longleftrightarrow x < 2 \\ \frac{1}{3} < x-1 \longrightarrow  \frac{4}{3} <x \\ ( -\infty, 2 )\cup \left(  \frac{4}{3}, \infty  \right) \\ \text{thus, }g^{-1}( V )=\left\{ x\in  \mathbb{R} : g( x )\in  ( a,b ) \right\}\end{gathered}$$
> - if $x\ne 1$ then $a<\frac{1}{x-1}<b$
> 	- implying $x-1<\frac{1}{a}$
> 	- meaning $x<1+\frac{1}{a}$
> 	- meaning $\frac{1}{x-1}<b$
> 	- so $1+\frac{1}{b}<x$
> - for $\left(  -\infty, 1+\frac{1}{a}  \right)\cap \left(  1+\frac{1}{b},\infty  \right)-\left\{ 1 \right\}$
#### Relation with compact sets
> [!example]
> $$f:\mathbb{R}\rightarrow \mathbb{R}, x\rightarrow x^{2}$$
> 1. $f( \mathbb{R} )=[0, \infty)$ is *not* compact
> 2. $g:(0,1]\rightarrow \mathbb{R}, x\rightarrow \frac{1}{x}$
> 	1. Continuous
> 	2. $g( (0,1] )=[1, \infty)$ is closed, but *not* compact
> 3. $h:[a, 1]\rightarrow \mathbb{R}, x\rightarrow \frac{1}{x}$ where $0<a<1$
> 	1. $h( \left[ a, 1 \right] )=[1, \frac{1}{a}]$