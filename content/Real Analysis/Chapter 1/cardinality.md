#ch1 
### Outline
- [Cardinality](#Cardinality)
- [Finiteness / Countable](#Finiteness / Countable)
- [Index Family of Subsets](#Index Family of Subsets)
- [Theorems](#Theorems)
##### Relations
- [[sets|Sets]]
- [[enumeration|Enumeration]]
### Cardinality
> [!definition]
> We say $A$ and $B$ have the same **cardinality** if they are *equivalent*.

> [!corollary]
> ### Properties
> 1. *Symmetric:* If $A\sim B$ then $B\sim A$
> 2. *Reflexive:* $A\sim A$ (given)
> 3. *Transitive:* If $A\sim B$ and $B\sim C$, then $A \sim C$.
### Finiteness / Countable
> [!definition]
> $$\mathbb{N}_{n}=\left\{ 1,2,3,\cdots, n \right\}$$
> 4. $A$ is **finite** if $A\sim \mathbb{N}_{n}$ for some $n\in \mathbb{N}$.
> 5. $A$ is **infinite** if it is *not finite*.
> 6. $A$ is **countable** if $A\sim \mathbb{N}$.
> 7. $A$ is **uncountable** if $A$ is *infinite* and *not countable.*
> 8. $A$ is **at most countable** if $A$ is *finite* or $A$ is *countable*.
### [[Index Family of Subsets]]
- we can count the union/intersection of the index family of subsets of countable sets
> [!theorem]
> If $\left\{ E_{n} \right\}_{n=1}^{\infty}$ is a sequence of countable [[sets]] at: $$S=\bigcup_{n=1}^{\infty}E_{n}$$... then $S$ is countable.

> [!theorem]
> $$E_{n}\text{ is countable.}$$

> [!proof]
> As follows:
> $$
> \begin{align} E_{1}&=\left\{ x_{1,1}, x_{1,2}, x_{1,3},\cdots  \right\}\\
> E_{2}&=\left\{ x_{2,1}, x_{2,2}, x_{2,3}, \cdots \right\} \\
> \cdots \\
> E_{n}&=\left\{ x_{n,1}, x_{n,2}, x_{n,3},\cdots \right\} \\
> \end{align}
> $$
> ... so the following holds:
> $$
> \begin{align} S=\bigcap_{n=1}^{\infty}E_{n}=\left\{ x_{n, k}:n\in \mathbb{N}, k\in \mathbb{N} \right\} \\
> \text{ where }f \begin{cases} \mathbb{N} \times  \mathbb{N} &\longrightarrow S \\ ( n, k ) &\longrightarrow x_{n,k} \\ \end{cases}\end{align}
> $$
> - $\mathbb{N} \times \mathbb{N}$ is countable, so there is a *one-to-one* and *onto* mapping for $\mathbb{N}\longrightarrow^{g} \mathbb{N} \times \mathbb{N}$
> - $f og:\mathbb{N\longrightarrow S}$ is onto
> - Therefore, $S$ is countable.

> [!theorem]
> $$\mathbb{Q}\text{ is countable.}$$

> [!proof]
> - Let $r\in \mathbb{Q}$
> 	- $r=\frac{m}{n}$, where $n\in \mathbb{Z}$, $m\in \mathbb{N}$
> - So: $$E_{m}=\left\{ \frac{m}{n}, n\in  \mathbb{Z} \right\}$$
> - We say $E_{n}$ *is countable*
> 	- $\mathbb{Z}\longrightarrow E_{m}$
> 	- onto $n\longmapsto \frac{n}{m}$.

> [!theorem]
> ##### $\left[ 0,1 \right]$ is uncountable.

> [!proof]
> - We show every countable subset of $\left[ 0,1 \right]$ is a *proper subset*
> 	- Let $E$ be a countable subset of $\left[ 0,1 \right]$
> 	- We show $y\in \left[ 0,1 \right]$, but not in $E$
> 		- Let $E=\left\{ x_{1}, x_{2}, \cdots \right\}$ be an *enumeration* of $E$.
> 		- Decimal expansion:
> 			$$
> 			\begin{align} x_{1}&=\ \cdot x_{(1,1)} \ x_{(1,2)}\  x_{( 1,3 )}\cdots \\ x_{2}&=\ \cdot x_{( 2,1 )}\ x_{( 2,2 )}\ x_{( 2,3 )}\cdots \\ &\cdots \text{ }\end{align}
> 			$$
> 			... observe $y= \cdot y_{1}\  y_{2}\  y_{3}$
> 			- If $x_{( 1,1 )}\le 5$ take $y_{1}=7$
> 			- If $x_{( 1,1 )}>5$ take $y_{1}=3$
> 			- If $x_{( 2,2 )}\leq 5$ take $y_{2}=7$
> 			- If $x_{( 2,2 )}>5$ take $y_{2}=3$
> 			- If $x_{( n,n )}\leq$ take $y_{2}=7$
> 			- If $x_{( n,n )}>5$ take $y_{2}=3$

> [!remark]
> Any interval $( a,b ), [a,b), (a,b], ( a, \infty ), ( -\infty, \alpha ), \mathbb{R}$ is *uncountable.*

> [!example]
> $$(10, 100]\text{ is uncountable.}$$
> - $\left[ 11,100 \right]\subseteq (10, 100]$
> - $\left[ 11,100 \right]\sim \left[ 0,1 \right]$
> - So $(10,100]$ is uncountable.
> $$\mathbb{R}-\mathbb{Q}\text{ is uountable.}$$
> - Assume $\mathbb{R}- \mathbb{Q}$ is countable
> 	- Then $\mathbb{R}=( \mathbb{R} - \mathbb{Q} )\cup \mathbb{Q}$ is a union of two countable sets
> 	- *Contradiction*: the union of two countable sets is countable
> - Thus, $\mathbb{R}-\mathbb{Q}$ is uncountable.
### Theorems
... following from enumeration def.
> [!theorem]
> Every infinite subset of a countable set is countable.

> [!proof]
> - Let $A$ be a countable set and $E$ an *infinite subset* of $A$.
> - For each $y\in E$, there exists an $n\geq 1$ such that $y=x_{n}$
> - *Proof by induction:*
> 	- Suppose $W=\left\{ n\in \mathbb{N}:x_{n}\in E \right\}\subseteq \mathbb{N}$
> 	- Take $n_{1}$ to be the smallest of $W$, so $x_{n_{1}}\in E$
> 	$$W_{1}=\left\{ n\in \mathbb{N}:x_{n}\in E - \left\{ x_{n_{n}1} \right\} \right\}\subseteq \mathbb{N}$$
> 	- Assume that $x_{n_{1}}, x_{n_{2}},...,x_{n_{k-1}}$ are in $E$
> 	$$W_{k-1}=\left\{ n\in  \mathbb{N}:x_{n}\in  E - \left\{ x_{n_{1}}, x_{n_{2}}, \cdots, x_{n_{k-1}} \right\} \right\}$$... $n_{k}$ is the smallest elemtn of $W_{k-1}$
> $$E=\left\{ x_{n_{k}}: k\in  \mathbb{N} \right\}$$
> 	- Thus, $E$ is countable.

> [!theorem]
> If $f$ maps $\mathbb{N}$ onto $A$, then $A$ is *at most countable*.

> [!proof]
> - Showing $f:\mathbb{N} \rightarrow A$ is onto:
> 	- For $a\in A$, $f^{-1}( \left\{ a \right\} )\subseteq \mathbb{N}$
> 	- Let $n_{a}$ be the smallest element of $f^{-1}( \left\{ a \right\} )$
> 	- Consider: $$\left\{ n_{a}:a\in  A \right\}\subseteq \mathbb{N}$$
> 		- Assume $A$ is infinite
> 		- So if $a\neq b$ then $n_{a}\neq n_{b}$ ($f( n_{a}=a )$, $f( n_{b} )=b$)
> 		- $\left\{ n_{a}:a\in A \right\}$ is an infinite subset of $\mathbb{N}$
> 		- By the previous theorem, $\left\{ n_{a}:a\in A \right\}$ is countable
> 		- Let $g:\left\{ n_{a}:a\in \mathbb{N} \right\}\rightarrow \mathbb{N}$ be one-to-one and onto
> 		- Take $h:A\rightarrow\left\{ n_{a}:a\in A \right\}$
> 		- $h$ is one-to-one and onto
> 			- $a\longmapsto n_{a}$
> 			- $goh:A\rightarrow\mathbb{N}$