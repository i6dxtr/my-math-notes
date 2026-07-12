#ch8

> [!definition]
> The equation $$A=U\Sigma V^{T}$$... can be used to compute the *singular values* of $A$, the values that describe the degree of variance inside the system. 
> Alternatively, we may express it in terms of $U$: $$U=AV\Sigma^{-1}$$... or in terms of the left singular values of $A$.
> #### Components
> - $A$ is some $m \times n$ matrix
> - $U$ a is $m \times m$ orthogonal matrix that contains the *left* singular values of $A$
> 	- i.e. the *eigenvectors* of $AA^{T}$
> 	- Exist in the output or column space of $A$
> 		- ... thereby being $m-$dimensional
> 	- Gives us information on where $A$ maps the scaled vectors
> 	- Relationship: $A\mathbf{u}_{j}=\sigma_{j}\mathbf{v}_{i}$
> - $\Sigma$ is the $m \times n$ diagonal matrix containing all the singular values of $A$
> 	- Always real and non-negative
> 	- The same values regardless of left-right perspective
> 	- Are the "scaling factors" in the decomposition
> - $V$ is the $n \times n$ orthogonal matrix containing the *right* singular vectors of $A$
> 	- Are the *columns* of $V$
> 	- Also are the eigenvectors of $A^{T}A$
> 	- Exist in the input/row space of $A$
> 		- ... thereby being $n-$dimensional
> 	- Give the principle directions in input space
> Recall: an input space is the *domain space*, all possible input vectors $\mathbf{x}$ that can go into $A$, i.e. if $A$ is $n \times m$ then the input space is $\mathbb{R}^{n}$
> #### Geometric Interpretation
> - $V^{T}$ *rotates* vectors to align with principal directions
> - $\Sigma$ stretches and scales along these directions
> - $U$ rotates to the final orientation
> #### Properties
> - for $U$:
> 	- Orthonormal columns: $U^{T}U=I$
> 	- Form basis for column space of $A$
> 	- Shows output directions
> - for $V$:
> 	- Orthonormal columns: $V^{T}V=I$
> 	- Basis for row space of $A$
> 	- Shows input directions
> - for $\Sigma$:
> 	- Contains the singular values as diagonal entries such that $\sigma_{1}\ge \sigma_{2}\cdots \sigma_{n}\le 0$
> 	- $\sigma_{i}=\sqrt{\lambda_{i}}$ where $\lambda_{i}$ are the eigenvalues of $A^{T}A$
> 	- Number of nonzero $\sigma_{j}$ is equal to the rank of $A$
> #### Relationships
> - $AV=U\Sigma$
> - $A^{T}U=V\Sigma ^{T}$
> - $AA^{T}=U\Sigma \Sigma^{T} U^{T}$
> - $A^{T}A=V\Sigma^{T}\Sigma V^{T}$

> [!example]
> - $A^{T}A=\begin{pmatrix} 1&0\\1&1 \end{pmatrix}\begin{pmatrix} 1&1\\0&1 \end{pmatrix}=\begin{pmatrix} 1&1\\1&2 \end{pmatrix}$
> 	- Computation of Gram matrix
> - $\begin{pmatrix} \lambda-1&1\\1&\lambda-2 \end{pmatrix}=( \lambda-1 )( \lambda-2 )-1$
> 	- $=\lambda^{2}-3\lambda+1$
> 	- Finding the characteristic equation
> - $\sigma_{1}^{2}=\frac{3+\sqrt{5}}{2}$
> 	- First eigenvalue of $A^{T}A$
> - $\sigma_{2}^{2}=\frac{3-\sqrt{5}}{2}$
> 	- Second eigenvalue of $A^{T}A$
> - $\Sigma=\begin{pmatrix} \sigma_{1}&0\\0&\sigma_{2} \end{pmatrix}$
> 	- Diagonalized matrix of singular values
> - $\begin{pmatrix} 1&1\\1&2 \end{pmatrix}-\begin{pmatrix} \sigma_{1}^{2}&0\\0&\sigma_{1}^{2} \end{pmatrix}$
> 	- The computation of $A^{T}A-\sigma _{1}^{2}$, revealing the first right singular vector.
> 	- This also serves to find the first eigenvector
> 	- $=\begin{pmatrix} 1-\sigma_{1}^{2}&1\\1&2-\sigma_{1}^{2} \end{pmatrix}$
> 	- row reduce: $\begin{pmatrix} 1-\sigma_{1}^{2}&1\\0&0 \end{pmatrix}$
> 		- The eigenvector
> - so $x_{1}( 1-\sigma_{1}^{2} )+x_{2}=0$
> 	- i.e. the first row of REF$( A^{T}A )$
> - $x_{1}=1$
> 	- Fixing the pivot variable
> - $x_{2}=\sigma_{1}^{2}-1$
> 	- This is the free variable for which we solved for
> - $v_{1}=\begin{pmatrix} 1\\\sigma_{1}^{2}-1 \end{pmatrix}\cdot\frac{1}{\sqrt{1+( \sigma_{1}^{2}-1 )^{2}}}$
> 	- Normalizes eigenvector to be of length 1
> - $V=\frac{1}{\sqrt{1+( \sigma_{1}^{2}-1 )^{2}}}\begin{pmatrix} 1&\sigma_1^{2}-1\\\sigma_{1}^{2}-1&-1 \end{pmatrix}$
> 	- The matrix of right singular variables
> - $u=AV\Sigma^{-1}=\frac{1}{\sqrt{1+( \sigma_{1}^{2}-1 )^{2}}}=\begin{pmatrix} 1&1\\0&1 \end{pmatrix}\begin{pmatrix} 1&\sigma_{1}^{2}-1\\\sigma_{1}^{2}-1&1 \end{pmatrix}\begin{pmatrix} \sigma_{1}^{-1}&0\\0&\sigma_{2}^{-1} \end{pmatrix}$
> 	- Finished equation with terms for $A, V, \Sigma$

