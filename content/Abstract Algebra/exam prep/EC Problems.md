## Problem 2
##### For each of the following problems, determine whether it is an isomorphism, not injective, not surjective, or not a homomorphsim.
- The function $f: \mathbb{Z}\rightarrow \mathbb{Q}^{+}$ defined by $f( n )= 2^{n}$
	- This function is *not* surjective:
		- Suppose by contradiction that $f$ is surjective
		- Then $\forall y\in \mathbb{Q}^{+}$, $\exists x\in \mathbb{Z}$ such that $f( x )=y$
		- Let $y=\frac{1}{3}$
		- Then $x=2^{n}$ or $-x=\frac{1}{2^{n}}$ 
			-  $2^{n}\neq \frac{1}{3}$ for all $n\in \mathbb{Z}^{+}$
			-  $\frac{1}{2^{n}}\neq \frac{1}{3}$ for all $n\in \mathbb{Z}^{+}$
		- So there is no $x\in \mathbb{Z}$ s.t. $f( x )=y$, a contradiction.
		- Therefore the function cannot be surjective.
- The function $f:GL_{2}( \mathbb{R} )\rightarrow\mathbb{R}^{+}$ defined by $f( A )=\text{det}( A )$
	- This function is *not* injective:
		- Suppose by contradiction that $f$ is injective
		- Then $\forall A, B\in GL_{2}( \mathbb{R} )$, $f( A )=f( B )\longrightarrow \text{det}( A )=\text{det}( B )$
		- Let $A=\begin{pmatrix} 1&0\\0&1 \end{pmatrix}$ and $B=\begin{pmatrix} 0&-1\\1&0 \end{pmatrix}$
		- So $f( A )=det( A )=( 1\cdot1-0\cdot0 )=1$
		- Moreover, $f( B )=\text{det}( B )=( 0\cdot0-(-1\cdot1) )=1$
		- We see that $f( A )=f( B )$
		- However, $A\ne B$, a contradiction
		- Therefore, the function cannot be injective.
- The function $f:\mathbb{Z}_{2} \times\mathbb{Z}_{2}\rightarrow\mathbb{Z}_{4}$ defined by $f( 0,0 )=0, f( 0,1 )=1, f( 1,0 )=2, f( 1,1 )=3$
	- This function is *not* homomorphic:
		- Suppose by contradiction that $f$ is homomorphic
		- Suppose that $f$ preserves multiplication
		- Then $f( a )f( b )=f( ab )$ $\forall a,b \in \mathbb{Z}_{2}  \times \mathbb{Z}_{2}$
		- Let $a=( 0,1 )$ and $b=( 1,0 )$
		- So $f( ab )=f( 0\cdot1, 1\cdot0 )=f( 0,0 )=0$
		- Furthermore, $f( a )f( b )=1\cdot2=2$
			- But $f( ab )=0\ne 2$, a contradiction
		- Thus, the function cannot be homomorphic
- The function $f:\mathbb{Z}\rightarrow \mathbb{Z}$ define by $f( n )=-n$
	- This function is an isomorphism:
		- It is homomorphic: let $n_{1}, n_{2}\in \mathbb{Z}$. Then $f( n_{1} )=-n$ and $f( n_{2} )=-n$, so $f( n_{1} )f( n_{2} )=( -n )( -n )=n^{2}$. Moreover, $f( n\cdot n )=-n\cdot n=n^{2}$, which is the same.
		- It is bijective: it has an inverse function $f^{-1}( x )=-x$
			- $f^{-1}( f( n ) )=f^{-1}( -n )=-( -n )=n$
			- $f( f^{-1}( x ) )=f( -x )=-( -x )=x$
		- Thus, the function is isomorphic.

