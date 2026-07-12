#ch2

> [!definition]
> An identity element of $S$ for $*$ means an element $e\in S$ such that: $$\forall x \in S\ \ e*x=x,\ x*e=x$$

- ex. $0$ is the identity element of $\mathbb{R}$ for $+$:
	- $\forall x\in \mathbb{R}\ \ 0+x=x,\ x+0=x$
- ex. 1 is the identity element of $\mathbb{R}$ for $\cdot$ is $1$:
	- $\forall x \in \mathbb{R}\ \ 1x=x, x1=x$
- note: if the identity element exists in a set, then we can define the [[inverse elements]] of the set

> [!example]
> $S=M_{2}(\mathbb{R})=$ the set of all $2 \times2$ matrices:
> - Identity matrix for $+$ is $0$:
> 	$$
> 	0=
> 	\begin{pmatrix}
> 	0 & 0 \\
> 	0 & 0
> 	\end{pmatrix}
> 	$$
> - Identity element for $\cdot$ is $I$:
> 	$$
> 	I=
> 	\begin{pmatrix}
> 	1 & 0 \\
> 	0 & 1
> 	\end{pmatrix}
> 	$$

> [!example]
> **Is there an identity element for concatenation of strings?**
> *Solution*: Yes, the empty string " "
> $$\text{" " } \times\ l_{1}l_{2}...l_{n} = l_{1}l_{2}...l_{n}$$
> - order doesn't matter here
> - quotes = empty string
>
> **Is there an identity element for $\cup$?**
> *Solution*: Yes, the empty set
>
>
> **Is there an identity element of $\mathbb{P}(\mathbb{Z})$ for $\cap$?**
> *Solution*: Yes, $\mathbb{Z}$: $\forall A \in \mathbb{P}(\mathbb{Z}),\ \ \mathbb{Z}\cap A=A,\ A\cap \mathbb{Z}=A$
> $\mathbb{P}(\{ 1,2,3 \})=\{ \text{empty set}, \{ 1 \}, \{ 2 \}, \{ 3 \}, \{ 1,2 \}, \{ 1,3 \}, \{ 2,3 \}, \{ 1,2,3 \} \}$
> $\mathbb{P(\mathbb{Z})}$ = the set of all subsets of $\mathbb{Z}$ (power set of $\mathbb{Z}$).

> [!corollary]
> The identity element (of $S$ for $*$) is unique, if it exists.

> [!proof]
> Suppose $e_{1}, e_{2}\in S$ are both identity elements of $S$.
> - WTS: $e_{1}=e_{2}$
> $$
> > \begin{align}
> e_{1}*e_{2}&=e_{1}&&\text{because }e_{2}\text{ is an identity element} \\
> e_{1}*e_{2}&=e_{2}&&\text{because }e_{1}\text{ is an identity element}
> \end{align}
> $$
> So $e_{1}=e_{2}$.

- Identity elements do not always exist:

> [!example]
> $\mathbb{Z}^{+}=\{ 1,2,3,... \}$ has no identity element for $+$. Why?:
> Let $e\in \mathbb{Z}^{+}$.
> - WTS: $e$ is *not* an identity element
> $e+x>x\text{ (since }e>0\text{)}$
> *OR*...
> Suppose toward a contradiction that $e+x=x$. then $e=0$ (subtract $x$ from both sides). But $0\notin \mathbb{Z}^{+}$, a contradiction.

