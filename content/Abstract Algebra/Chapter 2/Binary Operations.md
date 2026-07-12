#ch2

> [!definition]
> An operation $*$ on a set $S$ is a rule that assigns to each ordered pair $(x,y)$ of elements of $S$ an element $x*y$ of $S$.
> $$\forall x,y \in S, x*y\in S \text{ for all }x\neq y\in S$$

- basically, combining two objects to get a third object
	- denoted by an asterisk, $*$
	- addition, subtraction, multiplication, division, *min (the minimum)*, *max, avg*
		- addition specifically performed on numbers, vectors, matrices, etc.

> [!example]
> Concatenation of strings
> 	- eg. $\text{concat}(110,1011)=1101011$
> 		- or in "infix notation": $110*1011=1101011$
> - Union/intersection of sets ($A\cup B, A\cap B$)

- we can perform operations on several different [[useful sets]] that are [[Groups|groups]] 
- operations can have the properties of [[operation commutativity|commutativity]] and [[operation associativity|associativity]]

**Number of operations on a set**
- Let $S=\{ a,b \}$. An operation on $S$ is given by the following table:
$$
\begin{align}
&(a,a) &&? \\
&(a,b) &&? \\
&(b,a) &&? \\
&(b,b) &&? \\
\end{align}
\rightarrow \text{Each of these can be a or b, independently.}
$$
- Note: on a 3-element set, the number of operations is $3^{9}=19,683$
- [[Identity Element|identity elements]] of a [[useful sets|set]] for an operation $*$ are defined according to the operation

> [!example]
> *The group of integers modulo $n$*:
> - defined as $\mathbb{Z}_{n}=\{ 0,1,2,...,n-1 \}$, $+_{n}$ is addition $\text{mod }n$
> - eg. for $n=10$: 
> 	$4+_{10}9 =4+9\text{ mod }10$
> 	 $=13\text{ mod }10$
> 	 $=3$.
> 	- think of a clock
> Note: $\mathbb{Z}_{n}$ is an example of a *finite* group, so we can make an operation table
> - eg. for $n=5$:
> 	$$
> 	\begin{array}{c|cccc}
> 	\underline{t_{5}}  &  \underline{0} & \underline{1} & \underline{2} & \underline{3} & \underline{4} \\
> 	0  & 0 & 1 & 2 & 3 & 4  & \\
> 	1 & 1 & 2 & 3 & 4  & \underline{0}  & \text{: since }1+4\text{ mod }5=0\\
> 	2 & 2 & 3 & 4 & 0 & 1 &  \\
> 	3 & 3 & 4 & 0 & 1 & 2 &  \\
> 	4 & 4 & 0 & 1 & 2 & \underline{3} & \text{: since }4+4\text{ mod }5=3
> 	\end{array}
> 	$$

