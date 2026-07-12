#ch1 
### Outline
- **Logical properties**
- **Injective/Surjective functions**

> [!definition]
> Let $A$ and $B$ be sets. A **function** $f$ from $A$ to $B$ is a subset of $A \times B$ with the property that each $x\in A$ is the first component of *precisely one* ordered pair $( x,y )$ in $f$.

> [!remark]
> 1. If $( x,y )$ and $( x,z )$ are in $f$, then $y=z$.
> 2. If $( x,y )\in f$, then we can write $y=f( x )$.
> - We say $A$ is the domain of $f$, and $B$ the codomain (range).
> - symbolically, $f:A \rightarrow B$ where $f\subseteq A \times B$
- the number of elements in $f$ is equal to the smallest number of elements between $A$ and $B$.
- domain/codomain can defined in terms of a [[sets|cartesian product]]

> [!example]
> ### Example 1.
> $$A=\left\{ -3,-2,-1,0,1 \right\},\ B=\mathbb{Z}$$
> - $f= \left\{ ( -3,2 ), ( -2,-2 ),( -1,4 ),( 0,5 ),( 1,6 ) \right\}$
- recall the definition of[[(inverse) image| image and inverse image]] of a function

#### Logical properties
> [!theorem]
> Let $f$ be a function from $A$ to $B$. If $A_1$ and $A_{2}$ are subsets of $A$, then:
> 1. $f( A_{1}\cup A_{2} )=f( A_{1} )\cup f( A_{2} )$
> 2. $f( A_{1}\cap A_{2} )\subset f( A_{1} )\cap f( A_{2} )$

> [!proof]
> ##### Proof of 2.
> 1. Let $y\in f( A_{1}\cap A_{2} )$
> 	1. $( \rightarrow )$  $\exists x\in A_{1}\cap A_{2}$ st. $y=f( x )$
> 		1. Since $x\in A_{1}\cap A_{2}$, $x\in A_{1}$ and $x\in A_{2}$
> 		2. Moreover, since $x\in A_{1}$, $f( x )\in f( A_{1} )$
> 		3. Similarly, $x\in A_{2}, y=f( x )\in f( A_{2} )$
> 		4. Finally, $y\in f( A_{1} )\cap f( A_{2} )$

> [!example]
> 2. Let $f:\mathbb{R}\rightarrow \mathbb{R}$ and $f( x )=x^{2}$.
> 3. $A_{1}=(-\infty, 0] \Rightarrow f( A_{1})=[0,\infty)$
> 4. $A_{2}=[0,\infty)=\Rightarrow f( A_{2}=[0, \infty] )$
> 5. So $A_{2}\cap A_{2}\longrightarrow f( A_{2}\cap A_{2})=\left\{ 0 \right\}$, $f( A_{1} )\cap f( A_{2} )=[0,\infty)$

> [!theorem]
> Let $f$ be a function from $A$ to $B$ and let $B_{1}, B_{2}$ be subsets of $B$.
> 1. $f^{-1}( B_{1}\cup B_{2})=f^{-1}( B_{1} )\cup f^{-1}( B_{2} )$
> 2. $f^{-1}( B_{1}\cap B_{2} )=f^{-1}( B_{1} )\cap f^{-1}( B_{2} )$
> 3. $f^{-1}( B - B_{1} )=A - f^{-1}( B_{1} )$

> [!proof]
> ##### Proof of 3.
> $$
> \begin{align} \text{Let } x&\in f^{-1}(B -B_{1}) \Leftrightarrow f( x )\in  B - B_{1} \Leftrightarrow f( x )\notin B_{1} \\ &\longrightarrow x\notin f^{-1}( B_{1} ) \\ &\longrightarrow x\in  A-f^{-1}( B_{1} )\ \cdots &&\text{ ... so }x\in  f^{-1}( B-B_{1} ). \\
> \text{Let }x&\in A-f^{-1}( B_{1} ) \Leftrightarrow x\notin f^{-1}( B_{1} ) \\ &\longrightarrow f( x )\notin B_{1} \ \cdots && \text{...so }x\in  f^{-1}( B-B_{1} )
> \end{align}
> $$
#### injective / surjective functions

> [!definition]
> A function $f:A\rightarrow B$ is **one-to-one** if: $$f( x_{1} )=f( x_{2} )\longrightarrow x_{1}=x_{2}.$$

> [!definition]
> A function $f:A\rightarrow B$ is **onto** if: $$\forall  y\in  B, \exists x\in  A\  \text{such that}\  f( x )=y.$$