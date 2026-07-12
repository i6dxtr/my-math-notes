#ch18

> [!definition]
> For [[Rings|rings]] $A$ and $B$, $A$ is *isomorphic* to $B$, written $A\cong B$, means there is a function $f:A\rightarrow B$ that is an [[isomorphism]], meaning:
> 1. $\forall x,y\in A$, $f( x+y )=f( x )+f( y )$
> 2. $\forall x,y\in A$, $f( xy )=f( x )f( y )$
> 3. $f$ is bijective

> [!remark]
> If $A\cong B$ and $A$ is a [[field]], then $B$ is also a field. Moreover, if $A$ is an [[ideal]] then so is $B$.

> [!proof] Proof of 2.
> 1. $f( ( x+yi )( z+ti ) )=f( ( xa-yt )+( xt+yz )i )=\begin{pmatrix} xz-ty&xt+yz\\-xt-yz&xz-yt \end{pmatrix}$
> 2. $f( x+yi )f( z+ti )=\begin{pmatrix} x&y\\-y&x \end{pmatrix}\begin{pmatrix} z&t\\-t&z \end{pmatrix}=\begin{pmatrix} xz-yt&xt+yz\\-yz-xt&-yt+xz \end{pmatrix}$
> 	1. ... which is the same as the first.
>
> - This proves an isomorphism from $\mathbb{C}$ and some $A\in M_{2}( \mathbb{R} )$ where $f( x+yi )=\begin{pmatrix} x&y\\-y&x \end{pmatrix}$
> 	- ... i think.
> - so $f$ inputs a complex number and produces a real $2 \times 2$ matrix representation of it.

- same as below?

> [!example]
>
> ##### 1. Proving Isomorphism
> Define $\mathbb{C}=\left\{ x+yi\ |\ x,y\in \mathbb{R} \right\}$, where $i^{2}=-1$, with the following operations:
> - $( x+yi )+( z+ti )=( x+z )+( y+t )i$
> - $( x+yi )( z+ti )=xz+xti+yiz+yiti=( xz-yt )+( xt+yz )i$
> - note that this is both a ring and a field
>
> ==Claim==: $\mathbb{C}\cong \left\{ \begin{pmatrix} a&b\\-b&a \end{pmatrix}\ |\ a,b\in \mathbb{R} \right\}$
> 1. $f( ( x+yi )( z+ti ) )=f( ( xa-yt )+( xt+yz )i )=\begin{pmatrix} xz-ty&xt+yz\\-xt-yz&xz-yt \end{pmatrix}$
> 2. $f( x+yi )f( z+ti )=\begin{pmatrix} x&y\\-y&x \end{pmatrix}\begin{pmatrix} z&t\\-t&z \end{pmatrix}=\begin{pmatrix} xz-yt&xt+yz\\-yz-xt&-yt+xz \end{pmatrix}$
> 	1. ... which is the same as the first.
>
> - This proves an isomorphism from $\mathbb{C}$ and some $M_{2}( \mathbb{R} )$ where $f( x+yi )=\begin{pmatrix} x&y\\-y&x \end{pmatrix}$ (i think)
> ##### 2. Proving Isomorphism 
> For all $m,b\in \mathbb{Z}^{+}$, if $m,n$ are relatively prime, then $\mathbb{Z}_{mn}\cong \mathbb{Z}_{m} \times \mathbb{Z}_{n}$. In particular, the function $f:\mathbb{Z}_{mn}\rightarrow\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ where $f( x )=( x\text{ mod m}, x\text{ mod }n )$ is an isomorphism.
> 1. Recall definition of [[ideal]] (moreover, the *principal ideal*)

