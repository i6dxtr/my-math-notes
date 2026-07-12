 #ch1
#### Lecture
==Matrix Multiplication==
- $A$ is $7 \times6$
	- $B$ is $6 \times101$
	- $AB=A@B$ is $7 \times101$
- $A$ is $m \times n$, $b$ is $n \times1$ [[matrix]]
- Then $Ab$ is a $m \times1$ matrix

- **General Formula** (for matrix multiplication)

> [!corollary]
> $$Ab=b[0]A[:,0]+b[1]A[:,1]+...+b[n-1]A[:,n-1]$$

> [!example]
> $$
> \begin{pmatrix}
> 5 & 7 \\
> 4 & 1  \\
> 0 & -1
> \end{pmatrix} \times
> \begin{pmatrix}
> 2 \\
> 1
> \end{pmatrix} =
> \begin{pmatrix}
> 5\cdot2+7\cdot1 \\
> 4\cdot2+1\cdot1 \\
> 0\cdot2+-1\cdot1
> \end{pmatrix}
> $$
> - $A$ is $m \times n$, $B$ is $n \times K$
> - $AB[:, j]=\sum B[i,j]A[:,j]$
> $$
> \begin{pmatrix}
>  5 & 6 \\
> 2 & 1 
> \end{pmatrix} \times 
> \begin{pmatrix}
>  -1 & 1 \\
> 0 & 1 
> \end{pmatrix}=
> \begin{pmatrix}
>  5\cdot(-1)+6\cdot0 & 5\cdot1+6\cdot1 \\
> 2\cdot(-1)+1\cdot0 & 2\cdot1+1\cdot1 
> \end{pmatrix}

#### Book
- 3 operations:
	- Matrix Addition
		- is commutative, associative. predictable
	- Matrix Multiplication
		- see above
	- Scalar Multiplication
		- multiply each entry by some number
##### More on matrix multiplication:
- the product of row vector $\overline{a}$ and column vector $\mathbf{x}$ having same # of entries defined as: $$\overline{ax}=(a_{1}\ \ a_{2}\ \ ...\ \ a_{n})\begin{pmatrix} x_{1}\\x_{2}\\...\\x_{n} \end{pmatrix}=a_{1}x_{1}+a_{2}x_{2}+...+a_{n}x_{n}=\sum_{k=1}^{n}a_{k}x_{k}$$
- generally, if $A$ is $m \times n$ and $B$ is $n \times p$ s.t. the **number of columns in $A$ are equal to the rows in $B$**, then matrix product $C=AB$ defined as:
	$$
	c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
	$$
	- result is $m  \times p$ matrix whose $(i,j)$ entry equals vector product of $i^{th}$ row of $A$ and the $j^{th}$ column of $B$

> [!example]
> $$
> A\overline{x}=
> \begin{pmatrix}
>  1 & 2 & 1 \\
> 2 & 6 & 1 \\
> 1 & 1 & 4 
> \end{pmatrix}
> \begin{pmatrix}
>  x \\
> y \\
> z 
> \end{pmatrix}=
> \begin{pmatrix}
>  x+2y+z \\
> 2x+6y+z \\
> x+y+4z 
> \end{pmatrix}
> $$
> - which is the same as $A\overline{x}=\overline{b}$.\
> - note that result matrix is $3\times 1$

