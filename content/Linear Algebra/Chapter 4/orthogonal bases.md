#ch4
- a vector space $V$ can admit a [[basis]] consisting of mutually [[Orthogonality|orthogonal]] elements:

> [!definition]
> A basis $\mathbf{u}_{1}, ..., \mathbf{u}_{n}$ of an $n-$dimensional inner product space $V$ is called *orthogonal* if $\left\langle \mathbf{u}_{i}, \mathbf{u}_{j} \right\rangle=0\ \forall i\neq j$. The basis is called *orthonormal* if, in addition, each vector has unit length:
> $$\lvert \lvert \mathbf{u}_{i} \rvert  \rvert =1,\ \ \forall i=1,...,n$$

- ex. of orthonormal basis: the standard basis in $\mathbb{R}^{n}$

- since basis cannot contain zero vector, we have to convert an orthogonal basis to an orthonormal basis
	- replacing each basis vector w/ a unit vector pointing in the same direction
	- recall unit vector

> [!corollary]
> If $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ is an orthogonal basis of a vector space $V$, then the normalized vectors: $$\mathbf{u}_{i}=\mathbf{v}_{i}/ \lvert \lvert \mathbf{v}_{i} \rvert \rvert,\ i=1$$... form an orthonormal basis.

- computations with orthogonal bases are much easier to perform than with non-orthogonal bases
	- finding any coordinate in a space w/ basis can be time consuming in higher dimensions (in real life applications)
	- solution is to make basis orthogonal

> [!theorem]
> Let $\mathbf{u}_{1}, ..., \mathbf{u}_{n}$ be an orthonormal basis for an [[Dot Product|inner product space]] $V$. Then one can write any element $\mathbf{v}\in V$ as a linear combination $$\mathbf{v}=c_{1}\mathbf{u}_{1}+\cdot\cdot\cdot+c_{n}\mathbf{u}_{n}$$
> ... in which its *coordinates*
> $$
> > \begin{align}
> c_{i}=\left\langle \mathbf{v},\mathbf{u}_{i} \right\rangle, &&i=1,...,n
> \end{align}
>
> $$
> ... are explicitly given as inner products. Moreover, its norm is given by the *Pythagorean formula* $$\lvert \lvert \mathbf{v} \rvert  \rvert =\sqrt{c_{1}^{2}+\cdot\cdot\cdot+c_{n}^{2}}=\sqrt{\sum_{i=1}^{n}\left\langle \mathbf{v},\mathbf{u}_{i}^{2} \right\rangle}$$
> ... namely, the square root of the sum of the squares of its orthonormal basis coordinates.

