#ch4 
- allows for discovery of [[orthogonal bases]]

> [!definition]
> Let $W$ denote a finite-dimensional inner product space. Assume a basis $\mathbf{w}_{1},...,\mathbf{w}_{n}$ of $W$ where $n=\text{dim}(W)$ exists. Then, we can construct an orthogonal basis $\mathbf{v}_{1}, ..., \mathbf{v}_{n}$. Following the process to construct said orthogonal basis vector, we derive the general **Gram-Schmidt** formula: $$\mathbf{v}_{k}=\mathbf{w}_{k}-\sum_{j=1}^{k-1}\frac{\left\langle \mathbf{w}_{k}, \mathbf{v}_{j} \right\rangle}{\lvert \lvert \mathbf{v}_{j} \rvert  \rvert ^{2}}\cdot\mathbf{v}_{j},\ \ k=1,...,n$$

- the inner term of the sum is directly derived from the definition of [[projection]]
