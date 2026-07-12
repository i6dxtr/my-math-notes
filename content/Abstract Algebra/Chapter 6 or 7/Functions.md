#ch6

> [!definition]
> If $A$ and $B$ are sets, then a function from $A$ to $B$ ( $f\ :\ A\rightarrow B$ ) is a rule for which every element $x$ in $A$ assigns a unique element $y$ in $B$. This is noted $y=f(x)$ and we call $y$ the *image* of $x$ under $f$.

- $A$ being domain, $B$ being range ( consisting of all images of elements $\in A$ )
![[Pasted image 20240924142146.png]]

- $f$ can be represented as a matrix: $f=\begin{pmatrix} a&b&c\\x&x&y \end{pmatrix}$
	- $a$ maps to $x$, $b$ to $x$, etc.
	- row 1 is $A$, row 2 is $B$
	- useful when $A$ is finite

- functions can be [[injective]] or [[surjective]]; if both, it is considered [[bijective]]
- combining two functions results in the [[composition]] function
- functions may have their own [[function inverses|inverse]]
	- if it does, it must be bijective

> [!corollary]
> If $f:A\rightarrow B$ and $g:B\rightarrow C$ are functions, then the following hold:
> - If $f$ and $g$ are injective, then $g\circ f$ is injective.
> - If $f$ and $g$ are surjective, then $g\circ f$ is surjective.
> - IF $f$ and $g$ are bijective, then $g\circ f$ is bijective.

