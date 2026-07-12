 #ch2

- We can locate the [[basis]] for the [[kernel space]] of matrices:
$$
\begin{align}
A&& B=\text{ref}(A)  \\
\overline{x}\in \text{null}(A) && .. \\
A\overline{x}=\overline{0} \leftarrow && \rightarrow B\overline{x}=\overline{0} \\
\text{Conclude:} &&  \\
\text{null}(A)=\text{null}(B)
\end{align}
$$

> [!example]
> Find a basis for $\text{null}(A)$
> $A$ is a $3 \times 5$ matrix and:
> $$
> \text{ref}(A)=
> \begin{pmatrix}
> 1 & 2 & 0 & 1 & 1 \\
> 0 & 0 & 1 & 1 & 2 \\
> 0 & 0 & 0 & 0 & 0
> \end{pmatrix}
> $$
> 1. Identify free variables:
> 	 $x_{2}, x_{4}, x_{5}$
> 	 $x_{3}=-x_{4}-2x_{5}$
> 	 $x_{1}=-2x_{2}-x_{4}$
> - Easiest way to write down a basis: 
> $$
> > \begin{align}
> \underline{\text{Vector 1}} && \underline{\text{Vector 2}} &&& \underline{\text{Vector 3}}  \\
> x_{2}=1 && x_{2}=0 &&& x_{2}=0 \\
> x_{4}=0 && x_{4}=1 &&& x_{4}=0  \\
> x_{5}=0 && x_{5}=0 &&& x_{5}=1 \\
> \begin{pmatrix}
> -2 \\
> 1 \\
> 0 \\
> 0 \\
> 0
> \end{pmatrix} &&
> \begin{pmatrix}
> -1\\
> 0 \\
> -1 \\
> 1 \\
> 0
> \end{pmatrix} &&&
> \begin{pmatrix}
> -1 \\
> 0 \\
> -2 \\
> 0 \\
> 1
> \end{pmatrix}
> \end{align}
>
> $$
> Why do these 3 vectors span $\text{null}(A)$?
> - $\text{null}(A)$ is described by:
> $$
> > \begin{align}
> \begin{pmatrix}
> -2x_{2}-x_{4}-x_{5} \\
> x_{2} \\
> -x_{4}-2x_{5} \\
> x_{4} \\
> x_{5}
> \end{pmatrix} = x_{2}
> \begin{pmatrix}
> -2 \\
> 1 \\
> 0 \\
> 0 \\
> 0
> \end{pmatrix}+x_{4}
> \begin{pmatrix}
> -1 \\
> 0 \\
> -1 \\
> 1 \\
> 0
> \end{pmatrix} +x_{5}
> \begin{pmatrix}
> -1 \\
> 0 \\
> -2 \\
> 0 \\
> 1
> \end{pmatrix}
> \end{align}
>
> $$

- 

