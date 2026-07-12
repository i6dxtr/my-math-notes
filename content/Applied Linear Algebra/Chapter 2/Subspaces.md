 #ch2

> [!definition]
> A **subspace** of a vector space $V$ is a subset $W\subset V$ that is a [[Vector Space|vector space]]:
> 1. Closed under vector addition,
> 2. Closed under scalar multiplication, and
> 3. Contains the same zero element.

- from which, we define the subspaces of the reals
	- the space from which we will most often work with

> [!definition] Subspaces of $\mathbb{R}^n$:
>    $\emptyset \neq V \subset \mathbb{R}^n$ is a subspace if:
> 1. $x,y\in V$, then $x+y\in V$
> 2. $\alpha \in \mathbb{R}, x \in V$, then $\alpha x\in V$

> [!example]
> $$V=\left\{\begin{pmatrix}x_{1} \\x_{2}\end{pmatrix}:x_{1}, x_{2}\geq 0\right\} $$ ... In particular, $\langle 1,1 \rangle\in V$, but $-\langle 1,1 \rangle\not\in V$.

> [!corollary]
> (p.82) A nonempty set $W\subset V$ of a [[Vector Space|vector space]] is a subspace *if and only if*:
> 1. $\forall \mathbf{v}, \mathbf{w}\in W,\ \mathbf{v}+\mathbf{w}\in W$
> 2. $\forall \mathbf{v}\in W\ \forall c\in\mathbb{R},\ \ c\mathbf{v}=W$

> [!example]
> - The trivial subspace $W=\left\{ \mathbf{0} \right\}$
> - The entire space $W=\mathbb{R}^{3}$
> - The set of all vectors of the form $(x,y,0)^{T}$ i.e. the $xy-$plane
> - The set of solutions $(x,y,z)^{T}$ to the homogeneous linear equation $3x+2y-z=0$

#### Two special types of subspaces:
- [[column space]]
- [[row space]]

### Lecture

We care (almost) only about two special types of subspaces:
- $\overline v_{1}, \overline{v}_{2},\overline{v_{3}},..., \overline{v_{n}}\in\mathbb{R} ^{K}$
- then $\text{span}\langle \overline{v}_{1}, \overline{v}_{2},...,\overline{v}_{n} \rangle=\langle a_{1}\overline{v}_{1}+...+\alpha \overline{v}_{n}: \alpha_{1}, ..., \alpha _{n} \in \mathbb{R} \rangle$
- key example: $A$ is a $k \times n$ matrix
$\text{col}(A)$ = span of the the columns of $A$ ... $\subset \mathbb{R}^{K}$
$\text{row}(A)$ = span of rows of $A$ = $\text{col}(A^{T})$

$$
A=\begin{pmatrix}
4 & 2 & \pi & 4 \\
7 & 9 & 6 & 8 \\
8 & 1 & 10 & -1
\end{pmatrix}
$$
$$
\text{col}(A)=\text{span}\left\{ 
\begin{pmatrix}
 4 \\
7 \\
8 
\end{pmatrix}
\begin{pmatrix}
 2 \\
9 \\
1 
\end{pmatrix} ...

 \right\}\subset \mathbb{R}^{3}
$$
#### Null space of a matrix:
- The set of all $\overline{x}\in\mathbb{R}^{n}$ such that $A\overline{x}=\overline{0}$
	- $\overline{0}=\langle 0, ..., 0 \rangle \in \mathbb{R}^{K}$
	- $A$ is $k  \times n$, $\overline{x}$ is $n \times 1$
- Also denotes *linear independence*

link: [[Vector Space]]