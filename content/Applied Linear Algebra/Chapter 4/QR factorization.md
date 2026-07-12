#ch4 
- a "reinterpretation" of the [[Gram-Schmidt Process]]
- procedure:
	- take $\mathbf{w}_{1},...,w_{n}$, a basis of $\mathbb{R}^{n}$, and $\mathbf{u}_{1},...,\mathbf{u}_{n}$, the corresponding orthonormal basis resulting from using gram-schmidt
	- assemble each to form nonsingular $n \times n$ matrices $Q, A$: $$A=(\mathbf{w}_{1}\ \ \mathbf{w}_{2}\ \ \cdots \ \ \mathbf{w}_{n}),\ Q=(\mathbf{u}_{1}\ \ \mathbf{u}_{2}\ \ \cdots\ \ \mathbf{u}_{n})$$
	- Since $\mathbf{u}_{i}$ for orthonormal basis, $Q$ is an orthogonal matrix
	- afterwards, recast into following equivalent matrix form: 
$$
\begin{align}
A=QR &&\text{where }R=
\begin{pmatrix}
r_{11}&R_{12}&\cdots&r_{1n}\\ 0&r_{22}&...&r_{2n} \\ \cdots&\cdots&\cdots&\cdots \\ 0&0&\cdots&r_{nn}
\end{pmatrix}
\end{align}
$$
- $R$ is upper-triangular
- only requirement on $A$ is that its columns form a basis of $\mathbb{R}^{n}$
	- so any nonsingular matrix

> [!theorem]
> Every nonsingular matrix can be factored, $A=QR$, into the product of an orthogonal matrix $Q$ and an upper triangular matrix $R$. The factorization is unique if $R$ is *positive upper triangular*, meaning that all its diagonal entries are positive

Suppose $A = [a_1 \; a_2 \; ... \; a_n]$ (columns). To get $Q = [q_1 \; q_2 \; ... \; q_n]$, we:

1) First column:
   - $q_1 = \frac{a_1}{\|a_1\|}$
   - $r_{11} = \|a_1\|$ (this is the scaling factor we used)

2) Second column:
   - $r_{12} = q_1^T a_2$ (projection of $a_2$ onto $q_1$)
   - $q_2 = \frac{a_2 - r_{12}q_1}{\|a_2 - r_{12}q_1\|}$
   - $r_{22} = \|a_2 - r_{12}q_1\|$ (the scaling factor)

3) Third column:
   - $r_{13} = q_1^T a_3$
   - $r_{23} = q_2^T a_3$
   - $q_3 = \frac{a_3 - r_{13}q_1 - r_{23}q_2}{\|a_3 - r_{13}q_1 - r_{23}q_2\|}$
   - $r_{33} = \|a_3 - r_{13}q_1 - r_{23}q_2\|$

The pattern is:
- $r_{ij}$ entries are the dot products $q_i^T a_j$ for $i < j$
- $r_{ii}$ entries are the norms of the vectors after subtracting all previous projections
- $r_{ij} = 0$ for $i > j$ (making $R$ upper triangular)

So $R$ captures both:
1) The projection coefficients (off-diagonal entries)
2) The normalization factors (diagonal entries)
that we used while creating $Q$.