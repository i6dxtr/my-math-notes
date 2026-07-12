#ch20

> [!definition]
> Let $A$ be a nontrivial ring with unity. The **characteristic** of $A$ is the least $n\in \mathbb{Z}^{+}$ such that $1+1+1+\cdots+1\ (n\text{-times})=0$ where $1,0$ are the unity and zero element of $A$, respectively.

> [!remark]
> The characteristic is the *order* of $1$ in $( A,+ )$
> If no such $n$ exists (infiniteness), we say $A$ has characteristic of *zero*.

> [!example]
> ##### Ex. 1
> - The characteristic of $\mathbb{Z}_{n}$ is $n$.
> ##### Ex. 2
> - The characteristic of $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$ is $( 1,1 )$
> 	- unity is $( 1,1 )$
> 	- zero is $( 0,0 )$
> 	- $( 1,1 )+(1, 1 )=(1+1\text{ mod }2, 1+1\text{ mod }2 )=( 0,0 )$
> ##### Ex. 3
> - The characteristic of $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$ is $6$
> 	- $\mathbb{Z}_{2} \times \mathbb{Z}_{3}\cong \mathbb{Z}_{6}$

> [!remark]
> Generally, $a+a+\cdots+a$ ($n-$times) can be written as $na$:
> - where $na$ has $n\in \mathbb{Z}^{+}$ and $a\in A$
> 	- $n$ not necessarily in the ring, so this isn't necessarily the product of $2$ ring elements
> - $1+1+\cdots+1$ ($n-$times) can be written as $n1$

- If $A$ is an integral domain of characteristic $n\in \mathbb{Z}^{+}$, then every nonzero $a\in A$ has order $n$ in $( A,+ )$.
- Why?
	- $a+a+\cdots+a\ ( n\text{-times } )=a( 1+1+\cdots1 )=0$ if and only if $1+1+1=0$.

> [!theorem]
> Let $A$ be a nontrivial commutative [[ring]] with unity.
> The [[characteristic]] of an [[integral domain]] $A$ is either $0$ or a prime number.

> [!proof]
> 1. Suppose the characteristic $n$ is neither prime nor zero
> 2. Then $n=ab$ for some $a,b\in \mathbb{Z}^{+}$, $a,b<n$.
> 3. We show $A$ has zero divisors:
> 	1. $1+1+\cdots+1\ ( n\text{-times} )=0$ so $( 1+1+\cdots+1\ ( a\text{-times} ) )( 1+1+\cdots+1\ ( b\text{-times} ) )=0$
> 		1. where $a,b$ are multiplied, each being the terms in parenthesis respectively
> 		2. each are nonzero individually, since $a,b$ are less than the characteristic polynomial
> 		3. using distributive property gives $ab=( 1+1+\cdots+1 )$
> 	2. So clearly, $a,b$ are zero divisors such that $ab=0$

> [!remark]
> ##### The converse can fail!
> - $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$ has characteristic $2$ (prime) but is not an integral domain: $( 1,0 )( 0,1 )=( 0,0 )$
> 	- so the two terms on the left side are zero divisors

> [!theorem]
> Let $ab\in A$. If $A$ is an [[integral domain]] of characteristic $p$, then $( a+b )^{p}=a^{p}+b^{p}$
> - *Assumption: $p\ne 0$, therefore prime.*

> [!proof]
> 1. In any commutative ring:
> 	1. $( a+b )^{2}=a^{2}+2ab+b^{2}$
> 		1. $=a^{2}+b^{2}$ since $2ab=( 1+1 )ab=0ab=0$
> 		2. if $\text{char}=2$
> 	2. $( a+b )^{3}=a^{3}+3a^{2}b+3ab^{2}+b^{3}$
> 		1. $=a^{3}+b^{3}$ since $3a^{2}b$ and $3ab^{2}$ are $0$
> 		2. if $\text{char}=3$
> 	3. $( a+b )^{4}=a^{4}+4a^{3}+6a^{2}b^{2}+4ab^{3}+b^{4}$
> 		1. ...
> 	4. $( a+b )^{5}=a^{5}+5a^{4}b+10a^{3}b^{2}+10a^{2}b^{3}+5ab^{4}+b^{5}$
> 		1. $=a^{5}+b^{5}$ since $10a^{3}b^{2}=( 1+1+1+1+1 )2a^{2}b^{2}$
> 		2. if $\text{char}=5$

> [!remark]
> - Let $A$ be an integral domain of $\text{char}$ $p$ and $a\in A$.
> - Then $pa=a+a+\cdots+a\ ( p\text{-times} )=0$

> [!remark]
> Since $( ab )^{p}=a^{p}b^{p}$ is also true (by commutativity), then the function $f:A\rightarrow A$ where $f( x )=x^{p}$ is a homomorphism.

