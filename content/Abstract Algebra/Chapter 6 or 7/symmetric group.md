#ch7 

> [!definition]
> For any set $A$, the [[Groups|group]] of all the [[permutations]] of $A$ is called the **symmetric group** on $A$, and is represented with the symbol $S_{A}$.

- meanwhile, a *dihedral group* $D_{n}$ consists of all *geometric* symmetries, a subset of $S_{n}$ containing all permutations that preserve the shape of the represented geometric figure with $n$ vertices.

> [!example] Example: Permutations of $\left\{ 1,2,3 \right\}$
> $$
> > \begin{align}
> \epsilon=
> \begin{pmatrix}
> 1 & 2 & 3 \\
> 1 & 2 & 3
> \end{pmatrix}&&\alpha=
> \begin{pmatrix}
> 1 & 2 & 3 \\
> 1 & 3 & 2
> \end{pmatrix} &&\beta=
> \begin{pmatrix}
> 1 & 2 & 3 \\
> 3 & 1 & 2
> \end{pmatrix} \\
> \gamma=
> \begin{pmatrix}
> 1 & 2 & 3 \\
> 2 & 1 & 3
> \end{pmatrix}&&\delta=
> \begin{pmatrix}
> 1 & 2 & 3 \\
> 2 & 3 & 1
> \end{pmatrix}&&\kappa=
> \begin{pmatrix}
> 1 & 2 & 3 \\
> 3 & 2 & 1
> \end{pmatrix}
> \end{align}
>
> $$
> - $[\alpha\circ \beta](1)=\alpha(\beta(1))=a(3)=2$
> - $[\alpha\circ\beta](2)=\alpha(\beta(2))=\alpha(1)=1$
> - $[a\circ \beta](3)=\alpha(\beta(3))=\alpha(2)=3$
> - thus, $\alpha\circ \beta=\begin{pmatrix} 1&2&3\\2&1&3 \end{pmatrix}=\gamma$

> [!example] Group Table of $S_{3}$
> A [[group table]] can be formed for permutation groups under the composition operation:
> $$
> \left(\begin{array}{c|cccccc}
>   \underline\circ & \underline\epsilon & \underline\alpha & \underline\beta & \underline\gamma & \underline\delta & \underline\kappa \\
> \underline\epsilon & \epsilon & \alpha & \beta & \gamma & \delta & \kappa \\
> \underline\alpha & \alpha & \epsilon & \gamma & \beta & \kappa & \delta \\
> \underline\beta & \beta & \kappa & \delta & \alpha & \epsilon & \gamma \\
> \underline\gamma & \gamma & \delta & \kappa & \epsilon & \alpha & \beta \\
> \underline\delta & \delta & \gamma & \epsilon & \kappa & \beta & \alpha \\
> \underline\kappa &\kappa & \beta & \alpha & \delta & \gamma & \epsilon
> \end{array}\right)
> $$

- geometrically, symmetry of a shape involves moving the shape such that it coincides with it's former position
	- e.g. rotational operation on a square clockwise through angles $90^{\circ}, 180^{\circ}, 270^{\circ}$

> [!example]
> ![[Pasted image 20240925191759.png]]
> - vertices numbered in corners correspond to entries
> - following matrix:
> 	$$
> 	R_{1}=
> 	\begin{pmatrix}
> 	1 & 2 & 3 & 4 \\
> 	2 & 3 & 4 & 1
> 	\end{pmatrix}
> 	$$
> 	... corresponds to clockwise rotation of $90^{\circ}$ or $\frac{\pi}{2}$
> - $R_{2}=\begin{pmatrix} 1&2&3&4\\3&4&1&2 \end{pmatrix}$ yields $180^{\circ}$ rotation
> - $R_{3}=\begin{pmatrix} 1&2&3&4\\4&1&2&3 \end{pmatrix}$ yields $270^{\circ}$ rotation
>
> ![[Pasted image 20240925191745.png]]
>
> - rotations about $A,B,C,D$ are flips about the axes

