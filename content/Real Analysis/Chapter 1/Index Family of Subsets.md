#ch1 
### Outline/Relation
- **Union/Intersection family of subsets**
- [[sets|Sets]]
- [[Sequence|Sequence]]
- [[function|Function]]
- [[enumeration|Enumeration]]
- [[cardinality|Cardinality]]
- **Theorems**
- **Examples**
### Definition
> [!definition]
> Let $A$ and $X$ be nonempty [[sets]]. An **index family of subsets** of $X$ with index set $A$ is a [[function]] $f:A\rightarrow \mathcal{P}( X )$. 
> - *ex.* For $a\in A$, $f( a )$ is a subset of $X$. 
> - Notation: $\left\{ E_{a} \right\}_{a\in A}$
> - If $A=\mathbb{N}$, $\left\{ E_{n} \right\}_{n\in \mathbb{N}}$ is called a *[[sequence]] of subsets* of $X$.
> 	- denoted $\left\{ E_{n} \right\}_{n=1}^{\infty}$

> [!example]
> 1. $$\left\{ \mathbb{N}_{n} \right\}_{n\in  \mathbb{N}}=\left\{ \mathbb{N}_{n} \right\}_{n\ge1}=\left\{ \mathbb{N}_{n} \right\}_{n=1}^{\infty}$$... where $\mathbb{N}_{n}=\left\{ 1,2,...,n \right\}$.
> 2. $$I_{n}=\left\{ x\in  \mathbb{R}, 0<x<\frac{1}{n} \right\}$$... for each $n\in\mathbb{N}$.
> 3. $$E_{x}=\left\{ r\in  \mathbb{Q}, 0<r<x \right\}$$... for each $x\in ( 0,1 )$.
> 	1. $\left\{ E_{x} \right\}_{x\in ( 0,1 )}$ is an indexed family of subsets of $\mathbb{Q}$.
> 	2. The index set is $( 0,1 )$
#### Union family
> [!definition]
> Suppose $\left\{ E_{\alpha} \right\}_{\alpha\in A}$ is an indexed family of subsets of $X$. The **union** of the family of sets $\left\{ E_{\alpha} \right\}_{\alpha\in A}$ is defined to be: $$\bigcup_{\alpha\in  A}^{} E_{\alpha}=\left\{ x\in  X:x\in  E_{\alpha}\text{ for some }\alpha\in  A \right\} .$$
#### Intersection family
> [!definition]
> Similarly, the **intersection** of the family of sets $\left\{ E_{\alpha} \right\}_{\alpha\in A}$ is defined as: $$\bigcap_{\alpha\in A  }^{}E_{\alpha}=\left\{ x\in  X:x\in  E_{\alpha}\text{ for all }\alpha\in  A \right\}.$$

> [!remark]
> If $A=\mathbb{N}$, we use the notations:
> $$\bigcup_{n=1}^{\infty}E_{n}\text{ and }\bigcap_{n=1}^{\infty}E_{n}$$... instead of: $$\bigcup_{n\in  \mathbb{N}}^{}E_{n}\text{ and }\bigcap_{n\in  \mathbb{N}}^{}E_{n}.$$
### Theorems
> [!remark]
> $$
> \begin{align} x\in  \bigcup_{\alpha\in  A}^{}E_{\alpha} &\Longleftrightarrow \exists \alpha\in  A\text{ such that }x\in  E_{\alpha}. \\ y\in  \bigcap_{\alpha\in  A}^{}E_{\alpha} &\Longleftrightarrow \forall \alpha\in  A, y\in  E_{\alpha}. \end{align}
> $$

