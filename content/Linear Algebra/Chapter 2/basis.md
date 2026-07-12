 #ch2

> [!definition]
> If $V\subset \mathbb{R}^{n}$ is a [[Subspaces|subspace]], then a set $B=(b_{1}, ..., b_{k})$ is a **basis** for $V$ if:
> 1. $\text{span}(B)=V$ *(existence)*
> 2. $B$ is [[linearly independent]] *(uniqueness)*

> [!theorem]
> Every basis of $\mathbb{R}^{n}$ consists of exactly $n$ vectors. Furthermore, a set of $n$ vectors $\overline{v}_{1}, \overline{v}_{2}, ..., \overline{v}_{n}\in\mathbb{R}^{n}$ is a basis *if and only if* the $n \times n$ matrix $A=(\overline{v}_{1}\ ...\ \overline{v}_{n})$ is nonsingular: $\text{rank}(A)=n$

- obviously follows from being, by definition, [[linear independence|linearly independent]]
- this fact is crucial in establishing the definition of [[dimension]]

> [!theorem]
> Suppose $V$ is a $n-$dimensional vector space. Then:
> 1. Every set of more than $n$ elements of $V$ is linearly dependent.
> 2. No set of fewer than $n$ elements spans $V$
> 3. A set of $n$ elements forms a [[basis]] *if and only if* it [[span|spans]] $V$
> 4. A set of $n$ elements forms a basis *if and only if* it is linearly independent

- basically, when we know dimension of $V$, to check if collection has correct # of elements, establish either a.) it spans or b.) its linear independence.
	- $\mathbf{v}_{1}, ..., \mathbf{v}_{m} \in \text{span}(V)\longrightarrow \text{dim}(V)\leq m$
	- $\text{basis}(V)=\mathbf{v}_{1},...,\mathbf{v}_{n}\longrightarrow \forall x\in V\ \ \mathbf{x}=c_{1}\mathbf{v}_{1}+...+c_{n}\mathbf{v}_{n}=\sum_{i=1}^{n}c_{i}\mathbf{v}_{i}$
		- recall: $\mathbf{x}$ must be written uniquely

> [!example]
> The standard basis of the space $\mathcal{P}^{n}$ of polynomials of degree $\leq n$ is given by the $n+1$ monomials $1, x,x^{2},...,x^{n}$. So, we conclude that $\text{dim}(\mathcal{P})=n+1$. Also, all basis have $\text{dim}=1$
> - note, not all collections of $n+1$ polys in $\mathcal{P}^{n}$ is a basis

### Examples

> [!example]
> The standard basis of $\mathbb{R}^{n}$:
> $$
> \begin{align}
> &&\overline{e}_{1}=\begin{pmatrix} 1\\0\\0\\...\\0\\0 \end{pmatrix},&& \overline{e}_{2}=\begin{pmatrix} 0\\1\\0\\...\\0\\0 \end{pmatrix}, &&\overline{e}_{n}=\begin{pmatrix} 0\\0\\0\\...\\0\\1 \end{pmatrix}
> \end{align}
> $$

> [!example]
> Are the columns of ... 
> $$
> \begin{pmatrix}
>  1 & 1 & 1 \\
> 0 & 1 & 1 \\
> 0 & 0 & 1 
> \end{pmatrix}
> $$
> ... linearly independent?
>
> *Solution*: Yes,
> $$x_{1}\langle 1,0,0 \rangle+x_{2}\langle 1,1,0 \rangle+x_{3}\langle 1,1,1 \rangle=\langle 0,0,0 \rangle$$
> Solving this system of equations:
> $$
> \begin{pmatrix}
>  1 & 1 & 1 \\
> 0 & 1 & 1 \\
>  0 & 0 & 0
> \end{pmatrix}, x_{1}=x_{2}=x_{3}=0\text{ is the only solution.}
> $$
> Row operations:
> $$
> \begin{pmatrix}
>  1 & 1 & 1 \\
> 0 & 1 & 1 \\
> 0 & 0 & 0 
> \end{pmatrix}\rightarrow x_{3}\text{ free variable}, x_{2}=-x_{3}, x_{1}=-2x_{3}
> $$
> - $\infty$ many solutions $\longrightarrow$ linearly independent

#### Textbook Problem Set