- the operation on symmetric groups is [[composition]]
	- $R_{i}\circ R_{j}$ is the result of performing $R_{j}$ and then $R_{i}$
		- $R_{1}\circ R_{4}\longrightarrow$ flip on $A$, rotation $\text{rad}\left( \frac{\pi}{2} \right)$
- the 8 symmetries of a square form a group under $\circ$, called the *group of symmetries of the square*
	- $\forall n\geq 3$, regular polygon with $n$ sides has a group of symmetries, defined $D_{n}$
		- called the **dihedral groups**
		- e.g. group of square $\rightarrow D_{4}$, group of pentagon $\rightarrow D_{5}$
- every plane figure exhibiting regularities also exhibit symmetries

## Lecture
==Recall==: The dihedral group $D_{n}$ ($n\geq 3$) is the subgroup of $S_{n}$ consisting of symmetries of a regular $n-$gon with vertices $1,2,...,n$\
for $n=5$, here are a couple elements:
- rotation by $144^{\circ}$: $\begin{pmatrix} 1&2&3&4&5\\3&4&5&1&2 \end{pmatrix}$
- ![[Drawing 2024-09-23 14.58.03.excalidraw]]
- reflection: $\begin{pmatrix} 1&2&3&4&5\\2&1&5&4&3 \end{pmatrix}$
- [[Drawing 2024-09-23 15.04.11.excalidraw]]

in $D_{n}$:
- rotation $\circ$ rotation is a rotation
	- Do any two rotations commute?
		- ==yes==, b/c the angles of rotation are added to each other to produce a third rotation. additionally, the addition operation is commutative
- rotation $\circ$ reflection is a reflection
	- Do rotations always commute with reflections?
		- ==no==, unless the angle of rotation is $180^{\circ}$
			- which only exists in $D_{n}$ when $n$ is even
- reflection $\circ$ rotation is a reflection
	- 
- reflection $\circ$ reflection is a rotation
	- ==pf.== WTS for any two reflections $\sigma_{j}, \sigma_{k}$:
		$$
		\begin{align}
		\sigma_{j}(\sigma_{k}(i))&=\sigma_{j}(-i+k\text{ mod }n)  \\
		&=-(-i+k\text{ mod }n)+j\text{ mod }n \\
		&=-(-i+k)+j\text{ mod }n \\
		&=i+(j-k)\text{ mod }n \\
		&=p_{j-k}(i) & ...\text{ so }\sigma_{j}\circ\sigma_{k}=p_{j-k}\text{ mod }n.
		\end{align}
		$$
	- Do any two reflections commute?
		- ==no==, unless the axis of reflection are perpendicular ( the same )
continuing...
- The inverse of a rotation *by $x^{\circ}$* is a rotation *by $x^{\circ}$ clockwise*.
	- $360-x^{\circ}$
- The inverse of a reflection is a reflection ( itself )
- $\left\{ p\in D_{n}\ |\ p\text{ is a rotation} \right\}$ is a subgroup
	- ... but $\left\{ \sigma \in D_{n}\ |\ \sigma \text{ is a reflection} \right\}$ is *not*.
		- not closed
		- no identity element

alternative arithmetic definition of $D_{n}$
- define $S_{n}$ are permutations of $\left\{ 0,1,...,n-1 \right\}$ ( not up to $n$ )
	The rotations in $D_{n}$ are $p_{0},...,p_{n-1}$ where:
	$$
	\begin{align}
	p_{k}(i)=i+k\text{ mod }n &&  \text{e.g.}n=5,\ k=2 \\
	&& \text{rot. by }\frac{k}{n}\cdot360^{\circ}
	\end{align}
	$$
		- see image
	The reflections in $D_{n}$ are $\sigma_{0},...,\sigma_{n-1}$ where:
	$$
	\begin{align}
	p_{k}(i)&=-i+k\text{ mod }n && \text{e.g. }n=5,\ k=1 \\
	\end{align}
	$$
		- see image

link: [[permutations]] [[Groups]]