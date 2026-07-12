#ch17 

> [!definition]
> In a [[ring]] $A$, an **idempotent** element is an element $a\in A$ such that $a^{2}=a$.

> [!remark]
> If $A$ is an [[integral domain]], the only idempotent elements are $0$ and $1$.

> [!proof]
> Suppose $a^{2}=a$. So $a\cdot a=a\cdot1$. If $a$ is nonzero then, by cancellation, $a=1$.

> [!example]
> ##### Idempotents in $\mathbb{Z} \times \mathbb{Z}$
> 1. $( 0,0 )$
> 2. $( 1,1 )$
> 3. $( 1,0 )$
> 	1. $( 1,0 )( 1,0 )=( 1\cdot1,0\cdot0 )=( 1,0 )$
> 4. $( 0,1 )$

> [!remark]
> $\mathbb{Z} \times\mathbb{Z}$ is not an integral domain, since $( 1,0 )$ and $( 0,1 )$ are zero divisors: $$( 1,0 )( 0,1 )=( 1\cdot0 ,0\cdot1 )=( 0\cdot0 ).$$... we can also see failure of cancellation directly: $$( 1,0 )( 0,2 )=( 1,0 )( 0,3 )=( 0,0 )\text{  but, }( 0,2 )\ne( 0,3 )$$

> [!example]
> ##### Idempotents in $\mathcal{P}( S )$
> - Namely, all elements are idempotent
> - This is called a *Boolean* ring: $$\forall a\in \mathcal{P}( S ),a^{\cap}a=a.$$
> ##### Idempotents in $\mathbb{Z}_{10}$
> 1. $0^{2}=0$
> 2. $1^{2}=1$
> 3. $5^{2}=5$
> 4. $6^{2}=6$

> [!remark]
> If $f:A\rightarrow B$ is an [[isomorphism]] and $a\in A$ is idempotent, then so is $f( a )\in B$.

> [!example]
> ##### $\mathbb{Z}_{10}\cong \mathbb{Z}_{2} \times\mathbb{Z}_{5}$ by $f( k )=( k\text{ mod }2 , k\text{ mod }5 )$
> 1. $f( 0 )=( 0,0 )$
> 2. $f( 1 )=( 1,1 )$
> 3. $f( 5 )=( 1,0 )$
> 4. $f( 6 )=( 0,1 )$

link [[Rings]] 