#### First application of singular value decomposition
1. Let $\mathbf{x}\in \mathbb{R}^{n}$
2. Take the mean of $\mathbf{x}$ to be $\mu$
	1. $\mu=\frac{1}{n}\sum_{i=0}^{n-1}x\left[ i \right]$
3. Take the variance
	1. $\text{var}( \mathbf{x} )=\frac{1}{n}\sum_{i=0}^{n-1}( x\left[ 1 \right]-\mu )^{2}$
---
1. Center all data first:
	1. Replace $x$ with $x-\mu$
2. Then all samples have mean $\text{var}( x )=\frac{1}{n}\sum_{i=0}^{n-1}x\left[ i \right]^{2}$
*e.g.* $\begin{pmatrix} 1\\4\\3 \end{pmatrix}$:
1. $\mu=\frac{8}{3}$
2. $x-\mu=\begin{pmatrix} -\frac{5}{3}\\\frac{4}{3}\\\frac{1}{3} \end{pmatrix}$

Recall how if two samples ($x,y$) are *uncorrelated*, then their dot product is equal to 0

> [!remark]
> If two samples $x,y$ are *uncorrelated*, then$$\text{var}( x+y )=\text{var}( x )+\text{var}( y )$$

==Goal==: Take $A$ to be a data matrix, with linearly independent columns that are tall (e.g. $162 \times 5$).
Rearrange the data in $A$ such that:
1. We take the trace for the total variance (sum of diagonal entries): $$\text{var}_{\text{tot}}(A)=\text{Tr}( A^{T}A )$$
	1. $\text{Tr}( B )=\sum_{i=0}^{n-1}B\left[ i,j \right]$, where $B$ is the square
2. New coordinates are uncorrelated
3. New coordinates are arranged in decreasing order
	1. greatest $\rightarrow$ least variance
- If $A$, $V$ are $n \times k$, then:
	1. $\text{var}_{\text{tot}}(AV)=\text{Tr}( V^{T}A^{T}AV )$
		1. $=\text{Tr}( VV^{T}A^{T} )$ ? maybe
- Take $AV=U\Sigma$ where $A,V,U$ are $n \times k$, $\Sigma$ is $k \times k$
	1. Take $\Sigma$ to be diagonal
		1. ... where $\Sigma\left[ i,i \right]=\lvert\lvert u\left[ i,i \right] \rvert\rvert$
		2. diagonal entries in decreasing order
	2. We want to rewrite $U$ to be orthonormal
		1. $A=U\Sigma V^{T}$
	3. The SVD accomplishes exactly this...
- Observe: $U,\Sigma, V^{T}$ *all have valuable information*
- We use this to cluster data wisely
	- $U=$ old data in new coordinates
		- $U=AV\Sigma^{-1}$, 
			- $\Sigma^{-1}$ helps to measure variance by serving as a way to determine how different axis are to each other 

