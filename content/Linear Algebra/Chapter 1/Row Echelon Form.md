 #ch1

> [!definition]
> We say a set $A$ is an $n \times m$ [[Matrix|matrix]] (p. 59) that is in row-echelon form if it looks like the following:
> $$
> \begin{pmatrix}
>  \bf{*} & * &  * & * & ....  \\
> 0 & 0 & * & * & .... \\
> 0 & 0 & 0 & * & .... \\
> ...  \\
> 0 & 0 & ... & 0 & 0
> \end{pmatrix}
> $$
> - The numbers ( \* ) are non-zero and are called *pivots*
> 	- $\text{rank}$ is the same as the number of pivots
> - Any matrix can be put in row-echelon form via the 3 [[Row Operations|row operations]]
> - The number of pivots in a row-echelon is the *rank* of the matrix.
> - The columns in top rows can start with $0$ and still be in *ref*

> [!remark]
> $A$ is an $m \times n$ matrix and $B$ is a $m  \times n$ matrix, so $B$ is a *ref* of $A$
> - $\overline{x} \in \mathbb{R}^{n}$ satisfies $A\overline{x}=\overline{0}$ *if and only if* $B\overline{x}=\overline{0}$.
> $$
> \left(\begin{array}{c|c}
>   A & 0 \\
>  & ... \\
>  & 0
> \end{array}\right)\longrightarrow ^{\text{Operations...}}
> \left(\begin{array}{c|c}
>  B & 0 \\
>  & ... \\
>  & 0 
> \end{array}\right)
> $$

> [!example]
> $$
> B=
> \begin{pmatrix}
> 4 & 1 & 1 & 1 & 1 \\
> 0 & 0 & 2 & 3 & 1 \\
> 0 & 0 & 0 & 1 & 1
> \end{pmatrix}
> $$
> - Pivots:
> 	- $(1,1)$
> 	- $(2,3)$
> 	- $(4,3)$
> - All positions that are *not* pivots are called *free variables*.
> - $B\overline{x}=\overline{0}$ then $\overline{x}\in \mathbb{R}^{?}$ ...
> 	- $B\rightarrow 3 \times 5$
> 	- $\overline{x}\rightarrow5 \times1$
> 	- $\overline{0}\rightarrow 3 \times1$
> - Free variables found in 2nd and last columns
> 1. Identify free variables
> 	$x_{2}, x_{5}$
> 2. Write basic variables in terms of free ones
> 	$x_{4}+x_{5}=0 \longrightarrow x_{4}=-x_{5}$
> 	$2x_{3}+3x_{4}+x_{5}=0\longrightarrow 2x_{3}=-3x_{4}-x_{5}=-3(-x_{5})-x_{5}=2x_{5}=x_{5}$
> 	$4x_{1}=-x_{2}-x_{3}-x_{4}-x_{5}=-x_{2}-(x_{5})-x_{5}=-x_{2}-x_{5}$
> 3. Write final output in vector form:
> $$
> \begin{pmatrix}
>  -\frac{1}{4}x^{2}-\frac{1}{4}x_{5} \\
> x_{2} \\
> x_{5} \\
> -x_{5} \\
> x_{5} 
> \end{pmatrix};x_{2}, x_{5}\text{ are free variables.}
> $$
> - Note that $A\overline{x}=\overline{0}$ has *at least* one solution (the trivial solution)
> 	- $\overline{x}=0$

> [!example]
> $$
> \begin{pmatrix}
>  1 & 0 & 2 & 1 & 1 \\
> 0 & 1 & 0 & 1 & 3 \\
> 0 & 0 & 1 & 2 & 0 
> \end{pmatrix}
> $$
> *Solution*
> $$
> \begin{pmatrix}
>  3x_{4}-x_{5} \\
>  -x_{4}-4x_{5} \\
> -2x_{4} \\
> x_{4} \\
> x_{5}
> \end{pmatrix}
> $$
>
> $$
> \begin{pmatrix}
>  1 & 0 & 0 & 5 & 6 & 7 \\
> 0 & 0 & 1 & 1 & 1 & 1 \\
> 0 & 0 & 0 & 0 & 0 & 7 
> \end{pmatrix}
> $$
> *Solution*
> $$
> \begin{pmatrix}
>  -5x_{4}-6x_{3} \\
> x_{2} \\
> -x_{4}-x_{5} \\
> x_{4} \\
> x_{5} 
> \end{pmatrix}
> $$

> [!corollary]
> If $A$ is a $m  \times n$ matrix, then there exists an $m \times m$ permutation matrix $P$ and an $m \times m$ lower unitriangular matrix $L$ such that $$PA=LU$$... where $U$ is an $m \times n$ row echelon matrix.

> [!corollary]
> A square matrix of size $n \times n$ is nonsingular *if and only if* it's rank is equal to $n$

- i.e. only upper triangular matrices have this property

link: [[Matrix]] [[Row Operations]] 