##### Determine whether each of the following statements is true or false. If it is false, explain by stating that one group has a certain property(which should be preserved by isomorphisms) and that the other group does not have that property. If it is true, you do not need to explain
###### $\mathbb{Z}_{4} \times\mathbb{Z}_{9}\cong \mathbb{Z}_{36}$
*Solution:* This statement is true.
- We show there exists a bijective homomorphic function $f$ to prove isomorphism:
- *There exists a homomorphic function*: Let $f: \mathbb{Z}_{4} \times \mathbb{Z}_{9}\rightarrow \mathbb{Z}_{36}$ be a homomorphism defined as $f( a,b )=( 9a+4b )\text{ mod }36$. Let $( a_{1},b_{1} ), ( a_{2}, b_{2} )\in \mathbb{Z}_{4} \times \mathbb{Z}_{9}$. Then
	$$
	\begin{align} f( a_{1}, b_{1} )f( a_{2},b_{2} )&=( 9a_{1}+4b_{1} )+( 9a_{2}+4b_{2} )\text{ mod }36\\&=9( a_{1}+a_{2} )+4( b_{1}+b_{2} )\text{ mod 36}\end{align}
	$$
	... moreover:
	$$
	\begin{align} f( ( a_{1},b_{1} )+( a_{2},b_{2} ) ) &=f( a_{1}+a_{2}, b_{1}+b_{2} )\\&=9( a_{1}+a_{2} )+4( b_{1}+b_{2} )\text{ mod }36\end{align}
	$$
- since $f( a_{1}, b_{2} )+f( a_{2},b_{2} )=f( ( a_{1},b_{1} )+( a_{2},b_{2} ) )$, the function is homomorphic.
- $f$ *is injective*: if $f( a_{1}, b_{1} )=f( a_{2}, b_{2} )$ then $( a_{1},b_{1} )=( a_{2},b_{2} )$. So:
	$$
	\begin{align} f( a_{1},b_{1} )=9a_{1}+4b_{1}\text{ mod 36}&\equiv f( a_{2}, b_{2} ) 9a_{2}+4b_{2}\text{ mod 36}\\ 9a_{1}-9a_{2}\text{ mod }36&\equiv 4b_{2}-4b_{1}\text{ mod }36 \\ 9( a_{1}-a_{2} )\text{ mod }36&\equiv4( b_{2}-b_{1} )\text{ mod 36}   \end{align}
	$$
	... since $0\le a_{1}, a_{2} <4$ and $0\le b_{1}, b_{2}\le 9$, the left-hand side and the right-hand side are equivalent if $a_{1}=a_{2}$ and $b_{1}=b_{2}$
- $f$ *is surjective*: since $f$ is injective and $\text{ord}( \mathbb{Z}_{4} \times \mathbb{Z}_{9} )=\text{ ord}( \mathbb{Z}_{36} )$, the function must be surjective.


###### $S_{3} \times\mathbb{Z}_{4}\cong S_{4}$
*Solution*: This statement is false.
- *Counterexample*: $( ( 12 ), 0 )$ and $( e, 1 )$ commutes in ${S}_{3} \times \mathbb{Z}_{4}$, but there is no corresponding element in $S_{4}$ with order 4 that does the same.
###### $\mathbb{Z}_{5}^{*}\cong \mathbb{Z}_{4}$
*Solution:* This statement is true.
- We show there exists a bijective homomorphic function $f$ to prove isomorphism:
- There exists a homomorphsim: let $f:\mathbb{Z}_{5}^{*}\rightarrow\mathbb{Z}_{4}$ be a homomorphism defined $f( x )=2^{n}\text{ mod }5$
- $f$ *is bijective*: so $\forall x_{1}, x_{2}\in \mathbb{Z}_{5}^{*}$, $f( x_{1} )=f( x_{2} )\longrightarrow x_{1}=x_{2}$ and $\forall x\in \mathbb{Z}_{5}^{*}$ $\exists y\in \mathbb{Z}_{4}$ such that $f( x )=y$. Taking each $x$ and computing gives the following: 
	- $f( 0 )=2^{0}\text{ mod }5=1\text{ mod }5=1$
	- $f( 1 )=2^{1}\text{ mod }5=2\text{ mod 5}=2$
	- $f( 2 )=2^{2}\text{ mod }5=4\text{ mod 5}=4$
	- $f( 3 )=2^{3}\text{ mod }5=8\text{ mod }5=3$
