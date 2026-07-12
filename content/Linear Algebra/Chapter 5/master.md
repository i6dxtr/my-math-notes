#ch5
## Equilibrium Mechanics
- systems in equilibrium minimize potential energy
- simplest examples are in quadratic functions
	- *e.g.* given $f\left( x,y \right)=4x^{2}-2xy+4y^{2}+x-2y+1$, 
		- the equation derived from finding the lowest potential energy of a ball rolling downhill
		- want to find local minimum, so the point $x=x^{*}, y=y^{*}$, if it exists, s.t. $f\left( x^{*}, y^{*} \right)=\text{min}$ 
## Solution of Equations
- *e.g.* solving $f_{1}(\mathbf{x})=0$, $f_{2}(\mathbf{x})=0$, ..., $f_{m}(\mathbf{x})=0$ where $\mathbf{x}=\left( x_{1}, ..., x_{n} \right)\in\mathbb{R}^{n}$. 
- we can convert to minimization problem:
	- define $p(\mathbf{x})=\left[ f_{1}(\mathbf{x}) \right]^{2}+\cdots+\left[ f_{m}(\mathbf{x}) \right]^{2}=\lvert f(\mathbf{x}) \rvert^{2}$ where $\mathbf{f(x)}=\left( f_{1}(\mathbf{x}), ..., f_{m}(\mathbf{x}) \right)^{T}$ and $\lvert \cdot \rvert$ denotes Euclidean norm on $\mathbb{R}^{m}$ 
	- moreover, $p(\mathbf{x}^{*})=0$ iff each summand is 0; hence $\mathbf{x}=\mathbf{x}^{*}$ is a soln to the above
- most important case: $A\mathbf{x}=\mathbf{b}$
	- consisting of $m$ equations and $n$ unknowns
	- solutions obtained by minimizing the function: $$p(\mathbf{x})=\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert \rvert^{2}$$
	- $p(\mathbf{x})$ clearly has min = 0 achieved iff $\mathbf{x}$ a soln to the linear system
	- we now develop another theorem based off Gaussian elimination

> [!remark]
> Suppose that the linear system above does not have a solution, i.e. $\mathbf{b}$ does not lie in the image of matrix $A$. We may then choose to find an approximate solution by taking $\mathbf{x}^{*}$ that comes as close to solving the system as possible. *How?*
> 1. Observe the magnitude of the *error* as measured by the *residual vector* $\mathbf{r}=\mathbf{b}-A\mathbf{x}$ 
> 	1. i.e. the difference btwn RHS and LHS of system
> 	2. smaller the norm ( $\lvert \lvert \mathbf{r} \rvert \rvert=\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert \rvert$ ) the better the solution
> 2. Take the *least squares solution*, the vector $\mathbf{x}^{*}$ that minimizes the squared residual norm function $p(\mathbf{x})=\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert \rvert^{2}$
> 	1. since $\lvert \lvert \mathbf{r} \rvert \rvert^{2}=r_{1}^{2}+\cdots+ r_{n}^{2}$ is the sum of the squares of the individual error components
> 	2. if $A\mathbf{x}=\mathbf{b}$ has a solution, $\mathbf{x}^{*}$ still is the least squares solution since $\lvert \lvert A\mathbf{x}^{*}-\mathbf{b} \rvert \rvert=0$ achieves absolute minimum
> 	3. note that the norm must arise from an inner product, so weighted norms can be introduced to (de)emphasize various errors

## The Closest Point
*Problem.* Given $\mathbf{b}\in \mathbb{R}^{m}$ and subset $V\subset \mathbb{R}^{m}$, find point $\mathbf{v}^{*}\in V$ closest to $\mathbf{b}$.
- i.e. minimize Euclidean distance $d(\mathbf{v},\mathbf{b})=\lvert \lvert \mathbf{v}-\mathbf{b} \rvert \rvert$ for all $\mathbf{v}\in V$
- simplest: $V\subset \mathbb{R}^{m}$
	- let $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$ be a basis for $V$
	- general element $\mathbf{v}\in V$ is a linear combination of the basis vectors, thus rewrite in form: $$\mathbf{v}=x_{1}\mathbf{v}_{1}+\cdots+x_{n}\mathbf{v}_{n}=A\mathbf{x}$$ ... where $A=\begin{pmatrix} \mathbf{v}_{1}&\mathbf{v}_{2}&\cdots&\mathbf{v}_{n} \end{pmatrix}$ is $m \times n$ matrix form by col (basis) vectors & $\mathbf{x}=\left( x_{1}, x_{2}, ..., x_{n} \right)^{T}$ are coords of $\mathbf{v}$ relative to chosen basis
	- identify $\mathbf{v}$ with $\text{img}(A)$ 
		- the subspace spanned by its columns
	- closest point $\in V$ to $\mathbf{b}$ found by minimizing:
		- $\lvert \lvert \mathbf{v}-\mathbf{b} \rvert \rvert^{2}=\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert \rvert^{2}$ over all possible $\mathbf{x}\in\mathbb{R}^{n}$
		- exact same as least squares function ( !! )
