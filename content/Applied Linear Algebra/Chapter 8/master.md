### 8.1 Linear Dynamical Systems

....

### 8.2 Eigenvalues and Eigenvectors

> [!definition]
> Let $A$ be an $n \times n$ matrix. A scalar $\lambda$ is called an **eigenvalue** of $A$ if there is a nonzero vector $\mathbf{v}\neq 0$, called an **eigenvector**, such that: $$A\mathbf{v}=\lambda\mathbf{v}$$
> - Geometrically, $A$ stretches $\mathbf{v}$ by amount specified by $\lambda$

Consider the definition above to represent a system of linear equations for the entries of $\mathbf{v}$ that, combined with $\lambda$, presents a somewhat *nonlinear* system. Therefore, we take a different approach to solve.
##### Solving for eigenvalues
We can rewrite the definition as: $$( A-\lambda \mathbb{1}_{n} )\mathbf{v}=\mathbf{0}$$... where $\mathbb{1}_{n}$ is the $n \times n$ identity equal to the size of $A$
- Observe that b/c $\mathbf{v}\neq \mathbf{0}$, the coefficient matrix $A-\lambda\mathbb{1}_{n}$ must be non-invertible

> [!theorem]
> A scalar $\lambda$ is an eigenvalue of the $n \times n$ matrix $A$ *if and only if* the matrix $A-\lambda\mathbb{1}_{n}$ is singular, i.e., of $\text{rank}<n$. The corresponding eigenvectors are the nonzero solutions to the eigenvalue equation $( A-\lambda\mathbb{1}_{n} )\mathbf{v}=\mathbf{0}$.

> [!corollary]
> A scalar $\lambda$ is an eigenvalue of the matrix $A$ *if and only if* $\lambda$ is a solution to the *characteristic equation*: $$\text{det}( A-\lambda\mathbb{1}_{n} )=0.$$

> [!example]
> Consider the $3 \times 3$ matrix: $$A=\begin{pmatrix} 0&-1&-1\\1&2&1\\1&1&2 \end{pmatrix}$$... Applying formula for determinant gives the following:
> $$
> \begin{align} 0&=\text{det}( A-\lambda\mathbb{1}_{3} )=\text{det}\begin{pmatrix} -\lambda&-1&-1 \\ 1&2-\lambda&1 \\ 1&1&2-\lambda \end{pmatrix} \\ &=-\lambda^{3}+4\lambda^{2}-5\lambda+2\\&=-( \lambda-1 )^{2}( \lambda-2 ) \end{align}
> $$
> So there are 2 eigenvalues (although typically 3 for $3 \times 3$ matrices, but $1$ is a double eigenvalue).
> We then derive the eigenvector for $\lambda=1$: $$( A-(1)I )\mathbf{v}=\begin{pmatrix} -1&-1&-1\\1&1&1\\1&1&1 \end{pmatrix}\begin{pmatrix} x\\y\\z \end{pmatrix}=\begin{pmatrix} 0\\0\\0 \end{pmatrix}$$... for which the general solution to is as follows: $$\mathbf{v}=\begin{pmatrix} -a-b\\a\\b \end{pmatrix}=a\begin{pmatrix} -1\\1\\0 \end{pmatrix}+b\begin{pmatrix} -1\\0\\1 \end{pmatrix}$$... being dependent upon free variables $y=a$ and $z=b$. 
> Every nonzero solution forms valid eigenvectors for $\lambda_{1}=1$, therefore the general eigenvector is any nonzero linear combination of the two basis eigenvectors $\mathbf{v}_{1}=( -1,1,0 )^{T}$ and $\hat{\mathbf{v}}_{1}=( -1,0,1 )^{T}$.
> Conversely, the eigenvector given $\lambda_{2}=2$ can be computed by: $$( A-2I )\mathbf{v}=\begin{pmatrix} -2&-1&-1\\1&0&1\\1&1&0 \end{pmatrix}\begin{pmatrix} x\\y\\z \end{pmatrix}=\begin{pmatrix} 0\\0\\0 \end{pmatrix}$$... whereas the general solution is given by: $$\mathbf{v}=\begin{pmatrix} -a\\a\\a \end{pmatrix}=a\begin{pmatrix} -1\\1\\1 \end{pmatrix}$$... consisting of all scalar multiples of the eigenvector $\mathbf{v}_{2}=( -1,1,1 )^{T}$.
> So we've derived the following from this matrix:
> 1. $\lambda_{1}=1$
> 2. $\lambda_{2}=2$
> 3. $\mathbf{v}_{1}=\begin{pmatrix} -1\\1\\0 \end{pmatrix}$
> 4. $\mathbf{v}_{2}=\begin{pmatrix} -1\\1\\1 \end{pmatrix}$
> 5. $\hat{\mathbf{v}}_{1}=\begin{pmatrix} -1\\0\\1 \end{pmatrix}$
> ... meaning, every eigenvector for $\lambda_{2}=2$ is a nonzero scalar multiple of $\mathbf{v}_{2}$, while every eigenvector $\lambda_{1}=1$ is a nontrivial linear combination $a\mathbf{v}_{1}+b\hat{\mathbf{v}}_{1}$ fo the two linearly independent eigenvectors $\mathbf{v}_{1}, \hat{\mathbf{v}}_{1}$.

