#ch12
## Homomorphism
- there may be a function that transforms one of the groups into the other. while *not* being bijective (unlike isomorphisms)
	- ex. $\mathbb{Z}_{6}\rightarrow \mathbb{Z_{3}}$ $$\begin{pmatrix} 0&1&2&3&4&5 \\ 0&1&2&0&1 &2\end{pmatrix}\ $$ ... which can be verified w/ tables: ![[Pasted image 20241016135719.png]]

> [!definition]
> If $G$ and $H$ are groups, a **homomorphism** from $G$ to $H$ is a function $f:G\rightarrow H$ such that for any two elements $a,b \in G$, $$f(ab)=f(a)f(b)$$ If there exists a homomorphism from $G$ *unto* $H$, we say that $H$ is a **homomorphic image** of $G$.

> [!remark]
> If $G$ and $H$ are any groups, and there is a function $f$ which transforms $G$ into $H$, we say that $H$ is a *homomorphic image* of $G$.

- $f$ the *homomorphism* from $G\rightarrow\ H$
- thus, has the following property (implication): $$f(a)=a' \wedge f(b)=b'\longrightarrow f(ab)=a'b'$$
- 