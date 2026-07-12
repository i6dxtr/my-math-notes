#ch1
- A given *matrix* $A$ is an $m \times n$ matrix, meaning $A$ has $m$ rows and $n$ columns:

> [!example]
> $$
> A=\begin{pmatrix}
> 3 & 7 \\
> 8 & 4  \\
> 1 & 2
> \end{pmatrix}\text{ is a }3 \times 2\text{ matrix}
> $$

> [!remark]
> - Using NumPy notation:
> 	- $A[i,j]=$ the $ij$ entry of $A$
> 	- $A[0,1]=7$
> 	- $A[:,0]=$ "every *x*". *here, means every ==row==*
>  = $\langle 3,8,1 \rangle$
> 	- $A[2, :]=$ $[1, 2]$

> [!example]
> $$
> \begin{align} B&=\begin{pmatrix}
> 1 & 2 & 3 \\
> 4 & 5 & 6 \\
> 7 & 8 & 9
> \end{pmatrix}  \\
> B[1:,0:2]&=\begin{pmatrix}
> 4 & 5 \\
> 7 & 8
> \end{pmatrix}\end{align}
> $$

- We can perform [[Row Operations]] on them to place them in reduced form
	- Additionally, we can perform any of the [[Matrix Operations]]
- Any [[Image]] can be represented by matrices
- All matrices are composed of 4 fundamental subspaces
	- two of which include the [[kernel space]] and column space
	- we glean information from them using the property of [[linear independence]]

#### More Book Info:
- we use the following notation:
	$$
	A=
	\begin{pmatrix}
	a_{11} &  a_{12} & ... & a_{1n} \\
	a_{21} & a_{22} & ... & a_{2n} \\
	... & ... & ... & ... \\
	a_{m1} & a_{m2} & ... & a_{mn}
	\end{pmatrix}
	$$
	... for a general matrix of size $m \times n$.
- column vector is $m \times1$ 
	- the more important one, always represents a vector
- row vector is $1 \times n$
- general linear system ($m$ equations, $n$ unknowns):
	$$
	\begin{align}
	a_{11} x_{1}+a_{12}x_{2}+...+a_{1n}x_{n}&=b_{1} \\
	a_{21}x_{1}+a_{22}x_{2}+...+a_{2n}x_{n}&=b_{2} \\
	...& \\
	a_{m1}x_{1}+a_{m2}x_{2}+...+a_{mn}x_{n}&=b_{m}
	\end{align}
	$$
	... composed of 3 components:
- the $m \times n$ *coefficient matrix*: w/ entries $a_{ij}$
- the column vector $\overline{x}=\begin{pmatrix} x_{1}\\x_{2}\\...\\x_{n} \end{pmatrix}$ containing all unknowns
- the column vector $\overline{b}=\begin{pmatrix} b_{1}\\b_{2}\\...\\b_{m} \end{pmatrix}$ containing *right-hand sides* (of the $=$ sign)