- Clearly, $f$ is bijective.
###### $\mathcal{P}( \left\{ 1,2,3 \right\} )\cong \mathbb{Z}_{8}$
*Solution:* This statement is false
- *Counterexample:* the orders of elements $\mathcal{P}( \left\{ 1,2,3 \right\} )$ and $\mathbb{Z}_{8}$ are unequal. All non-identity element of $\mathcal{P}( \left\{ 1,2,3 \right\} )$ has order 2, while $2\in \mathbb{Z}_{8}$ has order 6. Thus, there are elements for which the isomorphism does not preserve order.
###### $\mathbb{Z}_{3} \times \mathbb{Z}_{4}\cong A_{4}$
*Solution:* This statement is false
	- *Counterexample:* In $( 1,1 )\in\mathbb{Z}_3 \times \mathbb{Z}_4$ has order 12, while the maximum order of any element in $A_{4}$ is 3, since $A_{4}$ has it's largest cycle being the 3-cycles. Thus, there are elements for which the isomorphism does not preseve order.


### Problem 3
##### Let $f:G_{1}\rightarrow G_{2}$ be a homomorphsim. Use fact: $f( e_{1} )=e_{2}$ and $f( x^{-1} )=f( x )^{-1}$
###### Prove that $\text{ker}( f )$ is a normal subgroup of $G_{1}$
- Define $\text{ker}( f )=K=\left\{ x\in G_{1} |\ f( x )=e_2 \right\}$. 
- We show $\text{ker}( f )$ is a normal subgroup: $\forall a\in H$ and $\forall x\in G_{1}$, $xax^{-1}\in H$.
	- We'll show $xax^{-1}\in G_{2}$:
-  $f( xax^{-1} )=f( x )f( a )f( x^{-1} )$ by definition of homomorphism.
-  Observe: $f( a )=e_{2}$
-  So $f( x )f( a )f( x^{-1} )=f( x )e_{2}f( x^{-1} )=f( x )f( x^{-1} )$
-  Applying fact: $f( x )f( x^{-1} )=f( x )f( x )^{-1}$
- So $f( xax^{-1} )=f( x )\left[ f( x )^{-1} \right]=e\in \text{ker}( f )$
-  Thus, $\text{ker}( f )$ is a normal subgroup.


###### Prove that it is a subgroup *and* that it is normal
- *Closed under operation:* Let $a,b\in \text{ker}( f ).$
-  We'll show $ab\in \text{ker}( f )$
	- $f( ab )=f( a )f( b )$ since $f$ is homomorphic
	- So $f( a )=e_{2}$ and $f( b )=e_{2}$
	- Then $f( ab )=e_{2}e_{2}=e_{2}$
	- Thus, $ab\in \text{ker}( f )$
-  *Contains identity:*
	- $f( e_{1} )=e_{2}$
	- so $e_{1}\in \text{ker}( f )$.
- So $\text{ker}( f )$ is a normal subgroup.

##### In the group $S_{3}$, let $H$ be the cyclic subgroup generated by $( 123 )$.
###### Find all distinct right cosets of $H$ in $S_{3}$
- Compute $\left\langle ( 123 ) \right\rangle$:  $\left\langle ( 123 ) \right\rangle=\left\{ e,( 123 ),( 132 ) \right\}$ 
- $S_{3}$ has order 6, and cosets $H( 123 )$ should partition $S_{3}$
	- $He=H=\left\{ 3,( 123 ),( 132 ) \right\}$
	- $H( 12 )=\left\{ ( 12 ),( 13 ),( 23 ) \right\}$
- Since the 6 elements in $S_{3}$ are accounted for, these are the distinct right cosets partitioning $S_{3}$.

###### Find all distinct left cosets of $H$ in $S_{3}$
- Similarly to the right cosets:
-  $eH = H = \{e, (123), (132)\}$
- $(12)H = \{(12), (23), (13)\}$
- Since the 6 elements in $S_{3}$ are accounted for, these are the distinct left cosets partitioning $S_{3}$.
###### Is $H$ a normal subgroup of $S_{3}$? You don't need to explain.
- $H$ is a normal subgroup of $S_{3}$, since $H$ has index 2, i.e., the number of distinct right cosets is equal to 2.

