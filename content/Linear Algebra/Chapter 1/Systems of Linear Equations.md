  #ch1
General process of solving:

> [!corollary]
> 1. Rewrite in vector form
> 2. Rewrite as matrix multiplication
> 3. Fill as "augmented matrix"
> 4. Solve resulting matrix using the [[Row Operations]]

#### Solutions of Linear Systems
consider:
$$
\begin{align}
x+2y+z&=2 \\
3x+6y+z&=7  \\
x+y+4z&=3
\end{align}
$$
- Linearity:
	- unknowns only in first power
	- no product terms ($xy, xyz$)
- Scalar multiple operation:
	- eliminate variables in equation by order of appearance:
$$
\begin{align}
x+2y+z&=2 \\
2y-z&=3 && \rightarrow \text{ first }x\text{ eliminated from second equation} \\
x+y+4z&=3
\end{align}
$$
$$
\begin{align}
x+2y+z&=2 \\
2y-z&=3 && \rightarrow \text{first }x\text{ eliminated in third equation}\\
-y+3z&=1
\end{align}
$$
- second and third equations now a *subsystem* involving only two unknowns
- once we solve the subsystem for $y$ and $z$, we can substitute the results into the first equation
	- meaning we'd only have to solve for a single linear equation ($x$)
$$
\begin{align}
x+2y+z&=2 \\
2y-z&=3 && \rightarrow \text{Eliminate }y\text{ from third equation}\\
\frac{5}{2}z&=\frac{5}{2}
\end{align}
$$
- this is the simple system, in *triangular form*
- from here, we can use **back substitution**
	- solve last equation first, requiring that $z=1$
	- substitute into second to last, such that $2y-1=3$
	- finally, substitute both into first equation s.t. $x+5=2$
- the solution: $$x=-3, y=2, z=1$$
- moreover, we observe that this system has a unique solution

> [!example]
> $$
> > \begin{align}
> 3x_{1}-7x_{2}&=8 \\
> 5x_{1}+x_{2}&=1
> \end{align}
>
> $$
> *Solution*:
> 1. Rewrite in vector form:
> $$
> \left(\begin{array}{c|c}
>  3x_{1}-7x_{2} & 8 \\
> 5x_{1}+x_{2} & 1 
> \end{array}\right)
> $$
> 2. Rewrite as matrix multiplication
> $$
> \begin{pmatrix}
>  3 & -7 \\
> 5 & 1 
> \end{pmatrix}\cdot
> \begin{pmatrix}
>  x_{1} \\
> x_{2} 
> \end{pmatrix}
> =
> \begin{pmatrix}
>  8 \\
> 1 
> \end{pmatrix}
> $$
> 3. Fill the "augmented matrix" (too much junk)
> $$
> \left(\begin{array}{cc|c}
>  3 & -7 & 8 \\
> 5 & 1 & 1 
> \end{array}\right)
> $$
> 4. Solve resulting matrix (starting with above using row operations)
> $$
> \left(\begin{array}{cc|c}
>  3 & -7 & 8 \\
> 5 & 1 & 1 
> \end{array}\right)\longrightarrow ^{\frac{5}{3}R_{1}, R_{2}\rightarrow R_{1}} 
> \left(\begin{array}{cc|c}
>  3 & -7 & 8 \\
> 0 & \frac{38}{3} & -\frac{37}{3} 
> \end{array}\right)
> $$
> $$
> \begin{align}
> 3x_{1}-7x_{2}&= 8 \\
> \frac{38}{3}x_{2}&=-\frac{37}{3} \\ \\
> x_{2}&-=\frac{37}{38} \\
> x_{1}&=\frac{8+7\left( -\frac{37}{38} \right)}{3}
> \end{align}
> $$

A unique example:

> [!example]
> $$
> \begin{pmatrix}
> x_{1} \\
> x_{2} \\
> x_{3}
> \end{pmatrix}=
> \begin{pmatrix}
> \frac{7}{3} \\
> \frac{1}{3} \\
> -\frac{2}{3}
> \end{pmatrix}
> $$
> - all three have unique solution, see:
> $$
> \begin{align} x_{1}+x_{2}&=7 \\ 2x_{1}+2x_{2}&=5 \\ &\text{No solution.} \end{align}
> $$
> - via augmented matrix:
> $$
> \left(\begin{array}{cc|c}
> 1 & 1 & 7 \\
> 2 & 2 & 5
> \end{array}\right)\longrightarrow
> \left(\begin{array}{cc|c}
> 1 & 1 & 7 \\
> 0 & 0 & -9
> \end{array}\right)
> $$
>    - $0=9$, no solution.

> [!corollary]
> - $Ax=b$ has a unique solution for any $n \times1\ b$. Moreover:
> - $x=A^{-1}b$

> [!remark]
> 1. $A\longrightarrow$ np.inv(A)$\cdot$b
>    $b\longrightarrow$ np.linalg.solve(A,b)
> 2. For human-to-human interaction, the inverse is useful.

##### Review
- two noteworthy methods:
	- same number of equations as unknowns (single solution)
	- general solution 

[[Row Operations]]