> [!example]
> Determine which of the following sets of vectors are bases of $\mathbb{R}^{2}$:
> - $\begin{pmatrix} 1\\-3 \end{pmatrix},\begin{pmatrix} -2\\5 \end{pmatrix}$
> 	- Yes, since $\text{rref}=\begin{pmatrix} 1&-2\\0&1 \end{pmatrix}$
> - $\begin{pmatrix} 1\\-1 \end{pmatrix}, \begin{pmatrix} -1\\1 \end{pmatrix}$
> 	- No:
> 		$$
> 		\begin{align}
> 		\begin{pmatrix}
> 		1 & -1 \\
> 		-1 & 1
> 		\end{pmatrix}\longrightarrow
> 		\begin{pmatrix}
> 		1 & -1 \\
> 		0 & 0
> 		\end{pmatrix}
> 		\end{align}
>
> 		$$
> 		... so no solution for $x_{2}+y_{2}=0$

> [!example]
> Given $\begin{pmatrix} 4\\0\\1 \end{pmatrix}, \begin{pmatrix} 2\\1\\0 \end{pmatrix},$ and $\begin{pmatrix} 2\\-1\\1 \end{pmatrix},\begin{pmatrix} 0\\2\\-1 \end{pmatrix}$:
> 1. Show that the sets of vectors are two different bases for the plane $x-2y-4z=0$
> 2. Show how to write both elements of the second basis as linear combinations of the first
> 3. Find a third basis
> #### Proof.
>  Let $\mathbf{x}=\begin{pmatrix} 4\\0\\1 \end{pmatrix}$ and $\mathbf{y}=\begin{pmatrix} 2\\1\\0 \end{pmatrix}$. Given plane equation $x-2y-4z=0$, we note $x_{2}=0$ and $y_{3}=0$. Therefore, the basis across the plane where $x^{2}=0, y^{2}=0$ i.e where $x-4z=0$ is:
>  $$
>  \left(\begin{array}{cc|c}
>  4 & 2 & 0 \\
>  1 & 0 & 0
>  \end{array}\right)\longrightarrow
>  \left(\begin{array}{cc|c}
>  1 & 0 & 0 \\
>  0 & 2 & 0
>  \end{array}\right)
>  $$
>  ... which is clearly a basis for $\mathbb{R}^{2}$ under the constraints given by the plane equation. Note the new vectors $\mathbf{y}=\left\{ 1,0 \right\}$ and $\mathbf{x}=\left\{ 0,2 \right\}$
> Now observe where $x_{3}=0, y_{3}=0$ i.e $x-4z=0$:
> $$
> \left(\begin{array}{cc|c}
>   4 & 0 & 0 \\
> 2 & 1 & 0
> \end{array}\right)\longrightarrow 
> \left(\begin{array}{cc|c}
>   4 & 0 & 0 \\
> 0 & 1 & 0
> \end{array}\right)
> $$
> ... which is also a basis. Note that $\mathbf{x}=\left\{ 4,0 \right\}$ and $\mathbf{y}=\left\{ 0,1 \right\}$. Clearly, $\mathbf{x}=\left\{ 0,2 \right\}\neq \left\{ 4,0 \right\}$ and $\mathbf{y}=\left\{ 1,0 \right\}\neq \left\{ 0,1 \right\}$.
> Thus we say that each $\mathbf{x}, \mathbf{y}$ are *linearly independent* of one another; thereby denoting that they are different bases

> [!example]
> Find a basis for:
> 1. The plane given by the equation $z-2y=0$ in $\mathbb{R}^{3}$
> 2. The plane given by the equation $4x+3y-z=0$ in $\mathbb{R}^{3}$
> 3. The hyperplane $x+2y+z-w=0$ in $\mathbb{R}^{4}$
> #### Proof.
> 1. We can define two basis vectors in the subspace $z-2y=0$ in $\mathbb{R}^{3}$ by the following:
> 	$$
> 	\begin{align}
> 	\mathbf{x}=\begin{pmatrix} 1\\0 \end{pmatrix}, \mathbf{y}=\begin{pmatrix} 0\\1 \end{pmatrix}
> 	\end{align}
> 	$$
> 	... which spans $\mathbb{R}^{3}$ in the case where $x=0$. This is given by the equation.
> 2. text here
> 3. The standard basis for $\mathbb{R}^{4}$ is sufficient in this case, since $x,y,z,w$ have well-defined integer coefficients that are non-zero. $$\mathbf{e}_{1}=\begin{pmatrix} 1\\0\\0\\0 \end{pmatrix}, \mathbf{e}_{2}=\begin{pmatrix} 0\\1\\0\\0 \end{pmatrix}, \mathbf{e}_{3}=\begin{pmatrix} 0\\0\\1\\0 \end{pmatrix}, \mathbf{e}_{4}=\begin{pmatrix} 0\\0\\0\\1 \end{pmatrix}$$

link: [[Subspaces]] [[linear independence]]