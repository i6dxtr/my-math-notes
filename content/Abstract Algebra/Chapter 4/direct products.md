#todo #ch4
[[properties of groups]]

> [!definition]
> If $G$ and $H$ are groups, the Cartesian product, known as the **direct product**, is $$G \times H=\left\{ (a,b)|a\in G,\ b\in H \right\}.$$
> It is also a group with the operation $(a,b)*(a\prime, b\prime)=(a*a\prime, b*b\prime)$

- the operation is not important
- multiplicative notation: $(a,b)(a\prime, b\prime)=(aa\prime, bb\prime)$
- additive notation: $(a,b)+(a\prime,b\prime)=(a+a\prime,b +b\prime)$
example
in $\mathbb{Z}_{2} \times \mathbb{Z}_{3},\ (1,1)+(1,1)=(1+_{2}1, 1+_{3}1)=(0,2)$.
- $\mathbb{Z}_{2}:\left\{ 0,1 \right\}$
- $\mathbb{Z}_{3}:\left\{ 0,1,2 \right\}$
$$
\left(\begin{array}{c|cccccc} 
   & \underline{(0,0)} & \underline{(0,1)} & \underline{(0,2)} & \underline{(1,0)} & \underline{(1,1)} & \underline{(1,2)} \\
(0,0) & (0,0) & (0,1)  & (0,2) & (1,0) & (1,1) & (1,2)  \\
(0,1) & (0,1) & (0,2) & (0,0) & (1,1)  & (1,2) & (1,0)\\
...  &  &  & ... & ...\\
... &  &  & ... & ...
\end{array}\right)
$$