- $\lambda\in \mathbb{R}$ eigenvalue $\Longleftrightarrow$ $V_{\lambda}\ne\left\{ \mathbf{0} \right\}$ nontrivial subspace

#### Basic Properties of Eigenvalues
assorted theorems:

> [!theorem]
> An $n \times n$ matrix possesses at least one and at most $n$ distinct complex eigenvalues.

> [!remark]
> If $\lambda$ is a complex eigenvalue of multiplicity $k$ for $A$, then its complex conjugate $\overline{\lambda}$ also has multiplicity $k$, since the complex conjugate roots of a real polynomial necessarily appear with identical multiplicities.

> [!theorem]
> A square matrix $A$ and its transpose $A^{T}$ have the same characteristic equation, and hence the same eigenvalues with the same multiplicities.

> [!remark]
> This doesn't mean their eigenvectors are necessarily the same; in fact, they are generally different
> - An eigenvector $\mathbf{v}$ satisfying $A^{T}\mathbf{v}=\lambda\mathbf{v}$ is called a *left eigenvector* of $A$

> [!theorem]
> The sum of the eigenvalues of a square matrix $A$ equals its trace: $$\lambda_{1}+\lambda_{2}+\cdots+\lambda_{n}=\text{tr}(A )=a_{11}+a_{22}+\cdots+a_{nn}$$... and the product of the eigenvalues equals its determinant: $$\lambda_{1}\lambda_{2}\cdots\lambda_{n}=\text{det }A.$$

> [!definition]
> A square matrix $A$ is called *strictly diagonally dominant* if: $$\lvert a_{ii} \rvert >\sum_{j\ne i}^{}\lvert a_{ij} \rvert ,\ \ \ \text{ for all }\ \ \ i=1,...,n.$$

- requires each diagonal entry to be larger in absolute value than the sum of *all* other entries in its row.

> [!theorem]
> A strictly diagonally dominant matrix is *nonsingular*.

### 8.3 Eigenvector Bases

> [!corollary] Lemma.
> If $\lambda_{1}, ..., \lambda_{k}$ are *distinct* eigenvalues of a matrix $A$, so $\lambda_{i}\ne \lambda_{j}$ when $i\ne j$, then the corresponding eigenvectors $\mathbf{v}_{1}, ..., \mathbf{v}_{k}$ are linearly independent.

> [!theorem]
> If the $n \times n$ real matrix $A$ has $n$ distinct real eigenvalues $\lambda_{1},...,\lambda_{n}$, then the corresponding real eigenvectors $\mathbf{v}_{1},...,\mathbf{v}_{n}$ form a basis for $\mathbb{R}^{n}$. If $A$ (which may now be either a real or a complex matrix) has $n$ distinct complex eigenvalues, then the corresponding eigenvectros $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ form a basis of $\mathbb{C}^{n}$

> [!definition]
> An eigenvalue $\lambda$ of a matrix $A$ is called **complete** if the corresponding eigenspace $V_{\lambda}=\text{ker}( A-\lambda I )$ has the same dimension as its multiplicity. The matrix $A$ is said to be **complete** if all its eigenvalues are complete.

> [!remark]
> - The multiplicity of an eigenvalue $\lambda_{i}$ is the same as its *algebraic multiplicity*.
> - The dimension of the eigenspace $V_{\lambda}$ is its *geometric multiplicity*

