#ch17

> [!definition]
> A **ring** is some set $A$ with two (abstract) operations, $+$ and $\cdot$, which are analogous to the standard operations of addition and multiplication such that:
> 1. $( A,+ )$ is an [[abelian]] [[Groups|group]]
> 2. $( A, \cdot )$ is associative
> 3. $\cdot$ distributes over addition: 
> $$
> \begin{align} a\cdot( b+c )=a\cdot b+a\cdot c&&\text{ and...}\\( b+c )\cdot a=b\cdot a+c \cdot a \end{align}
> $$

- from the definition, we derive the [[ring axioms]].
- if there exists an identity element for the $\cdot$ operation, we call it the [[unity]].
- if a ring is contained inside another ring, we call it a [[subring]].

> [!example] Examples of Rings
> 1. $\mathbb{Z}$ under ordinary addition, multiplication
> 2. $\mathbb{Q}$, same as above
> 3. $\mathbb{R}$, same as above
> 4. $M_{n}( \mathbb{R} )$ with matrix addition and multiplication
> 5. $\mathbb{Z}_{n}$ with addition/multiplication $\text{mod }n$
> 6. $\mathcal{P}( S )$ with $X+X=( X / Y )\cup ( Y / X )$ and $XY=X\cap Y$
> 	1. We know $( \mathcal{P}( S ),+ )$ is an abelian group
> 	2. $\cap$ is associative
> 		1. $( x\cap y )\cap z$ [[Drawing 2024-11-08 15.08.03.excalidraw|figure]]
> 		2. $x\cap( y\cap z )$ [[Drawing 2024-11-08 15.08.18.excalidraw|fig]]
> 		3. $X\cap( Y+z )$ [[Drawing 2024-11-08 15.09.27.excalidraw|fig]]
> 		4. $Y+Z$ [[Drawing 2024-11-08 15.09.56.excalidraw|fig]]
> 		5. $( X\cap Y )+( X\cap Z )$ [[Drawing 2024-11-08 15.10.54.excalidraw|fig]]
> 		6. $X\cap Y$ [[Drawing 2024-11-08 15.11.32.excalidraw|fig]]
> 		7. $X \cap Z$ [[Drawing 2024-11-08 15.12.24.excalidraw|fig]]
> 	3. $\cap$ distributes over $+$:
> 		$$
> 		\begin{align} X+Y&=( X\cap Y^{c} )\cup ( Y\cap X^{c} )\\X\cap( y+z )&=x\cap \left(( y\cap z^{c} )\cup ( z\cap y^{c} )\right)\\&=( x\cap y\cap z^{c} )\cup ( x\cap z\cap y^{c} )\\( x\cap y )&=\left(\left( x\cap y \right)\cap ( x\cap z )^{c}\right)\cup ( ( x\cap z )\cap ( x\cap y )^{c} )\\&=( ( x\cap y )\cap ( x^{c}\cup z^{c} ) )\cup ( ( x\cap z )\cap ( x^{c}\cup y^{c} ) )\\&=( ( ( x\cap y )\cap x^{c} )\cup ( ( x\cap y )\cap z^{c} ) )\cup ( ( x\cap z )\cap x^{c} )\cup ( ( x\cup z )\cap y^{c} )\\&=( x\cap y\cap z^{c} )\cup ( x\cap z\cap y^{c} ) \end{align}
> 		$$
> ##### Expanding off examples
> 1. $\mathbb{Z}, \mathbb{Q}, \mathbb{R}$
> 2. $M_{n}( \mathbb{R} ),\mathbb{Z}_{n}, P( S )$
> 3. $\mathscr{F}(\mathbb{R})=\left\{ f\ |\ f:\mathbb{R}\rightarrow\mathbb{R} \right\}$ 
> 	1. with operations $+, \cdot$ defined pointwise:
> 		1. $( f+g )( x )=f( x )+g( x )$
> 		2. $( f\cdot g )( x )=f( x ) \cdot g( x )$

### Subtraction Operation
We can also define an operation analogous to *subtraction*:

> [!definition]
> Let $A$ with $+ ,\cdot$ be a ring. Then, **subtraction** is defined by $$a-b=a+( -b ).$$

### Trivial Ring
We call the ring $A=\left\{ 0 \right\}$ *trivial*. Technically, it is a ring with [[unity]], since $0$ satisfies the definition of multiple identity. 

> [!remark]
> In a nontrivial ring with unity, $0\ne 1$

> [!proof]
> 1. Suppose $0=1$.
> 2. WTS the ring $A$ is trivial
> 	1. Let $a\in A$. 
> 	2. WTS $a=0$
> 		1. $a \cdot 1=a \cdot 0$
> 		2. $a = 0$.
> 	3. So $a=0$
> 3. So $A$ is trivial.  *QED*

### Squares

> [!remark]
> Generally, in a ring:
> $$
> \begin{align} ( a+b )( a-b )&=( a+b )a-( a+b )b &&\text{(distrib.)}\\&=( aa+ba )-( ab+bb )&&\text{(distrib.)}\\&=a^{2}+ba-ab-b^{2}\\&=a^{2}-b^{2}. \end{align}
> $$
> ... *if* the ring is commutative.
> Similarly,
> $$
> \begin{align} ( a+b )^{2}&=( a+b )( a+b )\\&=a^{2}+ab+ba+b^{2}\\&=a^{2}+2ab+b^{2} \end{align}
> $$
> ... *if* the ring is commutative.

### Boolean Rings

> [!definition]
> A ring $A$ is a **Boolean** ring if $$a^{2}=a$$... for every $a\in A$.
> In other words, every element is [[idempotent]].

> [!remark] Properties of Boolean rings
> 1. For every $a\in A$, $a=-a$
> 2. $A$ is commutative
> 3. Every element except $0$ and $1$ is a zero divisor
> 4. $1$ is the only invertible element in $A$
> 5. Letting $a \vee b=a+b+ab$ requires the following in $A$:
> 	1. $a\vee bc=( a\vee b )( a\vee c )$
> 	2. $a\vee( 1+a )=1$
> 	3. $a\vee a=a$
> 	4. $a( a\vee b )=a$

### Homomorphsim / Kernel
- Homomorphisms are defined similarly for rings as they are for groups:

> [!definition]
> A [[homomorphism]] from a ring $A$ to a ring $B$ is a function $f:A\rightarrow B$ satisfying the following identities:
> 1. $f( x_{1}+x_{2} )=f( x_{1} )+f( x_{2} )$
> 2. $f( x_{1}x_{2} )=f( x_{1} )f( x_{2} )$

- similarly for the kernel: 

> [!definition]
> The [[kernel]] of $f$ is the set: $$K=\left\{ x\in  a: f( x )=0 \right\}.$$

- note that the kernel of $f$ is an ideal of $A$.

link [[abelian]] [[Groups]]