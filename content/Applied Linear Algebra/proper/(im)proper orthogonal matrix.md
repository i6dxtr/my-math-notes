#ch4
- an [[orthogonal matrices|orthogonal matrix]] is called *proper* or *special* if it has determinant $+1$
	- the columns would form a right-handed basis of $\mathbb{R}^{n}$
- conversely, an *improper* orthogonal matrix w/ $\text{det}=-1$ corresponds to a left-handed basis in a mirrored image space

> [!corollary]
> The product of two orthogonal matrices is also orthogonal

> [!proof]
> Implication:
> $$
> > \begin{align}
> Q_{1}^{T}&Q_{1}=I=Q_{2}^{T}Q_{2}\\
> &\longrightarrow\ (Q_{1}Q_{2})^{T}(Q_{1}Q_{2})=Q_{2}^{T}Q_{1}^{T}Q_{1}Q_{2}=Q_{2}^{T}Q_{2}=I \\
> \text{QED}
> \end{align}
>
> $$

- implies the set of all orthogonal matrices form a *group*, i.e. the orthogonal group