> [!theorem]
> Let $E_{\alpha}$, where $\alpha\in A$, $E_{\alpha}\subseteq X$, and $E\subseteq X$. Then the following hold:
> 1. $E\cap ( \cup _{\alpha\in A} E_{\alpha} )=\cup _{\alpha\in A}( E\cap E_{\alpha} )$
> 2. $E\cup ( \cap _{\alpha\in A}E_{\alpha} )=\cap_{\alpha\in A}( E\cup E_{\alpha} )$
> 3. $( \bigcap_{\alpha\in A}E_{\alpha} )^{c}$ ... (didn't finish)

> [!theorem]
> Let $f:X\rightarrow Y$ be a function.
> 1. If $( E_{\alpha} )_{\alpha\in A}$ is a family of subsets of $X$, then: $$f\left(  \bigcup_{\alpha\in  A}^{}E_{\alpha}  \right)=\bigcup_{\alpha\in  A}^{}f( E_{\alpha} ).$$
> 2. If $( E_{\alpha} )_{\alpha\in A}$ is a family of subsets of $X$, then: $$f\left(  \bigcap_{\alpha\in  A}^{}E _{\alpha}  \right)\subset \bigcap_{( \alpha\in  A )}^{}f( E_{\alpha} ).$$
> 3. If $( F_{\alpha} )\alpha\in A$ is a family of subsets of $Y$, then:
> 	$$
> 	\begin{align} f^{-1}\left(  \bigcup_{\alpha\in  A}^{}F_{\alpha}  \right)&=\bigcup_{\alpha\in  A}^{}f^{-1}( F_{\alpha} ) \\ f^{-1}\left(  \bigcup_{\alpha\in  A}^{}F_{\alpha}  \right)&=\bigcap_{\alpha\in  A}^{}f^{-1}( F_{\alpha} ). \end{align}
> 	$$

> [!example]
> $$f( x )=y=\sin x.$$
> - $E_{n}=[n, \infty)$
> - $f( E_{n} )=[-1,1]$
> - $\bigcap_{n=1}^{\infty}E_{n}=\emptyset$
> - $\bigcap_{n=1}^{\infty}f( E )=[-1,1]$
> - $f\left(  \bigcap_{n=1}^{\infty}E_{n}  \right)=\emptyset$

> [!theorem]
> Let $E_{\alpha}$, where $\alpha\in A$, $E_{\alpha}\subseteq X$, and $E\subseteq X$. Then the following hold:
> $$
> \begin{align} a.)&&E\cap \left(  \bigcup_{\alpha\in  A}^{}E_{\alpha}  \right)&=\bigcup_{\alpha\in  A}^{}( E\cap E_{\alpha} ) \\ b.)&&E\cup\left(  \bigcap_{\alpha\in A}^{}E_{\alpha}  \right)&=\bigcap_{\alpha\in  A}^{}( E\cup E_{\alpha} ) \\ c.)&& \left(  \bigcup_{\alpha\in  A}^{}E_{\alpha}  \right)^{C} &= \bigcap_{\alpha\in  A}^{}E_{\alpha}^{c} \\ d.)&&\left(  \bigcap_{\alpha\in  A}^{}E_{\alpha}  \right)^{c}&=\bigcup_{\alpha\in  A}^{}E_{\alpha}^{c} \end{align}
> $$

> [!theorem]
> Let $f:X\rightarrow Y$ be a function.
> 1. If $( E_{\alpha} )_{\alpha\in A}$ is a family of subsets of $X$, then: $$f\left(  \bigcup_{\alpha\in  A}^{}E_{\alpha}  \right)=\bigcup_{\alpha\in  A}^{}f( E_{\alpha} ).$$
> 2. If $( E_{\alpha} )_{\alpha\in A}$ is a family of subsets of $X$, then: $$f\left(  \bigcap_{\alpha\in  A}^{}E _{\alpha}  \right)\subset \bigcap_{( \alpha\in  A )}^{}f( E_{\alpha} ).$$
> 3. If $( F_{\alpha} )\alpha\in A$ is a family of subsets of $Y$, then:
> 	$$
> 	\begin{align} f^{-1}\left(  \bigcup_{\alpha\in  A}^{}F_{\alpha}  \right)&=\bigcup_{\alpha\in  A}^{}f^{-1}( F_{\alpha} ) \\ f^{-1}\left(  \bigcup_{\alpha\in  A}^{}F_{\alpha}  \right)&=\bigcap_{\alpha\in  A}^{}f^{-1}( F_{\alpha} ). \end{align}
> 	$$

> [!example]
> $$f( x )=y=\sin x.$$
> - $E_{n}=[n, \infty)$
> - $f( E_{n} )=[-1,1]$
> - $\bigcap_{n=1}^{\infty}E_{n}=\emptyset$
> - $\bigcap_{n=1}^{\infty}f( E )=[-1,1]$
> - $f\left(  \bigcap_{n=1}^{\infty}E_{n}  \right)=\emptyset$
### Cardinality
- the union/intersection of the indexed family of subsets of a *countable* set is also *countable.*
### Examples
> [!example]
> $$\left\{ \mathbb{N}_{n} \right\}_{n=1}^{\infty}$$
> - $\bigcup_{m=1}^{\infty}\mathbb{N}_{n}=\mathbb{N}$
> - $\bigcap_{m=1}^{\infty}\mathbb{N}_{n}=\left\{ 1 \right\}$
> ----
> $$I_{n}=\left\{ x\in  \mathbb{R}: 0<x<\frac{1}{n} \right\}$$
> - $\bigcup_{m=1}^{\infty}\mathbb{I}_{n}=( 0,1 )$
> - $\bigcap_{m-1}^{\infty}I_{n}=\emptyset$
> - ... for every $x>0$
> - By the [[Archimedean property]], there exists $k\in\mathbb{N}$ such that $kx>1$
> 	- Implying $x>\frac{1}{k}\Longleftrightarrow x\not\in I_{k}$
> 		- $\Rightarrow x\notin \bigcap_{m=1}^{\infty}I_{n}$