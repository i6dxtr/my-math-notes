#ch2

> [!definition]
> An operation $*$ on $S$ is commutative means: 
> $$\forall x,y\in S \text{   }x*y=y*x$$

> [!example]
> - $+$ is commutative on $\mathbb{R}$: $x+y=y+x$
> 	- $-$ isn't: $1-2=-1, 2-1=1\neq1-2$
> - $\cdot$ is commutative on $\mathbb{R}$: $xy=yx$
> 	- $/$ isn't: $\frac{1}{2}=\frac{1}{2}, \frac{2}{1}=2\neq \frac{1}{2}$

- With concatenation of strings, $*$ is not commutative:
	- $1101*0110=11010110$, but
	- $0110*1101=01101101$

> [!example]
> Let $M_{2}(\mathbb{R})$ be the set of all $2 \times 2$ matrices (with real entries). Is matrix addition commutative?
> _Solution_: Yes:
> $$
> \begin{pmatrix}
> a & b \\
> c & d
> \end{pmatrix}+
> \begin{pmatrix}
> e & f \\
> g & h
> \end{pmatrix}=
> \begin{pmatrix}
> a+e & b +f \\
> c +g & d + h
> \end{pmatrix}=
> \begin{pmatrix}
> e & f \\
> g & h
> \end{pmatrix}+
> \begin{pmatrix}
> a & b  \\
> c & d
> \end{pmatrix}
> $$
> Is matrix multiplication commutative?
> *Solution*: No:
> $$
> \begin{align}
> \begin{pmatrix}
> 1 & 2 \\
> 3 & 4
> \end{pmatrix}\cdot
> \begin{pmatrix}
> 1 & 0 \\
> 0 & -1
> \end{pmatrix}&=
> \begin{pmatrix}
> 1 & -2 \\
> 3 & -4
> \end{pmatrix} \\
> \begin{pmatrix}
> 1 & 0 \\
> 0 & -1
> \end{pmatrix}\cdot
> \begin{pmatrix}
> 1 & 2 \\
> 3 & 4
> \end{pmatrix}&=
> \begin{pmatrix}
> 1 & 2 \\
> -3 & -4
> \end{pmatrix}
> \end{align}
> $$
> We observe that the outcome of the matrix multiplication does not result in the same matrix for each operation.
>
> Are $\cup$ and $\cap$ commutative?
> *Solution*: Yes:
> $$
> \begin{align}
> A\cup B&=\{ x | x\in A\text{ or }x\in B \} \\
> &=\{ x | x\in B\text{ or }x\in A \} \\
> &=B\cup A.
> \end{align}
> $$
>  - Same process for $\cap$

