
### 5.6 Discrete Fourier Analysis
- involves decomposing signals into fundamental periodic constituents
	- namely, *sine* and *cosine*, or *complex exponentials*
- such signals can compose an [[orthogonal bases|orthogonal basis]] when expressed as complex exponentials
- the *Fast Fourier Transform* is an efficient algorithm that can compute the discrete Fourier representation of signals, as well as signal reconstruction given from the Fourier coefficients

#### Singular-dimension
- Define $f(x)$ on $a\le x\le b$
- Computer stores measured values w/ a finite # of sample points
	- $a\le x_{0} < x_{1}< \cdots<x_{n}\le b$
	- such points are equally spaced such that:
		$$
		\begin{align} x_{j}=a+jh,&&j=0,...,n\\\text{...where}&&h=\frac{b-a}{n} \end{align}
		$$
		... indicates the sample rate.
	- $x$ represents time
		- $x_{j}$ being the times at which we sample signal $f( x )$
		- can be high (every 10-20ms)
	- adopt "standard" interval of $0\le x\le 2\pi$ with $n$ equally spaced sample points:
		$$
		\begin{align} x_{0}&=0, &x_{1}&=\frac{2\pi}{n}, &x_{2}&=\frac{4\pi}{n},\\\cdots&& x_{j}&=\frac{2j\pi}{n}&&\cdots \\\cdots& &x_{n-1}&=\frac{2(n-1)\pi}{n}&&\cdots\end{align}
		$$
- sampling a (complex-valued) signal or function $f( x )$ produces the *sample vector*: $$\mathbf{f}=\left(  f_{0}, f_{1}, ..., f_{n-1} \right)^{T}=\left( f( x_{0} ),f( x_{1} ),...,f( x_{n-1} ) \right)^{T}$$... where $f_{j}=f( x_{j} )=f\left(\frac{2j\pi}{n}\right),\ \ j=0,...,n-1$.
- sampling can't distinguish btwn functions w/ same values at all sample points
	- *e.g.* $f( x )=e^{inx}=\text{cos}(nx)+i\sin( nx )$ (complex exponential function) ![[Pasted image 20241103190348.png]]
- equally spaced sample points *cannot* detect periodic signals of frequency $n$
	- *e.g.* $e^{i( k+n )x}$ and $e^{ikx}$ are indistinguishable
- we only need to use the first $n$ periodic complex exponential functions in order to represent any $2\pi$ periodic sampled signal
	- *e.g.* $f_{0}( x )=1, f_{1}( x )=e^{ix}, f_{2}( x )=e^{2ix}, ..., f_{n-1}( x )=e^{( n-1 )ix}$
- exponentials $e^{-ikx}$ of "negative" frequency can be converted to positive:
	- negative $\rightarrow$ positive: $e^{-1kx}\rightarrow e^{i( n-k )x}$ 
	- *e.g.* $e^{-ix}=\cos( x )-i\sin( x )$ and $e^{( n-1 )ix}=\cos( n-1 )x+i\sin( n-1 )x$ have identical values
- note that while the functions have the same sample points, the actual function behavior can differ significantly
	- this is called *aliasing*
- the *discrete Fourier representation* decomposes a sampled function $f( x )$ into a linear combination of complex exponentials
- than be expressed as a finite linear combination: $$f( x )\sim p( x )=c_{0}+c_{1}e^{ix}+c_{2}e^{2ix}+\cdots+c_{n-1}e^{( n-1 )ix}=\sum_{k=0}^{n-1}c_{k}e^{ikx}$$... of the first $n$ exponentials
	- $\sim$ means $f( x ), p( x )$ agree on sample points 
		- ... s.t. $f( x_{j} )=p( x_{j} )$ for $j=0,...,n-1$
		- interpret $p( x )$ to be a complex-valued interpolation trigonometric polynomial of degree $\le n-1$ for sample data $f_{j}=f( x_{j} )$

