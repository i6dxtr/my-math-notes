 #ch2 
- the vectors used to form a [[span]] are essential in determining linear independence:

> [!definition]
> The vector elements $\mathbf{v}_{1}, ..., \mathbf{v}_{k}\in V$ are called **linearly dependent** if $\exists c_{1}, ..., c_{k} \neq 0$ s.t. $$c_{1}\mathbf{v}_{1}+...+c_{k}\mathbf{v}_{k}=\mathbf{0}$$ ... otherwise, the elements are **linearly independent**.

> [!theorem]
> Let $\mathbf{v}_{1}, ..., \mathbf{v}_{k} \in \mathbb{R}^{n}$ and let $A=( \mathbf{v}_{1}\ ...\ \mathbf{v}_{k} )$ be the corresponding $n \times k$ matrix whose columns are the given vectors.
> 1. The vectors $\mathbf{v}_{1}, ..., \mathbf{v}_{k}\in \mathbb{R}^{n}$ are linearly dependent *if and only if* there is a non-zero solution $\mathbf{c}\neq 0$ to the homogeneous system $A\mathbf{c}=\mathbf{0}$.
> 2. The vectors are linearly independent *if and only if* the solution to the homogeneous system $A\mathbf{c}=\mathbf{0}$ is the trivial solution.
> 3. A vector $\mathbf{b}$ lies in the span of $\mathbf{v}_{1}, ..., \mathbf{v}_{k}$ *if and only if* the linear system $A\mathbf{c}=\mathbf{b}$ is compatible, i.e has at least one solution.

- we ignore the trivial case where all $c_{i}=0$
- dependent when
	- vectors are parallel
	- multiples or equal to one another
	- all zero-row when placing matrix in [[Row Echelon Form]]
		- ... after constructing matrix of vectors w/ each being a *column vector* in the matrix'
- recall: any collection of $k>n$ vectors in $\mathbb{R}^{n}$ is *linearly dependent*
	- also, set of $k$ vectors in $\mathbb{R}^{n}$ linearly indep. $\longleftrightarrow$ $n \times k$ matrix $A$ has rank $k$ ($k\leq n$)
	- i.e. constructed matrix has no free variables

> [!example]
> $$
> > \begin{align}
> \mathbf{v}_{1}=\begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix}, && \mathbf{v}_{2}=\begin{pmatrix}0\\3\\1\end{pmatrix}, && \mathbf{v}_{3}=\begin{pmatrix} -1\\4\\3 \end{pmatrix}
> \end{align}
>
> $$
> - linearly dependent, since $\mathbf{v}_{1}-2\mathbf{v}_{2}+\mathbf{v}_{3}=\mathbf{0}$.
> - $\mathbf{v}_{1}, \mathbf{v}_{2}$ would be linearly independent
> 	- $c_{1}\mathbf{v}_{1}+c_{2}\mathbf{v}_{2}=\mathbf{0}$ doesn't hold since $c_{1}=0,\ 2c_{1}+3_{2}=0,\ -c_{1}+c_{2}=0$ has only the trivial solution

### Lecture

> [!definition]
> A set of vectors $\overline{v}_{1}, \overline{v}_{2}, ..., \overline{v}_{k}\in\mathbb{R}^{n}$ are **linearly independent** if $$\alpha_{1}\overline{v}_{1}+...+\alpha_{k}\overline{v}_{k}=\overline{0}$$
> ... which implies $\alpha_{1}=...=a_{k}=0$ (the trivial solution)

- helpful for computer calculations
- each $\overline{v}_{i}$ is not in the span of the other vectors

> [!example]
> $$
> > \begin{align}
>
> \overline{u}=\begin{pmatrix}
> 1 \\
> -1 \\
> 2
> \end{pmatrix},
> \overline{v}=
> \begin{pmatrix}
> 0 \\
> 1 \\
> 1
> \end{pmatrix},
> \overline{w}=
> \begin{pmatrix}
> 3 \\
> -5 \\
> 3
> \end{pmatrix}
> \end{align}
>
> $$
> - $\{ \overline{v},\overline{u}, \overline{w} \}$ is linearly independent.
> $3\overline{u}-2\overline{v}-\overline{w}$, so $\alpha_{1}=3,\alpha_{2}=-2, \alpha_{3}=-1$ is a nontrivial solution
> - observe that $\overline{w}\in\text{span}\{ \overline{u}, \overline{v} \}$
> 	- $\overline{w}=3\overline{u}-2\overline{v}$

- note that linear independence is a necessary requirement to find the [[basis]] vectors for a [[Subspaces|subspace]] $V$

