#ch2 

> [!definition]
> The *image* of an $m \times n$ [[matrix]] $A$ is the [[subspace]] $\text{img }A\subset \mathbb{R}^{m}$ spanned by its columns. The **kernel** of $A$ is the subspace $\text{ker }A\subset \mathbb{R}^{n}$ consisting of all vectors that are annihilated by $A$, so: 
>
> $$
> \text{ker }A=\left\{ \mathbf{z}\in  \mathbb{R}^{n}\ |\ A\mathbf{z}=\mathbf{0} \right\}
> $$

> [!remark]
> The image of a matrix is also known as the **column space**. Moreover, the kernel is the same as the **null space**.

- a vector $\mathbf{b}\in\mathbb{R}^{n}$ is in $\text{img }A$ if $\mathbf{b}=x_{1}\mathbf{v}_{1}+\ ...\ +x_{n}\mathbf{v}_{n}$
	- where $A=(\mathbf{v}_{1}\ \mathbf{v}_{2}\ ...\ \mathbf{v}_{n})$ (the columns)
- using matrix multiplication, RHS of $\mathbf{b}$ equals $A\mathbf{x}$ where $\mathbf{x}=(x_{1}, x_{2},...,x_{n})^{T}$, therefore $\mathbf{b}=A\mathbf{x}$, $\mathbf{x}\in \mathbb{R}^{n}$. Therefore:
	- $\text{img }A=\left\{ A\mathbf{x}\ |\ \mathbf{x}\in \mathbb{R}^{n} \right\}\subset\mathbb{R}^{m}$
	- vector $\mathbf{b}$ lies in the image of $A$ $\Longleftrightarrow$ $A\mathbf{x}=\mathbf{b}$ has a solution

> [!definition]
> Null space of a [[matrix]]:
> - The set of all $\overline{x}\in\mathbb{R}^{n}$ such that $A\overline{x}=\overline{0}$
> 	- $\overline{0}=\langle 0, ..., 0 \rangle \in \mathbb{R}^{K}$
> 	- $A$ is $k  \times n$, $\overline{x}$ is $n \times 1$

- related to [[linear independence]], since the null space of a linearly independent matrix $A$ has exactly one $\mathbf{x}$ (excluding the trivial solution) s.t. $A\mathbf{x}=\mathbf{0}$.
- note that any linear combination of the solutions of $\mathbf{x}$ for $A\mathbf{x}=0$ are also solutions
	- this is called the [[superposition principle]]

- once $\text{ker}\ {A}$ found (space of solns to homogeneous system, $A\mathbf{z}=\mathbf{0}$), we can find the same for the inhomogeneous linear systems:

> [!theorem]
> The linear system $A\mathbf{x}=\mathbf{b}$ has a solution $\mathbf{x}^{*}$ if and only if $\mathbf{B}$ lies in the image of $A$. If this occurs, then $\mathbf{x}$ is a solution to the linear system if and only if: $$\mathbf{x}=\mathbf{x}^{*}+\mathbf{z}$$
> ... where $\mathbf{z}\in \text{ker}\ {A}$ is an element of the kernel of the coefficient matrix

- We can characterize the situations in which a linear system has a unique solution in any of the following equivalent ways:

> [!corollary]
> If $A$ is an $m \times n$ matrix, then the following conditions are equivalent:
> 1. $\text{ker}\ {A}=\left\{ \mathbf{0} \right\}$ i.e. $A\mathbf{x}=\mathbf{0}$ has the unique solution $\mathbf{x}=\mathbf{0}$.
> 2. $\text{rank}\ {A}=n$
> 3. The linear system $A\mathbf{x}=\mathbf{b}$ has no free variables
> 4. The system $A\mathbf{x}=\mathbf{b}$ has a unique solution for each $\mathbf{b}\in \text{img}\ {A}$

- so uniqueness is universal
- direct equivalents can be found for square matrices too

> [!example]
> Compute the kernel of: $A=\begin{pmatrix} 1&-2&0&3\\2&-3&-1&-4\\3&-5&-1&-1 \end{pmatrix}$
> #### Solution
> - Solve $A\mathbf{x}=\mathbf{0}$, place in row echelon: $$U=\begin{pmatrix} 1&-2&0&3\\0&1&-1&-10\\0&0&0&0 \end{pmatrix}$$
> - ... which corresponds to equations $x-2y+3w=0$, $y-z-10w=0$. Free variables $z,w$
> $$
> x=
> \begin{pmatrix}
> x \\
> y \\
> z \\
> w 
> \end{pmatrix}=
> \begin{pmatrix}
> 2z+17w \\
> z+10w \\
> z \\
> w 
> \end{pmatrix}=z
> \begin{pmatrix}
> 2 \\
> 1 \\
> 1 \\
> 0 
> \end{pmatrix}+w
> \begin{pmatrix}
> 17 \\
> 10 \\
> 0 \\
> 1 
> \end{pmatrix}
> $$
> - describes general vector in $\text{ker}\ {A}$, the 2d subspace of $\mathbb{R}^{4}$ spanned by $(2,1,1,0)^{T}$, $(17,10,0,1)^{T}$

