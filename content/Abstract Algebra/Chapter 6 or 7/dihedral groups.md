#ch7 

> [!definition]
> The dihedral group $D_{n}\ (n\geq 3)$ is the subgroup of $S_{n}$ (the [[symmetric group]]) consisting of symmetries of a regular $n-$gon with vertices $1,2,...,n$

- $D_{n}$ has order $2n$, consisting of $n$ rotations and $n$ symmetries
- we note their composition groups:
	- rotation $\circ$ rotation is a rotation
		- *commutative* since addition of angles produces a third rotation
	- rotation $\circ$ reflection is a reflection
		- *not commutative*, unless angle = $180^\circ$, which can only exist where $n$ is even
	- reflection $\circ$ rotation is a reflection
		- *not commutative*, see above
	- reflection $\circ$ reflection is a rotation
		- *pf.* apply arithmetic def. with $\sigma_{j}(\sigma_{k}(i))=...=p_{j-k}(i)$
		-  *not commutative*, unless the axis of reflection are the same
	- $(\text{rot }x^\circ)^{-1}$ is a rotation $x^\circ$ clockwise
		- $360^\circ-x^\circ$
	- the inverse of a reflection is the reflection itself
	- $\left\{ p\in D_{n}\ |\ p\text{ is a rotation} \right\}$ is a subgroup
		- $\left\{ \sigma\in D_{n}\ |\ \sigma \text{ is a reflection}\right\}$ is *not*
			- not closed, no identity

### Arithmetic Definition
Define $S_{n}$ as a [[Groups|group]] of [[permutations]] of $\left\{ 0,1,...,n-1 \right\}$. 
- The *rotations* in $D_{n}$ are $p_0, ..., p_{n-1}$ where: $$p_{k}(i)=i+k\text{ mod }n,\ \ \ \ \ k\leq n-1$$... and the angle of rotation is given by $\frac{k}{n}\cdot 360^\circ$
- The *reflections* in $D_{n}$ are $\sigma_{0}, ..., \sigma_{n-1}$ where: $$p_{k}(i)=-i+k\text{ mod }n,\ \ \ k\leq n-1$$

link [[symmetric group]]