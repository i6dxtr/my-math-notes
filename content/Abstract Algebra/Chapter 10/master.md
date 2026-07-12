## Properties of exponentiation
- recall [[law of exponents]]
- proofs:
	- $a^{m}a^{n}=aa\cdots a$ ($m$ times) $\cdot aa\cdots a$ ($n$ times) $=a^{m+n}$
	- $(a^{m})^{n}=a^{m}a^{m}\cdots a^{m}$ ($n$ times) $=aa\cdots a$ ($mn$ times)$=a^{m}n$
	- $a^{-n}=a^{-1}\cdots a^{-1}=(a^{-1})^{n}$, 
		- so $(a^{n})^{-1}=(aa\cdots a)^{-1}=a^{-1}a^{-1}\cdots a^{-1}=a^{-n}$
	- there also exists cases where $m,n$ are $0$ or negative

## Division algorithm

> [!definition]
> If $m$ and $n$ are integers and $n$ is positive, there exists unique integers $q$ and $r$ such that: $$m=nq+r\ \ \wedge \ \ 0\leq r\leq n$$ ... where $q$ is the *quotient* and $r$ is the *remainder*.

Take the division algorithm to be a **postulate** of the system of integers.

> [!theorem]
> Let $G$ be a group, and $a$ and element of $G$. If there exists a nonzero integer $m$ such that $a^{m}=e$, then there exists a positive integer $n$ such that $a^{n}=e$: $$\exists\ m\neq0\text{ s.t. }a^{m}=e\ \  \longrightarrow\ \  n>0\text{ s.t. }a^{n}=e$$

- if $a^{m}=e$ where $m$ is negative, then $a^{-m}=(a^{m})^{-1}=e^{-1}=e$
	- moreover, $a^{-m}=e$ where $-m$ is positive
	- necessary for next definition

> [!definition]
> Let $G$ be an arbitrary group and $a\in G$. If there exists a nonzero integer $n$ such that $a^{m}=e$, then the **order** of the element $a$ is defined to be the *least positive integer* $n$ such that $a^{n}=e$. 
> If there does not exist any nonzero integer $m$ such that $a^{m}=e$, we say that $a$ has order *infinity*.
> Formally, these statements read as the following:
> $$\forall\ x\in G\ \ \text{ord}(x)>0\  \vee\text{ord}(\infty)$$

- every element has an order, either positive or infinity
	- such element has either finite or infinite order accordingly

> [!theorem] Theorem: Powers of $a$, if $a$ has finite order.
> If the order of $a$ is $n$, there are exactly $n$ different powers of $a$, namely: $$a^{0}, a, a^{2}, a^{3}, ..., a^{n-1}$$

- every $+$ or $-$ power of $a$ is equal to one of the above
- order of $a$ in $n$, so $a^{n}=e$ w/ $n$ being the *smallest* positive integer satisfying the equation.

> [!proof]
> ==Postulate==: Every power of $a$ is equal to one of the powers of $a^{0}, a^{1}, a^{2}, ..., a^{n-1}$.
> ==Proof.== Let $a^{m}$ be any power of $a$.
> - Division algorithm ($m=nq+r,\ \ 0\leq r<n$) to divide $m$ by $n$:
> 	$$
> 	> 	\begin{align}
> 	m&=nq+r \\
> 	a^{m}&=a^{nq+r} \\
> 	&=a^{nq}a^{r} \\
> 	&=(a^{n})^{q}a^{r} \\
> 	&=e^{q}a^{r} \\
> 	&=a^{r}.
> 	\end{align}
>
> 	$$
> 	... thus, $a^{m}=a^{r}$, and $r$ is one of the integers $0,1,2,...,n-1$.
>
> ==Postulate==: $a^{0}, a^{1}, a^{2}, ..., a^{n-1}$ are unique.
> ==Proof.== by contradiction: Suppose $a^{0}, a^{1}, a^{2}, ..., a^{n-1}$ are not unique.
> - Then $a^{r}=a^{s}$ where $r,s$ are distinct integers s.t. $0<r, s<n-1$.
> - Then $r<s$ or $s<r$.
> - Take $s<r$ s.t. $0\leq s<r<n$.
> - Consequentially: $0<r-s<n$. 
> - But $a^{r}=a^{s}$, hence, $a^{r}(a^{s})^{-1}=a^{s}(a^{s})^{-1}$
> - Therefore, $a^{r}a^{-s}=e$
> - So $a^{r-s}=e$
> 	- *Contradiction*: $r-s$ must be positive integer $<n$, whereas $n$ (the order of $a$) is the *smallest* positive integer s.t. $a^{n}=e$
> - Thus, we state $a^{r}\neq a^{s}$ where $r\neq s$ for any $r,s <n-1$

> [!theorem] Theorem: Powers of $a$, if $a$ has infinite order.
> If $a$ has order infinity ( $\text{ord}(a)=\infty$ ) then all the powers of $a$ are different. That is, if $r$ and $s$ are distinct integers, then $a^{r}\neq a^{s}$

> [!proof]
> Let $r,s \in \mathbb{Z}$. By contradiction:
> - Suppose $a^{r}=a^{s}$
> - Then $a^{r}(a^{s})^{-1}=a^{s}(a^{s})^{-1}$
> - hence $a^{r-s}=e$.

> [!theorem]
> Suppose an element $a$ in a group has order $n$. Then $a^{t}=e$ *if and only if* $t$ is a multiple of $n$, i.e. $t=nq$ for some $q\in\mathbb{Z}$.

> [!proof]
> If $t=nq$, then $a^{t}=a^{nq}=(a^{n})^{q}=e^{q}=e$. Conversely, suppose $a^{t}=e$. Divide $t$ by $n$ using the [[division algorithm]]: $$t=nq+r\ \ 0\leq r<n$$... then, by simple substitution and application of exponential laws: $$e=a^{t}=a^{nq+r}=(a^{n})^{q}a^{r}=e^{q}a^{r}=a^{r}$$... thus, $a^{r}=e$ where $0\leq r<n$. If $r\neq -$ then $0<r<n$ where $n$ is the *smallest* positive integer s.t. $a^{n}=e$