> [!remark]
> Since the finite-dimensional complex vector space $\mathbb{C}^{n}$ is the vector space, the discrete Fourier series can be reformulated in vectorial form:
> $$
> \begin{align} \psi_{k}&=( e^{ikx_{0}}, e^{ikx_{1}}, e^{ikx_{2}},...,e^{ikx_{n-1}} )^{T} \\ &=( 1, e^{2k\pi i / n}, e^{4k\pi i / n}, ..., e^{2( n-1 )k\pi i / n} )^{T}\end{align}
> $$
> ... where $k=0,...,n-1$. Thus, these conditions of sample point concurrence between the function and the sum can be recast into the equivalent form: $$\mathbf{f}=c_{0}\psi _{0}+c_{1}\psi _{1}+\cdots+c_{n-1}\psi _{n-1}$$

- i.e. to compute Fourier coefficients $c_{0},...,c_{n-1}$ of $f$, we have to rewrite sample vector $\mathbf{f}$ as a linear combination of the sampled exponential vector $\psi _{0},...,\psi_{n-1}$.

Crucially, $\psi$ vectors being orthonormal allows us to perform Fourier analysis in the first place:

> [!definition]
> The sampled exponential vectors $\psi _{0}, ..., \psi_{n-1}$ form an [[orthogonal bases|orthonormal basis]] of $\mathbb{C}^{n}$ with respect to the inner product: $$\left\langle \mathbf{f}, \mathbf{g} \right\rangle=\frac{1}{n}\sum_{j=0}^{n-1}f_{j}\overline{g}_{j}=\frac{1}{n}\sum_{j=0}^{n-1}f( x_{j} )\overline{g( x_{j} )},\ \ \text{for some}\ \mathbf{f},\mathbf{g}\in \mathbb{C}$$
>             ![[Pasted image 20241103233940.png]]

> [!proof]
> 1. Largely relies on the properties of complex numbers:
> 	1.  $\zeta_{n}=e^{2\pi i / n}=\cos\left(  \frac{2\pi}{n}  \right)+i\sin\left(  \frac{2\pi}{n}  \right)$
> 		1. where $n=1,2,3,...$
> 2. Particular cases:
> 	1. $\zeta_2=-1$
> 	2. $\zeta_{3}=-\frac{1}{2}+\frac{\sqrt{3}}{2}i$
> 	3. $\zeta _{4}=i$
> 	4. ... and $\zeta_{8}=\frac{\sqrt{2}}{2}+\frac{\sqrt{2}}{2}i$
> 3. $n^{th}$ power of $\zeta_{n}$: $$\zeta_{n}^{n}=( e^{2\pi\ i / n} )^{n}=e^{2\pi i}=1$$... therefore $\zeta_{n}$ is one of the complex $n^{th}$ *roots of unity*
> 	1. $\zeta_{n}=\sqrt[n]{1}$
> 	2. also known as the *primitive* $n^{th}$ *root of unity*.
> 		1. since it generates all the others, see...
> 4. There are $n$ distinct complex $n^{th}$ roots of $1$
> 	1. including itself (the powers of $\zeta_{n}$): $$\zeta_{n}^{k}=e^{2k\pi i / n}=\cos \left(  \frac{2k\pi}{n}  \right)+i\sin\left(  \frac{2k\pi}{n}  \right)$$... where $k=0,...,n-1$
> 5. Geometrically:
> 	1. first encounter primitive root $\zeta_{n}$, the first vertex as we follow figure counterclockwise
> 	2. other roots appear in natural order
> 		1. $\zeta_{n}^{2}\ \rightarrow \zeta_{n}^{3}\rightarrow\cdots\rightarrow \zeta_{n}^{n-1}$
> 		2. ... till we cycle to $\zeta_{n}^{n}=1$.
> 6. The complex conjugate of $\zeta_{n}^{}$ is the "last" $n^{th}$ root: $$e^{-2\pi\ i / n}=\overline{\zeta_{n}^{}}=\frac{1}{\zeta_{n}^{}}=\zeta_{n}^{n-1}=e^{2( n-1 )\pi\ i/ n}$$
> 7. The complex numbers are a complete set of roots of $z^{n}-1$
> 	1. thus, can be completely factored: 
> 		1. $z^{n}-1=( z-1 )( z-\zeta_{n}^{} )( z-\zeta_{n}^{2} )\cdots ( z-\zeta_{n}^{n-1} )$
> 	2. Observe the real factorization: 
> 		1. $z^{n}-1=( z-1 )( 1+z+z^{2}+\cdots+z^{n-1} )$
> 	3. Comparing both: 
> 		1. $1+z+z^{2}+\cdots+z^{n-1}=( z-\zeta_{n}^{} )( z-\zeta_{n}^{2} )\cdots( z-\zeta_{n}^{n-1} )$
> 	4. Substituting $z=\zeta_{n}^{k}$ to both sides to deduce:
> 		1. $1+\zeta_{n}^{k}+\zeta_{n}^{2k}+\cdots+\zeta_{n}^{( n-1 )k}=\begin{cases} n,&k=0\\0,&0<k<n \\ \end{cases}$
> 	5. ... which is easily generalizable to the integers $k$
> 8. Rewrite sampled exponential vectors in terms of $n^{th}$ roots of unity:
> 	1. $\psi=( 1,\zeta_{n}^{k},\zeta_{n}^{2k},\zeta_{n}^{3k},...,\zeta_{n}^{( n-1 )k} )^{T}$
> 	2. ... where $k=0,...,n-1$
> 9. Apply above expression and conclude: $$\left\langle \psi_{k}, \psi _{l} \right\rangle=\frac{1}{n}\sum_{j=0}^{n-1}\zeta_{n}^{jk}\overline{\zeta_{n}^{jl}}=\frac{1}{n}\sum_{j=0}^{n-1}\zeta_{n}^{j( k-l )}=\begin{cases} 1,&k=l\\0,&k\neq l \\ \end{cases} $$... for $0\leq k$ and $l<n$. Thus, we establish normality of the sampled exponential vectors.

