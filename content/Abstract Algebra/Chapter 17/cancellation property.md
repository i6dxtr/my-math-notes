#ch17 

> [!definition]
> A [[Rings|ring]] $A$ has the **cancellation property** *if and only if*
> $$
> \begin{align} \forall a,b,c\in A&&ab=ac\ \wedge\ a\ne 0\longrightarrow b=c\\ &&ba=ca\ \wedge\ a\ne0 \longrightarrow b=c\end{align}
> $$

- is equivalent to stating the theorem below

> [!theorem]
> $A$ has the cancellation property *if and only if* $A$ has no [[zero divisors]].

> [!proof]
> 1. Suppose $A$ has the cancellation property. 
> 2. Suppose toward a contradiction it has zero divisors $ab=0$
> 	1. Then $ab=0=a0$
> 	2. Then $ab=a0$ *and* $a\neq0$
> 	3. So by contradiction, $b=0$
> 		1. But $b\ne0$, a contradiction
> 3. Conversely, suppose $A$ has no zero divisors.
> 4. WTS cancellation.
> 	1. Let $a,b,c\in A$ 
> 	2. Suppose $ab=ac$ *and* $a\ne 0$
> 	3. WTS $b=c$
> 		1. So $ab-ac=0$
> 		2. Then $a( b-c )=0$
> 		3. So $a\ne 0$ and there are no zero divisors
> 		4. So $b-c=0$
> 		5. Thus $b=c$.
> 	4. Similarly, we can show $ba=ca$ and $a\ne 0\longrightarrow b=c$

link [[Rings]] [[zero divisors]]