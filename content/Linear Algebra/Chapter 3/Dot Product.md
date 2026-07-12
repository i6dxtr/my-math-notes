#ch3
- the **dot product** is an example of a vector *inner product*
- computed between column vectors $\mathbf{v}=(v_{1}, v_{2}, ..., v_{n})^{T}$, $\mathbf{w}=(w_{1}, w_{2}, ..., w_{n})^{T}$, both lying in $\mathbb{R}^{n}$: $$\mathbf{v}\cdot \mathbf{w}=v_{1}w_{1}+v_{2}w_{2}+..+v_{n}w_{n}=\sum_{i=1}^{n}v_{i}w_{i}$$
- observe: this is equal to the matrix product:
	$$
	\mathbf{v}\cdot\mathbf{w}=\mathbf{v}^{T}\mathbf{w}=(v_{1}\ \ v_{2}\ \ ...\ \ v_{n})
	\begin{pmatrix}w_{1} \\ w_{2} \\ ... \\ w_{n} \end{pmatrix}
	$$
	...between row vector $\mathbf{v}^{T}$ and column vector $\mathbf{w}$.
- since the dot product of a vector by itself is essentially the sum of the square of it's entries, it can be represented geometrically (pythagoras)
	- thus, we can define the [[norm]] of a vector accordingly

> [!definition]
> An **inner product** on the real vector space $V$ is a pairing that takes two vectors $\mathbf{v}, \mathbf{w}\in V$ and produces a real number $\left\langle \mathbf{v}, \mathbf{w} \right\rangle\in \mathbb{R}$. The inner product is required to satisfy the following three axioms for all $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$ and scalars $c,d\in \mathbb{R}$:
> 1. Bilinearity: $\left\langle c\mathbf{u}+d\mathbf{v},\ \mathbf{w} \right\rangle=c\left\langle \mathbf{u}, \mathbf{w} \right\rangle+d\left\langle \mathbf{v},\mathbf{w} \right\rangle$ AND $\left\langle \mathbf{u}, c\mathbf{v}+d\mathbf{w} \right\rangle=c\left\langle \mathbf{u}, \mathbf{v} \right\rangle+d\left\langle \mathbf{u}, \mathbf{w} \right\rangle$
> 2. Symmetry: $\left\langle \mathbf{v}, \mathbf{w} \right\rangle=\left\langle \mathbf{w}, \mathbf{v} \right\rangle$
> 3. Positivity: $\left\langle \mathbf{v}, \mathbf{v} \right\rangle>0$ whenever $\mathbf{v}\neq \mathbf{0}$, while $\left\langle \mathbf{0}, \mathbf{0} \right\rangle=0$.

- two basic [[geometric rep. of inner products]] valid for *any* inner product space:

> [!remark]
> $$Ax\cdot y=(Ax)^{T}y=x^{T}A^{T}y=x\cdot A^{T}y$$

## Lecture Notes
$x,y \in \mathbb{R}^{n}$, think of them as $n \times1$ matrices
- $x=\begin{pmatrix} x_{0}\\x_{1}\\...\\x_{n-1} \end{pmatrix}$, y=$\begin{pmatrix} y_{0}\\y_{1}\\...\\y_{n-1} \end{pmatrix}$
- $x\cdot y= x_{0}y_{0}+x_{1}y_{1}+...+x_{n-1}y_{n-1}$
- ==Remark== $x\cdot y=y\cdot x$
	- $x\cdot x= x_{0}^{2}+x_{1}^{2}+...+x_{n-1}^{2}=\lvert \lvert x \rvert \rvert^{2}$
	- $x\cdot x=0\leftrightarrow x=\overline{0}$

##### Geometry
$\mathbf{x}, \mathbf{y}\in \mathbb{R}^{n}$. the law of cosines 
- or really a trig identity says:
- $\cos \vartheta=\frac{x\cdot y}{\lvert \lvert x \rvert \rvert\ \lvert \lvert y \rvert \rvert}$

How might we use this?
Q: Comparison of homes in Oxford. Sample 4 data points:
$$
\begin{align}
\begin{pmatrix}
\text{Price}  \\
\text{Sq. Ft.} \\
\text{Num. of bedrooms} \\
\text{Prep Tax}

\end{pmatrix}\\
\text{ ... where Price }&\geq 100,000,\\
\text{sq.ft}&>600,\\
\text{num. of bedrooms}&\geq ?, \\
\text{Prep Tax}&\geq \text{high}
\end{align}
$$
- to locate similar homes, once can test the 'angle' between them.

The (not so) secret to a happy life:
##### Setup
$A$ is $m \times n$
$B$ is $n \times K$
$$
\begin{align}
(AB)^{T}&=B^{T}A^{T}  \\
C.T&=C && &\text{ if }c\text{ is a }1 \times  1\text{ matrix} \\\\
&\text{... Now, let }x\in \mathbb{R}^{n}, y\in \mathbb{R}^{m}. && &\text{ where both }1 \times 1\\ \\
A\mathbf{x}\cdot\mathbf{y}&=y^{T}Ax \\
&=(y^{T}Ax)^{T} \\
&=x^{T}A^{T}y \\
&=A^{T}y\cdot x \\
&=x\cdot A^{T}y
\end{align}
$$

> [!remark]
> $$
> Ax\cdot y=x\cdot A^{T}y
> $$