- Orthonormality of basis vectors implies the Fourier coefficient can be computed by taking inner products:
	$$
	\begin{align} c_{k}&=\left\langle \mathbf{f}, \psi_{k} \right\rangle\\&=\frac{1}{n}\sum_{j=0}^{n-1}f_{j}\ \overline{e^{ikx_{j}}} \\&= \frac{1}{n}\sum_{j=0}^{n-1}f_{j}e^{-ikx_{j}}\\&=\frac{1}{n}\sum_{j=0}^{n-1}\zeta_{n}^{-jk}f_{j}.\end{align}
	$$
	... note how $c_{k}$ obtained by averaging sampled values of $f(x)e^{-ikx}$, the product function
- Passage from signal $\rightarrow$ Fourier coef. is known as the **discrete Fourier transform** (DFT)
	- the reverse process called the *inverse* discrete Fourier transform

### Fast Fourier Transform
1. Fix $n=2^{l}$ where $l\ge1$
2. choose two ways to compute roots of unity:
	1. $\zeta_{n}^{2}=( e^{2\pi i / n} )=e^{2\pi i / ( n / 2 )}=\zeta_{_{n / 2}}^{}$
	2. $\zeta_{n}^{n / 2}( e^{2\pi i / n} )^{n / 2}=e^{\pi i}=-1$
3. Fix $f=\begin{pmatrix} f_{0}\\f_{1}\\f_{2}\\\cdots\\f_{n-1} \end{pmatrix}\in \mathbb{C}^{n}$
4. Define the following (where $0\le k\le n-1$): 
	1. $f_{\text{even}}=\begin{pmatrix} f_{0}\\f_{2}\\f_{4}\\\cdots\\f_{n-2} \end{pmatrix}\in \mathbb{C}^{n / 2}$
	2. $f_{\text{odd}}=\begin{pmatrix} f_{1}\\f_{3}\\f_{5}\\\cdots\\f_{n-1} \end{pmatrix}\in\mathbb{C}^{n /  2}$