- ==Core Idea==: if $\mathbf{x}^{*}$ the LSS to system $A\mathbf{x}=\mathbf{b}$ then $\mathbf{v}^{*}=A\mathbf{x}^{*}$ is the closest point to $\mathbf{b}$ belonging to $V=\text{img }A$.
	- $\mathbf{v}\in V$ is also the orthogonal projection of $\mathbf{b}$ onto the subspace
			![[Pasted image 20241021233313.png]]
### Minimizing quadratic functions of several variables
The minimization of a real quadratic polynomial is derived from the least-squares equation and is as follows: $$p(\mathbf{x})=p(x_{1}, ..., x_{n})=\sum_{i,j=1}^{n}k_{ij}x_{i}x_{j}-2\sum_{i=1}^{n}f_{i}x_{i}+c$$ ... depending on $n$ variables $\mathbf{x}=\left( x_{1}, x_{2}, ..., x_{n} \right)^{T}\in \mathbb{R}^{n}$
- assume coefficients are symmetric: $k_{ij}=k_{ji}$
- $p(\mathbf{x})$ is more general
- we can rewrite above quadratic function in more compact matrix: $$p(\mathbf{x})=\mathbf{x}^{T}K\mathbf{x}-2\mathbf{x}^{T}\mathbf{f}+c,\ \ \mathbf{x}\in \mathbb{R}^{n}$$... where $K=(k_{ij})$, a symmetric $n \times n$ matrix, $\mathbf{f}\in \mathbb{R}^{n}$ is a constant vector, and $c$ is a constant scalar 
	- see example 5.1 
- from this, we can yield the following theorem: 

> [!theorem]
> If $K$ is a positive definite (and hence symmetric) matrix, then the quadratic function has a unique minimizer, which is the solution to the linear system
> $$
> \begin{align}
> K\mathbf{x}=\mathbf{f},&&\text{ namely, }&&\mathbf{x}^{*}=K^{-1}\mathbf{f}
> \end{align}
> $$
> ... the minimum value of $p(\mathbf{x})$ is equal to any of the following expressions: $$p(\mathbf{x}^{*})=p(K^{-1}\mathbf{f})=c-\mathbf{f} ^{T}K^{-1}\mathbf{f}=c-\mathbf{f}^{T}\mathbf{x}^{*}=c-(\mathbf{x}^{*})^{T}K\mathbf{x}^{*}$$

> [!proof]
> Positive definiteness implies that $K$ is nonsingular, such that $K\mathbf{x}=\mathbf{f}$ has a unique solution $\mathbf{x}^{*}=K^{-1}\mathbf{f}$. So $\forall\mathbf{x}\in \mathbb{R}^{n}$, since $\mathbf{f}=K\mathbf{x}^{*}$, we derive the following:
> $$
> \begin{align}
> p(\mathbf{x})&=\mathbf{x}^{T}K\mathbf{x}-2\mathbf{x}^{T}\mathbf{f}+c\\ &=\mathbf{x}^{T}K\mathbf{x}-2\mathbf{x}^{T}K\mathbf{x}^{*}+c\\&=(\mathbf{x}-\mathbf{x}^{*})^{T}K(\mathbf{x}-\mathbf{x}^{*})+\left[ c-(\mathbf{x}^{*})^{T}K\mathbf{x}^{*} \right].
> \end{align}
> $$

## 5.3 Closest Point
 - todo: start from beginning

> [!theorem]
> Let $\mathbf{w}_{1},...,\mathbf{w}_{n}$ form a basis for the subspace $W\subset\mathbb{R}^{m}$. Given $\mathbf{b}\in \mathbb{R}^{m}$, the closest point $\mathbf{w}^{*}=x_{1}^{*}\mathbf{w}_{1}+\cdots+x_{n}^{*}\mathbf{w}_{n}\in W$ is unique and prescribed by the solution $\mathbf{x}^{*}=K^{-1}\mathbf{f}$ to the linear system $$K\mathbf{x}=\mathbf{f}$$... where the entries of $K$ and $\mathbf{f}$ are given by $$k_{ij}=\left\langle \mathbf{w}_{i}, \mathbf{w}_{j} \right\rangle$$... and $$\left\langle \mathbf{w}, \mathbf{b} \right\rangle=\sum_{i=1}^{n}x_{i}f_{i}=\mathbf{x}^{T}\mathbf{f}$$... and, for  $\mathbf{f}\in \mathbb{R}^{n}$, $$f_{i}=\left\langle \mathbf{w}_{i}, \mathbf{b} \right\rangle.$$
> The minimum distance between the point and subspace is $$d^{*}=\lvert\lvert \mathbf{w}^{*}-b \rvert\rvert =\sqrt{\lvert\lvert \mathbf{b} \rvert\rvert ^{2}-\mathbf{f}^{T}\mathbf{x}^{*}}$$