> [!proof]
> We will compute the inner product of the element $\mathbf{v}$ with one of the basis vectors. 
> Using the orthonormality conditions:
> $$
> \left\langle \mathbf{u}_{i}, \mathbf{u}_{j} \right\rangle=
> \bigg\{\begin{array}{cc}
> 0 && i\neq j \\
> 1 && i=j
> \end{array}
> $$
>    ... and bilinearity of the inner product, we obtain:
> $$\left\langle \mathbf{v},\mathbf{u}_{i} \right\rangle=\left\langle \sum_{j=1}^{n} \right\rangle c_{j}\left\langle \mathbf{u}_{j}, \mathbf{u}_{i} \right\rangle=c_{i}\lvert \lvert \mathbf{u}_{i} \rvert  \rvert ^{2}=v_{i}$$
> Proof for coordinates $c_{i}=\left\langle \mathbf{v},\mathbf{u}_{i} \right\rangle$ are as follows: $$\lvert \lvert \mathbf{v} \rvert  \rvert ^{2}=\left\langle \mathbf{v}, \mathbf{v} \right\rangle=\left\langle \sum_{j=1}^{n}c_{i}\mathbf{u}_{i} ,\ \sum_{j=1}^{n}c_{j}\mathbf{u}_{j}\right\rangle=\sum_{i,j=1}^{n}c_{i}c_{j}\left\langle \mathbf{u}_{i}, \mathbf{u}_{j} \right\rangle=\sum_{i=1}^{n}c_{i}^{2}$$

- Pythagorean-type formula is valid for *all* inner products:

> [!example] Rewrite $\mathbf{v}=(1,1,1)^{T}$ in terms of the orthonormal basis
> $$
> > \begin{align}
> \mathbf{u}_{1}=
> \begin{pmatrix}
> \frac{1}{\sqrt{6}}\\ \frac{2}{\sqrt{6}}\\-\frac{1}{\sqrt{6}}
> \end{pmatrix}, && \mathbf{u}_{2}=
> \begin{pmatrix}
> 0\\\frac{1}{\sqrt{5}}\\\frac{2}{\sqrt{5}}
> \end{pmatrix}
> ,&&
> \mathbf{u}_{3}\begin{pmatrix}
> \frac{5}{\sqrt{30}}\\-\frac{2}{\sqrt{30}}\\ \frac{1}{\sqrt{30}}
> \end{pmatrix}
> \end{align}
>
> $$
>    ... Computing dot products gives
> $$
> > \begin{align}
> \mathbf{v}\cdot\mathbf{u}_{1}=\frac{2}{\sqrt{6}},&&
> \mathbf{v}\cdot\mathbf{u}_{2}=\frac{3}{\sqrt{5}},&&
> \mathbf{v}\cdot\mathbf{u}_{3}=\frac{4}{\sqrt{30}}
> \end{align}
>
> $$
>    ... so we conclude:
> $$\mathbf{v}=\frac{2}{\sqrt{6}}\mathbf{u}_{1}+\frac{3}{\sqrt{5}}\mathbf{u}_{2}+\frac{4}{\sqrt{30}}\mathbf{u}_{3}$$

- sometimes it's more useful to work with unnormalized bases
- the process follows naturally from normalization:

> [!theorem]
> If $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ form an orthogonal basis, then the corresponding coordinates of a vector:$$\mathbf{v}=a_{1}\mathbf{v}_{1}+\cdot\cdot\cdot+a_{n}\mathbf{v}_{n}$$ ... are given by: $$a_{i}=\frac{\left\langle \mathbf{v},\mathbf{v}_{i} \right\rangle}{\lvert \lvert \mathbf{v}_{i} \rvert \rvert^{2}}$$
> In this case, its norm can be computed using the formula $$\lvert \lvert \mathbf{v} \rvert  \rvert ^{2}=\sum_{i=1}^{n}a_{i}^{2}\lvert \lvert \mathbf{v}_{i} \rvert  \rvert ^{2}=\sum_{i=1}^{n}\left( \frac{\left\langle \mathbf{v},\mathbf{v}_{i} \right\rangle}{\lvert \lvert \mathbf{v}_{i} \rvert  \rvert } \right)^{2}$$

- $a_{i}$ is directly derived from the definition of [[projection]] i.e. it *is* a projection for $\mathbf{v}$ onto itself

> [!example]
> The wavelet basis:
> $$
> > \begin{align}
> \mathbf{v}_{1}=
> \begin{pmatrix}
> 1\\1\\1\\1
> \end{pmatrix}, && \mathbf{v}_{2}=
> \begin{pmatrix}
> 1\\1\\-1\\-1
> \end{pmatrix},\mathbf{v}_{3}=
> \begin{pmatrix}
> 1\\-1\\0\\0
> \end{pmatrix}, \mathbf{v}_{4}=
> \begin{pmatrix}
> 0\\0\\1\\-1
> \end{pmatrix}
> \end{align}
>
> $$
>    ... is an orthogonal basis of $\mathbb{R}^{4}$. The norms are:
> $$
> > \begin{align}
> &\lvert \lvert \mathbf{v}_{1} \rvert  \rvert =2, &&\lvert \lvert \mathbf{v}_{2} \rvert  \rvert =2
> \\ &\lvert \lvert \mathbf{v}_{3} \rvert  \rvert =\sqrt{2}, &&\lvert \lvert \mathbf{v}_{4} \rvert  \rvert=\sqrt{2}
> \end{align}
>
> $$
> Thus, we can express any vector as a linear combination of the wavelet basis vectors, like as follows:
> $$
> \mathbf{v}=
> \begin{pmatrix}
>  4\\-2\\1\\5 
> \end{pmatrix}=2\mathbf{v}_{1}-\mathbf{v}_{2}+3\mathbf{v}_{2}-2\mathbf{v}_{4}
> $$
>    .... where the wavelet coordinates are computed directly by
> $$
> > \begin{align}
> &\frac{\left\langle \mathbf{v},\mathbf{v}_{1} \right\rangle}{\lvert \lvert \mathbf{v}_{1} \rvert  \rvert ^{2}}=\frac{8}{4}=2,\\
> &\frac{\left\langle \mathbf{v},\mathbf{v}_{2} \right\rangle}{\lvert \lvert \mathbf{v}_{2} \rvert  \rvert ^{2}}=\frac{-4}{4}=-1,\\
> &\frac{\left\langle \mathbf{v},\mathbf{v}_{3} \right\rangle}{\lvert \lvert \mathbf{v}_{3} \rvert  \rvert ^{2}}=\frac{6}{2}=3, \\
> &\frac{\left\langle \mathbf{v},\mathbf{v}_{4} \right\rangle}{\lvert \lvert \mathbf{v}_{4} \rvert  \rvert ^{2}} =\frac{-4}{2}=-2.
> \end{align}
>
> $$
> Note how much quicker this is compared to directly solving linear systems.

### Finish these (only theorems)

> [!example]
> - take $\mathbb{R}^{3}$ basis vectors that are mutually perpendicular:
> $$
> > \begin{align}
> \mathbf{v}_{1}=
> \begin{pmatrix}
> 1\\2\\-1
> \end{pmatrix}, &&\mathbf{v}_{2}=
> \begin{pmatrix}
> 0\\1\\2
> \end{pmatrix}, &&\mathbf{v}_{3}=
> \begin{pmatrix}
> 5\\-2\\1
> \end{pmatrix}
> \end{align}
>
> $$
> - divide each by its length:
> 	$$
> 	> \begin{align}
> 	\mathbf{u}_{1}=\frac{1}{\sqrt{6}}
> 	\begin{pmatrix}
> 	1\\2\\-1
> 	\end{pmatrix}=
> 	\begin{pmatrix}
> 	\frac{1}{6}\\\frac{2}{\sqrt{6}}\\-\frac{1}{\sqrt{6}}
> 	\end{pmatrix},&&\mathbf{u}_{2}=\frac{1}{5}
> 	\begin{pmatrix}
> 	0\\1\\2
> 	\end{pmatrix}=
> 	\begin{pmatrix}
> 	0\\\frac{1}{\sqrt{5}}\\\frac{2}{\sqrt{5}}
> 	\end{pmatrix},&&\mathbf{u}_{3}=\frac{1}{\sqrt{30}}
> 	\begin{pmatrix}
> 	5\\-2\\1
> 	\end{pmatrix}=
> 	\begin{pmatrix}
> 	\frac{5}{\sqrt{30}}\\-\frac{2}{\sqrt{30}}\\\frac{1}{\sqrt{30}}
> 	\end{pmatrix}
> 	\end{align}
>
> 	$$
> - result:
> 	- satisfies $\mathbf{u}_{1}\cdot\mathbf{u}_{2}=\mathbf{u}_{1}\cdot\mathbf{u}_{3}=\mathbf{u}_{2}\cdot\mathbf{u}_{3}=0$ and $\lvert \lvert \mathbf{u}_{1} \rvert \rvert=\lvert \lvert \mathbf{u}_{2} \rvert \rvert=\lvert \lvert \mathbf{u}_{3} \rvert \rvert=1$
> 	- linearly independent

link: [[Dot Product]] [[linear independence]] 