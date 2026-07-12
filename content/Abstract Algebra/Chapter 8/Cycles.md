#ch8 

> [!definition]
> Let $a_{1}, a_{2},...,a_{s}$ be distinct elements of the set $\left\{ 1,2,...,n \right\}$. The **cycle** $(a_{1}a_{2}\cdots a_{s})$ is the permutation $a_{1}\rightarrow a_{2}\rightarrow a_{3}\rightarrow\cdots\rightarrow a_{s-1}\rightarrow a_s$ of $\left\{ 1,2,...,n \right\}$ with remaining elements of $\left\{ 1,2,...,n \right\}$ remaining fixed.

> [!example]
> In $S_{5}$, the cycle $(254)$ is the permutation $$\begin{pmatrix} 1&2&3&4&5 \\ 1&5&3&2&4 \end{pmatrix}$$

- notice how in the example above, $2$ maps to $5$, and $4$ maps to $2$, such that $\cdots \rightarrow 2\rightarrow 5\rightarrow 4\rightarrow2\rightarrow\cdots$

- A [[composition]] of 2 cycles can be formed as you'd expect
	- typically called the *product* of two cycles

> [!example]
> $$
> > \begin{align}
> (245)(124)&=
> \begin{pmatrix}
> 1&2&3&4&5 \\ 1&4&3&5&2
> \end{pmatrix}\circ
> \begin{pmatrix}
> 1&2&3&4&5 \\ 2&4&3&1&5
> \end{pmatrix}\\ &=
> \begin{pmatrix}
> 1&2&3&4&5 \\ 4&5&3&1&2
> \end{pmatrix}
> \end{align}
>
> $$
>
> Let $\alpha=(245)$ and $\beta=(124)$:
> - $\beta$ performs $1\rightarrow2$; $\alpha$ performs $2\rightarrow4$
> 	- $\alpha\beta$ performs $1\rightarrow4$
> - $\beta$ performs $2\rightarrow4$; $\alpha$ performs $4\rightarrow5$
> 	- $\alpha\beta$ performs $2\rightarrow5$
> - $\beta, \alpha$ leaves $3$ fixed; composite does the same
> 	- $\alpha\beta$ leaves $3$ static
> - $\beta$ leaves $5$ fixed; $\alpha$ performs $5\rightarrow2$
> 	- $\alpha\beta$ performs $5\rightarrow2$

- If $(a_{1}a_{2}\cdots a_{s})$ is a cycle, the integer $s$ is called its *length*
- If two cycles have no elements in common, they are considered [[disjoint cycles]]
	- such cycles are commutative

