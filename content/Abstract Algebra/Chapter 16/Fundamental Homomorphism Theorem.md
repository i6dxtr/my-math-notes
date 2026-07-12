#ch16

> [!definition]
> Every [[Homomorphism|homomorphic]] image of $G$ is [[Isomorphism|isomorphic]] to a [[Quotient Groups|quotient]] of $G$.
> In particular, if $f:G\rightarrow H$ is a [[surjective]] homomorphism, then $H\cong G / K$, where $K=\text{ker}( f )$, namely, the [[kernel]] of $f$.

> [!proof]
> 1. Define $\Phi:G / K\rightarrow H$
> 	1. by $\Phi( Kx )=f( x )$
> 	2. note: $\Phi( Ka )=\Phi( Kb )$
> 	3. note: $\Phi$ an isomorphism from $G / K$ to $H$.
> 2. also, $\gamma: G\rightarrow G / K$
> 	1. by $\gamma( x )=Kx$
> 	2. see [[Drawing 2024-11-04 15.30.27.excalidraw|figure]]
> 3. We show:
> 	1. $\Phi$ is well-defined
> 		1. if $Ka=Kb$ then $f( a )=f( b )$
> 		2. so $\Phi( Ka )=\Phi( Kb )$, true by lemma
> 	2. $\Phi$ is injective
> 		1. if $\Phi ( Kb )$ then $f( a )=f( b )$
> 		2. so $Ka=Kb$, true by lemma
> 	3. $\Phi$ is surjective
> 		1. Let $h\in H$
> 		2. $f$ is surjective
> 			1. $\exists a\in G$ s.t. $f( a )=h$
> 		3. So $Ka\in G / H$ and $\Phi( Ka )=f( a )=h$
> 	4. $\Phi$ is a homomorphsim
> 		1. Let $Ka,Kb\in G / H$
> 		2. $\Phi( KaKb )=\Phi( Kab )$
> 			1. $=f( ab )$
> 			2. $=f( a )f( b )$, since $f$ is homomorphic
> 			3. $=\Phi ( Ka ) \Phi( Kb )$
> 	5. *Q.E.D*

- The notions of *homomorphic image* and of [[Quotient Groups|quotient groups]] are interchangeable. 

> [!corollary] Lemma.
> 1. Given:
> 	1. $F:G\rightarrow H$, a homomorphism
> 	2. $K=\text{ker}( f )$
> 	3. some $a,b\in G$
> 2. Implies the following holds: $$Ka=Hb\Longleftrightarrow f( a )=f( b ).$$

> [!example]
> ##### $f:GL_{n}( \mathbb{R} )\rightarrow \mathbb{R}^{*}$
> 1. $f( A )=\text{det}( A )$
> 2. $K=\text{ker}( f )=SL_{n}( \mathbb{R} )$
> 3. We conclude, by the above lemma:
> 	1. $SL_{n}( \mathbb{R} )A=SL_{n}( \mathbb{R} )B\Longleftrightarrow \text{det}( A )=\text{det}( B )$
> 	2. Cosets of $SL_{n}( \mathbb{R} )$ in $GL_{n}( \mathbb{R} )$ correspond to *nonzero* real numbers
> ##### $f:\mathbb{Z}\rightarrow \mathbb{Z}_{n}, f( k )=k\text{ mod }n$
> 1. $K=\text{ker}( f )=\left\{ ...,-2n, -n, 0, n, 2n, ... \right\}=\left\langle n \right\rangle$
> 2. We conclude, by the above lemma: 
> 	1. $\left\langle n \right\rangle+a=\left\langle n \right\rangle+b\Longleftrightarrow a\text{ mod }n=b\text{ mod }n$.

> [!example]
> We look to find the homomorphic image of a quotient group which is also an isomorphism. In other words, we will find a more familiar group it's isomorphic to.
> ##### Use the Fundamental Homomorphism Theorem to compute $Gl_{n}( \mathbb{R} ) / SL_{n}( \mathbb{R} )$.
> 1. We want to define a homomorphism $f:GL_{n}( \mathbb{R} )$ with $\text{ker}( f )=SL_{n}( \mathbb{R} )$
> 	1. Define $f( A )=\text{det}( A )$
> 		1. $f:GL_{n}( \mathbb{R} )\rightarrow\mathbb{R}^{*}$ is a surjective homomorphism
> 		2. $\text{ker}( f )=SL_{n}( \mathbb{R} )$
> 2.  The Fundamental Homomorphsim Theorem thereby proves the statement: $$GL_{n}( \mathbb{R} ) / SL_{n}( \mathbb{R} )\cong \mathbb{R}^{*}.$$
> ##### Use the Fundamental Homomorphism Theorem to compute $\mathbb{Z} / \left\langle n \right\rangle$, where $n\in \mathbb{Z}^{+}$.
> 1. We want to define a homomorphism $f:\mathbb{Z}\rightarrow \mathbb{Z}_{n}$ by $f( k )=k\text{ mod }n$
> 	1. $f$ is a surjective homomorphism
> 	2. $\text{ker}( f )=\left\langle n \right\rangle$
> 2. The Fundamental Homomorphsim Theorem thereby proves the statement: $$\mathbb{Z} / \left\langle n \right\rangle\cong \mathbb{Z}_{n}. $$

link [[Homomorphism]] [[Isomorphism]] [[Quotient Groups]] [[injective]]