5. By definition of matrix multiplication, the following formula can be used to compute the discrete Fourier transform:
	$$
	\begin{align} \text{DFT}_{n}( f )\left[ k \right]&=\frac{1}{n}\sum_{j=0}^{n-1}\zeta_{n}^{-jk}f\left[ j \right] \\
	&= \frac{1}{n}\sum_{j=0}^{n / 2-1}\zeta_{n}^{-2jk}f_{\text{even}}\left[ j \right]+\frac{1}{n}\sum_{j=0}^{n / 2-1}\zeta_{n}^{-2( 1j+1 )k}f_{\text{odd}}\left[ j \right] \\
	&= \frac{1}{n}\sum_{j=0}^{n / 2-1}\left( \zeta_{n}^{2} \right)^{-jk}f_{\text{even}}\left[ j \right]+\frac{1}{n}\zeta_{n}^{-k}\sum_{j=0}^{n / 2-1}\left(\zeta_{n}^{2}\right)^{jk} f_{\text{odd}}\left[ j \right]
	\\ &=\frac{1}{n}\sum_{j=0}^{n / 2-1}\left(\zeta_{\frac{n}{2}}^{}\right)^{-jk}f_{\text{even}}\left[ j \right]+\frac{1}{n}\zeta_{n}^{-k}\sum_{j=0}^{n/2-1}\left(\zeta_{\frac{n}{2}}^{} \right)f_{\text{odd}}\left[ j \right]
	\end{align}
	$$
6. Suppose $0\le k\le \frac{n}{2}-1$; then rewrite sum in terms of $\text{DFT}_{\frac{n}{2}}$.
	1. Use fact: $$\frac{1}{n}=\frac{1}{2}\frac{1}{n / 2}$$
	2. Then compose expression: $$\text{DFT}_{n}( f )\left[ k \right]=\frac{1}{2}\text{DFT}_{\frac{n}{2}}( f_{\text{even}} )\left[ k \right]+\frac{1}{2}\zeta_{n}^{-k}\text{DFT}_{\frac{n}{2}}( f_{\text{odd}} )\left[ k \right]$$
7. Suppose $\frac{n}{2}\le k <n$
	1. Then $k=p+\frac{n}{2}$ for some $0\le p < \frac{n}{2}-1$
	2. Then compose expression: $$\zeta_{\frac{n}{2}}^{-jk}=\zeta_{\frac{n}{2}}^{-j\left(  p+\frac{n}{2}  \right)}=\left( \zeta_{\frac{n}{2}}^{\frac{n}{2}} \right)^{-j}\zeta_{\frac{n}{2}}^{-jp}=1^{-j}\zeta_{\frac{n}{2}}^{-jp}=\zeta_{\frac{n}{2}}^{-jp}$$
	3. Furthermore: $$ \zeta_{n}^{-k}=\zeta_{n}^{-\left(  p+\frac{n}{2}  \right)}= \zeta_{n}^{-p}\zeta_{n}^{-\frac{n}{2}}=-\zeta_{n}^{-p} $$
8. Make above substitutions into string of equalities to construct expression: $$\text{DFT}_{n}( f )[p]=\frac{1}{2}\text{DFT}_{\frac{n}{2}}\left( f_{\text{even}} \right)+\frac{1}{2}\zeta_{n}^{-p}\text{ DFT}_{\frac{n}{2}}\left( f_{\text{odd}} \right)\left[ p \right]\ \ \text{... for }p=0,1,..., \frac{n}{2}-1$$
9. Set the following: $$Z=\begin{pmatrix} \zeta_{n}^{-0}\\\zeta_{n}^{-1}\\\zeta_{n}^{-2}\\\cdots\\\zeta_{n}^{-\left(  \frac{n}{2}-2  \right)}\\\zeta_{n}^{-\left(  \frac{n}{2}-1  \right)} \end{pmatrix}$$
10. Then:
	1. $x_{\text{top}}:=\frac{1}{2}\text{ DFT}_{\frac{n}{2}}( f_{\text{even}} )+\frac{1}{2}Z*\text{DFT}_{\frac{n}{2}}( f_{\text{odd}} )\in \mathbb{C}^{\frac{n}{2}}$
	2. $x_{\text{bottom}}:=\frac{1}{2}\text{DFT}_{\frac{n}{2}}( f_{\text{even}} )-\frac{1}{2}Z*\text{DFT}_{\frac{n}{2}}( f_{\text{odd}} )\in \mathbb{C}^{\frac{n}{2}}$
11. Thus, we obtain: $$\text{DFT}_{n}( f )=\begin{pmatrix} x_{\text{top}}\\x_{\text{bottom}} \end{pmatrix}$$