> [!theorem]
> Let $W\subset V$ be a finite-dimensional subspace of an inner product space. Given a point $\mathbf{b}\in V$, the closest point $\mathbf{w}^{*}\in W$ coincides with the orthogonal projection of $\mathbf{b}$ onto $W$.

## 5.4 Least Squares

> [!definition]
> A **least squares solution** to a linear system of equations $$A\mathbf{x}=\mathbf{b}$$... is a vector $\mathbf{x}^{*}\in \mathbb{R}^{n}$ that minimizes the squared Euclidean norm $\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert \rvert^{2}$.

- is new *only if* the system does not have a solution
	- $\mathbf{b}$ does not lie in the image of $A$.
- should be unique iff $\text{ker } A=\left\{ \mathbf{0} \right\}$
	- cols linearly independent forming basis for $\text{img }W$
	- $\text{rank }A=n$
- if $\mathbf{z}\in\text{ker }A$, equation $A\tilde{\mathbf{x}}=\mathbf{x}+\mathbf{z}$ satisfies: $$\lvert \lvert A\tilde{\mathbf{x}}-\mathbf{b} \rvert  \rvert^{2}=\lvert \lvert A(\mathbf{x}+\mathbf{z})-\mathbf{b} \rvert  \rvert ^{2}=\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert  \rvert ^{2} $$... also a minimum.
	- uniqueness requires $\mathbf{z}=\mathbf{0}$
- connection w/ closest point:
	- identify subspace $W=\text{img }A\subset\mathbb{R}^{m}$ as img/col space of $A$
	- linearly independent cols $\rightarrow$ basis formed
	- $\forall\mathbf{w}\in\text{img }A$ can be rewritten $\mathbf{w}=A\mathbf{x}$
		- minimizing $\lvert \lvert A\mathbf{x}-\mathbf{b} \rvert \rvert^{2}$ $\equiv$ minimizing distance $\lvert \lvert \mathbf{w}-\mathbf{b} \rvert \rvert$ btwn points & subspace
	- solution $\mathbf{x}^{*}$ to quadratic minimization produces $\mathbf{w}^{*}=A\mathbf{x}^{*}$ in $W=\text{img }A$

> [!theorem]
> Assume that $\text{ker }A=\left\{ \mathbf{0} \right\}$. Then the least squares solution to the linear system $A\mathbf{x}=\mathbf{b}$ under the Euclidean norms is the unique solution $\mathbf{x}^{*}$ to the *normal equations*
> $$
> \begin{align}
> (A^{T}A)\mathbf{x}=A^{T}\mathbf{b},&&\text{ where }&&\mathbf{x}^{*}=(A^{T}A)^{-1}A^{T}\mathbf{b}
> \end{align}
> $$
> ... where the *least squares error* is: $$\lvert \lvert A\mathbf{x}^{*}-\mathbf{b} \rvert  \rvert ^{2}=\lvert \lvert \mathbf{b} \rvert  \rvert ^{2}-\mathbf{f}^{T}\mathbf{x}^{*}=\lvert \lvert \mathbf{b} \rvert  \rvert ^{2}-\mathbf{b}^{T}A(A^{T}A)^{-1} A^{T}\mathbf{b}$$

- obtained by multiplying $A\mathbf{x}=\mathbf{b}$ on both sides by $A^{T}$
- allows for a new formula to soln to $A\mathbf{x}=\mathbf{b}$ when $A$ is non-invertible and $\mathbf{b}\in\text{img }A$

> [!theorem]
> Suppose $A$ is an $m \times m$ matrix such that $\text{ker }A=\left\{ \mathbf{0} \right\}$, and suppose $C>0$ is any positive definite $m \times m$ matrix specifying the weighted norm $\lvert\lvert \mathbf{v} \rvert\rvert^{2}=\mathbf{v}^{T}C\mathbf{v}$. Then the least squares solution to the linear system $A\mathbf{x}=\mathbf{b}$ that minimizes the weighted squared error $\lvert\lvert A\mathbf{x}-\mathbf{b} \rvert\rvert^{2}$ is the unique solution $\mathbf{x}^{*}$ to the *weighted normal equations*:
> $$
> \begin{align}
> A^{T}CA\mathbf{x}^{*}=A^{T}C\mathbf{b}&&\text{such that}&&\mathbf{x}^{*}=(A^{T}CA)^{-1}A^{T}C\mathbf{b}
> \end{align}
> $$
> ... and the *weighted least squares error* is:
> $$
> \begin{align}
> \lvert\lvert A\mathbf{x}^{*}-\mathbf{b} \rvert\rvert ^{2}&=\lvert\lvert \mathbf{b} \rvert\rvert ^{2}-\mathbf{f}^{T}\mathbf{x}^{*}\\ &=\lvert\lvert \mathbf{b} \rvert\rvert ^{2}-\mathbf{b}^{T}CA(A^{T}A)^{-1}A^{T}C\mathbf{b}
> \end{align}
> $$