- a simple eigenvalue is automatically complete, since its eigenspace is the one dimensional subspace or eigenline spanned by the corresponding eigenvector
	- so only multiple eigenvalues can cause a matrix to be incomplete
- in other words, a matrix is complete if and only if its eigenvectors span $\mathbb{C}^{n}$

> [!theorem]
> An $n  \times n$ real or complex matrix $A$ is complete if and only if its eigenvectors span $\mathbb{C}^{n}$. In particular, an $n \times n$ matrix that has $n$ distinct eigenvalues is complete.

#### Diagonalization

- let $L:\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ be a linear transformation on $n$D Euclidean space
- $L\left[ \mathbf{x} \right]=A\mathbf{x}$ can be given by multiplication by $n \times n$ matrix $A$
	- matrix representation depends on chosen basis for $\mathbb{R}^{n}$
- linear transformations having complicated matrix representation in terms of $\mathbf{e}_{1}, ..., \mathbf{e}_{n}$ can be simplified by choosing suitably adapted basis $\mathbf{v}_{1},...,\mathbf{v}_{n}$.
###### Example
- Take $L\begin{pmatrix} x\\y \end{pmatrix}=\begin{pmatrix} x-y\\2x+4y \end{pmatrix}$
	- represented by $A=\begin{pmatrix} 1&-1\\2&4 \end{pmatrix}$ as expressed by std. basis of $\mathbb{R}^{2}$
	- alternative basis: $\mathbf{v}_{1}=\begin{pmatrix} 1\\-1 \end{pmatrix}$, $\mathbf{v}_{2}=\begin{pmatrix} 1\\-2 \end{pmatrix}$ is then represented by matrix $\begin{pmatrix} 2&0\\0&3 \end{pmatrix}$
		- implication: has a simple stretching action on new basis vectors $A\mathbf{v}_{1}=2\mathbf{v}_{1}$, $A\mathbf{v}_{2}=3\mathbf{v}_{2}$
	- ==idea==: *the new basis consists of the two eigenvectors of the matrix $A$*.
		- representing a lin. transformation in terms of eigenvector basis has the effect of changing its matrix representation into simple diagonal form
		- this is called *diagonalization*
- if $\mathbf{v}_{1},...,\mathbf{v}_{n}$ form a basis of $\mathbb{R}^{n}$, then the corresponding matrix representation of transformation $L\left[ \mathbf{v} \right]=A\mathbf{v}$ is given by similar matrix $B=S^{-1}AS$
	- where $S=( \mathbf{v}_{1}, \mathbf{v}_{2}, ..., \mathbf{v}_{n} )$ is the matrix whose cols are basis vectors

> [!definition]
> A square matrix $A$ is called **diagonalizable** if here exists a nonsingular matrix $S$ and a diagonal matrix $\Lambda=\text{diag}( \lambda_{1},...,\lambda_{n} )$ such that: $$S^{-1}AS=\Lambda \ \ \ \text{... equivalently, ...}\ \ \ A=S\Lambda S^{-1}.$$

- stretches in direction of basis vectors
	- so an elementary combination of complex stretching transformations
- can be rewritten equivalently: $$AS=S\Lambda$$... where one can observe the $k^{th}$ column of the $n \times n$ matrix equation is given by: $$A\mathbf{v}_{k}=\lambda_{k}\mathbf{v}_{k}$$... where $\mathbf{v}_{k}$ denotes $k^{th}$ column of $S$
	- so $S$ cols are *necessarily* the eigenvectors, with corresponding entries in $\Lambda$ are eigenvals
	- as a result, diagonalizable $A$ must have $n$ linearly independent eigenvectors

> [!theorem]
> A matrix is *complex diagonalizable* if and only if it is complete. A real matrix is real diagonalizable if and only if it is complete and has all real eigenvalues

### 8.4 Invariant Subspaces

> [!definition]
> Let $L:V\rightarrow V$ be a linear transformation on a vector space $V$. A subspace $W\subset V$ is said to be **invariant** if $L\left[ \mathbf{w} \right]\in W$ whenever $\mathbf{w}\in W$

- trivial cases: the entire space $W=V$ and the zero subspace $W=\left\{ \mathbf{0} \right\}$

