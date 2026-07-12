#ch5 #ch10 
- there are several uses of the term "order" in algebra. we define it for [[Groups|groups]] as follows:

> [!definition]
> Let $G$ be a group; the **order** of an *element* $a$ in $G$ is the least positive integer $n$ such that $$aaa\cdot\ \cdot\ \cdot a=e$$
> ... with $n$ factors.
> Alternatively,
> The **order** of the *group* $G$ can be defined as the number of elements in $G$. Note, the order of $G$ is denoted by $\lvert G \rvert$.

> [!remark]
> The *order* of a group is equal to its **cardinality**.

> [!corollary]
> Observe the connection between the previous two definitions:
>
> Let $a$ be an element of order $n$ in a group. Then, there are exactly $n$ powers of $a$, hence $\left\langle a \right\rangle$ has $n$ elements. Thus, $$\text{If ord}(a)=n\ \ \ \ \ \text{then }\lvert \left\langle a \right\rangle \rvert =n$$ ... that is, the order of a [[cyclic subgroup]] *is the same as the order of its [[generators|generator]].*

## Chapter 10

> [!definition]
> Let $G$ be an arbitrary [[group]] and $a\in G$. If there exists a nonzero integer $n$ such that $a^{m}=e$, then the **order** of the element $a$ is defined to be the *least positive integer* $n$ such that $a^{n}=e$. 
> If there does not exist any nonzero integer $m$ such that $a^{m}=e$, we say that $a$ has order *infinity*.
> Formally, these statements read as the following:
> $$\forall\ x\in G\ \ \text{ord}(x)>0\  \vee\text{ord}(\infty)$$

- every element has an order, either *finite* or *infinite*

> [!theorem]
> Let $G$ be a group, and $a$ and element of $G$. If there exists a nonzero integer $m$ such that $a^{m}=e$, then there exists a positive integer $n$ such that $a^{n}=e$: $$\exists\ m\neq0\text{ s.t. }a^{m}=e\ \  \longrightarrow\ \  n>0\text{ s.t. }a^{n}=e$$

- if $a^{m}=e$ where $m$ is negative, then $a^{-m}=(a^{m})^{-1}=e^{-1}=e$
	- moreover, $a^{-m}=e$ where $-m$ is positive
	- necessary for the above definition of order

> [!theorem] Theorem: Powers of $a$, if $a$ has finite order.
> If the order of $a$ is $n$, there are exactly $n$ different powers of $a$, namely: $$a^{0}, a, a^{2}, a^{3}, ..., a^{n-1}$$

every $+$ or $-$ power of $a$ is equal to one of the above
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

link [[generators]]