#ch19 

> [!definition]
> If $f:A\rightarrow B$ is a [[surjective]] [[Homomorphism|homomorphsim]] and $K=\text{ker}( f )$, where $A,B$ are rings, then $A / K\cong B$, forming an [[Isomorphism|isomorphism]].

> [!remark]
> The [[kernel]] $K=\text{ker}( f )$ is an [[ideal]], as opposed to a [[normal subgroup]] as it were for the definition of the fundamental homomorphism theorem on groups.

> [!example]
> $\mathscr{F}( \mathbb{R} ) / K=\mathbb{R}$:
> 1. For $f\in \mathscr{F}( \mathbb{R} )$, define $h:\mathscr{F}( \mathbb{R} )\rightarrow \mathbb{R}$ by $h( f )=f( 3 )$
> 2. Then:
> 	$$
> 	\begin{align} \text{ker}( h )&=\left\{ f\in  \mathscr{F}( \mathbb{R} )\ |\ h( f )=0 \right\}\\ &=\left\{ f\in  \mathscr{F}( \mathbb{R} )\ |\ \mathscr{F}( 3 )=0 \right\}\\ &=\text{ ker}( f ) \end{align}
> 	$$
> 3. ... there's more, this is unfinished

> [!proof] Proof: of the Fundamental Homomorphism Theorem for rings
> 1. Recall: [[Quotient Rings]]
> 2. Define $\Phi: A / K\rightarrow B$ by $\Phi( K+x )=h( x )$
> 	1. $x\in A\longrightarrow^{h} h( x )\in B$
> 		1. $\longrightarrow K+x\in A / K$
> 	2. $K+x\longrightarrow^{\Phi}h( x )$
> 3. We will show $\Phi$ is an isomorphism:
> 	1. The condition of the operation being well-defined and surjectivity are proven in the same manner as the [[Fundamental Homomorphism Theorem]]
> 	2. Proving homomorphism:
> 		1. Let $K+x, K+y\in A / K$
> 		2. The proof is worked as follows:
>
> $$
> \begin{align} \Phi( ( K+x )+( K+y ) )&=\Phi( K+( x+y ) )\\&=h( x+y )\\&=\Phi( ( K+x )( K+y ) )\\\Phi( K+xy )&=h( xy )\\&=h( x )h( y )\\&=\Phi( K+x )\Phi( K+y ). \end{align}
> $$

### Relationship between unity elements

> [!remark]
> Let $f:A\rightarrow B$ be a homomorphism of [[rings]]. Even if $A$ and $B$ are rings with unity, $f( 1_{A} )$ *does not* have to equal $1_{B}$. If it happens to, we call $f$ a *unital homomorphism.*

> [!example]
> ##### $A=\mathbb{Z}( 1_{A}=1 )$ and $B=\mathbb{Z} \times \mathbb{Z}( 1_{B}=( 1,1 ) )$
> 1. Define $f:\mathbb{Z}\rightarrow \mathbb{Z} \times \mathbb{Z}$
> 2. $f$ is a homomorphism:
> 	1. $f( x+x' )=( x,0 )+( x',0 )=( x+x',0 )$
> 	2. $f( xx' )=( x,0 )( x',0 )=( xx',0 )=f( x )f( x' )$
> 3. *But*, $f( 1 )=( 1,0 )\ne 1_{\mathbb{Z} \times \mathbb{Z}}$
> 	1. so $f$ is not unital.

link [[Fundamental Homomorphism Theorem]] [[Rings]] [[ideal]]