> [!example]
> 1. let $V=\mathbb{R}^{2}$
> 2. we wanna find all invariant subspaces of scaling transformation given by: $$L( x,y )=( 2x,3y )^{T}$$
> 	1. take $W$, a line spanned by $\mathbf{w}=( a,b )^{T}$
> 	2. suppose $\mathbf{w}\ne 0$ 
> 	3. then $L\left[ \mathbf{w} \right]=( 2a, 3b )^{T}\in W$ *if and only if* $( 2a, 3b )^{T}=c\mathbf{w}=( ca,cb )^{T}$ 
> 		1. for some scalar $c$
> 		2. only possible if $a=0$ or $b=0$
> 	4. therefore, the only one-dimensional invariant subspaces are the $x$ and $y-$axes.
> other example
> 1. consider $L( x,y )=( x+3y, y )^{T}$
> 2. let $\mathbf{w}$ be a 1d spanning subspace s.t. $\mathbf{w}=( a,b )^{T}\ne \mathbf{0}$
> 	1. $\mathbf{w}$ invariant *iff* $( a+3b,b )^{T}=( ca, cb )^{T}$ for $c\in \mathbb{R}$
> 	2. possible only if $b=0$
> 3. thus only 1d invariant subspace of the transformation is the $x-$axis itself.

- note that linear transformation $L$ on either $\mathbb{R}^{n}$ or $\mathbb{C}^{n}$ given by matrix multiplication
	- $L\left[ \mathbf{x} \right]=A\mathbf{x}$ for some $n \times n$ matrix $A$

> [!corollary]
> A one-dimensional subspace is invariant under the linear transformation $L\left[ \mathbf{x} \right]$ if and only if it is an eigenline spanned by an eigenvector of $A$.

....... unfinished

### 8.5 Eigenvalues of Symmetric Matrices

> [!theorem]
> Let $A=A^{T}$ be a real symmetric $n \times n$ matrix. Then:
> 1. All the eigenvalues of $A$ are real
> 2. Eigenvectors corresponding to distinct eigenvalues are orthogonal
> 3. There is an orthonormal basis of $\mathbb{R}^{n}$ consisting of $n$ eigenvectors of $A$
> In particular, all real symmetric matrices are complete and real diagonalizable

> [!theorem]
> A symmetric matrix $K=K^{T}$ is **positive definite** *if and only if* all of its eigenvalues are strictly positive

> [!theorem]
> Let $A=A^{T}$ be an $n \times n$ symmetric matrix. Let $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ be an orthogonal eigenvector basis such that $\mathbf{v}_{1},..., \mathbf{v}_{r}$ correspond to nonzero eigenvalues, while $\mathbf{v}_{r+1},...,\mathbf{v}_{n}$ are null eigenvectors corresponding to the zero eigenvalue (if any). Then $r=\text{rank } A$; the non-null eigenvectors $\mathbf{v}_{1},..,\mathbf{v}_{r}$ form an orthogonal basis for $\text{ker }A=\text{coker }A$.

#### Spectral Theorem
- all real symmetric matrices can admit an eigenvector basis
	- hence are diagonalizable
- we can choose them to be [[orthogonal bases|orthogonal]]
	- matrices characterized by $Q^{-1}=Q^{T}$
- using orthonormalized eigenvector basis in diagonalization formula results in *spectral factorization* of a symmetric matrix

> [!theorem]
> Let $A$ be a real, symmetric matrix. Then there exists an orthogonal matrix $Q$ such that: $$A=Q\Lambda Q^{-1}=Q\Lambda Q^{T}$$... where $\Lambda$ is a real diagonal matrix. The eigenvalues of $A$ appear on the diagonal of $\Lambda$, while the columns of $Q$ are the corresponding orthonormal eigenvectors.

> [!remark]
> The spectral factorization gives an alternative means of diagonalizing the associated quadratic form (ie, of completing the square): $$q( \mathbf{x} )=\mathbf{x}^{T}A\mathbf{x}=\mathbf{x}^{T}Q\Lambda Q^{T}\mathbf{x}=\mathbf{y}^{T}y=\sum_{i=1}^{n}\lambda_{i}y_{i}^{2}$$... where the entries of $\mathbf{y}=Q^{T}\mathbf{x}=Q^{-1}\mathbf{x}$ are the coordinates of $\mathbf{x}$ with respect to the orthonormal eigenvector basis of $A$.

- $q( \mathbf{x} )>0$ for all $\mathbf{x}\ne 0$
- $A$ is positive definite *if and only if* each eigenvalue $\lambda_{i}$ is strictly positive