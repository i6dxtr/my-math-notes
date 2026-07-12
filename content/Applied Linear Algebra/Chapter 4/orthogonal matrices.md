#ch4 

> [!definition]
> A square matrix $Q$ is called **[[orthogonality|orthogonal]]** if it satisfies: $$Q^{T}Q=QQ^T=I$$

> [!remark]
> The orthogonality condition implies inversion: $$Q^{-1}=Q^{T}$$
> - recall definition of inverse

- both conditions equivalent, therefore a matrix is orthogonal *if and only if its inverse is equal to it's transpose*.
	- i.e. $I$ is orthogonal
- orthogonal matrices can be either [[(im)proper orthogonal matrix|proper or improper]].

> [!corollary]
> A matrix $Q$ is orthogonal if and only if its columns form an *orthonormal basis* with respect to the Euclidean dot product on $\mathbb{R}^{n}$

> [!proof]
> Let $\mathbf{u}_{1},...,\mathbf{u}_{n}$ be the columns of $Q$. Then $\mathbf{u}_{1}^{T},...,\mathbf{u}_{n}^{T}$ are the rows of the transposed matrix $Q^{T}$. The $(i,j)$ entry of the product $Q^{T}Q$ is given as the product of the $i^{th}$ row of $Q^{T}$ and the $j^{th}$ column of $Q$. Thus, the orthogonality requirement implies:
> $$
> \mathbf{u}_{i}\cdot\mathbf{u}_{j}=\mathbf{u}_{i}^{T}\mathbf{u}_{j}=\bigg\langle \begin{array}{cc}
>   1, &&i=j\\ 0,&&i\neq j
> \end{array}
> $$
> ... which are the conditions for $\mathbf{u}_{1},...,\mathbf{u}_{n}$ to form an orthonormal basis.

- example: written, orthogonal matrices: transpose inverseness

> [!corollary]
> An orthogonal matrix $Q$ has determinant $\text{det}\ Q=+-1$

> [!proof]
> Taking determinant: 
> $$
> > \begin{align}
> 1&=\text{det}\ I \\
> &=\text{det}(Q^{T}Q) \\
> &=\text{det}\ Q^{T}\ \text{det}\ Q\\
> &=(\text{det}\ Q)^{2} \\
> \text{QED}
> \end{align}
>
> $$

link: [[Orthogonality]]