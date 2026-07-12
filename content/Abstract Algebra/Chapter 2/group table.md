#ch2
- a visual representation of the association between different elements in a given [[Groups|group]] by their operation:

> [!example]
> Let $A$ be the following matrix:
> $$
> > \begin{align}
> A&=\begin{pmatrix}
> 0 & 1 \\
> -1 & 0
> \end{pmatrix} \\
> A^{2}&=
> \begin{pmatrix}
> 0 & 1 \\
> -1 & 0
> \end{pmatrix}\cdot
> \begin{pmatrix}
> 0 & 1 \\
> 0 & -1
> \end{pmatrix}=
> \begin{pmatrix}
> -1 & 0 \\
> 0 & -1
> \end{pmatrix}=-I \\
> A^{3}&=-A=
> \begin{pmatrix}
> 0 & -1 \\
> 1 & 0
> \end{pmatrix} \\
> A^{4}&=I \\
> G&=\{ I, A, -I, -A \} \\
> \ &... \text{ is a group under matrix multiplication}.
> \end{align}
> $$
> The associated table:
> $$
> \begin{array}{c|cccc}
> \ \  \cdot & \underline{I} & \underline{A} & \underline{-I} & \underline{A} \\
> \ \ \underline{I} & I & A & -I & -A \\
> \ \ \underline{A} & A & -I & -A & I \\
> -\underline{I} & -I & -A & I & A \\
> -\underline{A} & -A & I & A & -I
> \end{array}
> $$
> - see how $G$ is abelian; diagonal fully + or -

> [!example]
> $G=\{ 1,2,5,7 \}$ under $\cdot _{8}$ (multiplication modulo 8)
> - eg. $3\cdot_{8}5=15\text{ mod }8=7$
> $$
> \begin{array}{c|cccc}
> \underline{\cdot_{8}} & \underline{1} & \underline{3} & \underline{5} & \underline{7} \\
> 1 & 1 & 3 & 5 & 7 \\
> 3 & 3 & 1 & 7 & 5 \\
> 5 & 5 & 7 & 1 & 3 \\
> 7 & 7 & 5 & 3 & 1
> \end{array}
> $$

