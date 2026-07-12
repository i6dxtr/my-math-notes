#ch6 
- Suppose $f$ is a [[Functions|function]] from $A$ to $B$, and $g$ is a function from $B$ to $C$:
	- Apply $f$ to an element in $A$ and get an element $y\in B$
	- Apply $g$ to the element $y$ and get an element $z\in C$
	- Performing this in succession results in a function defined as follows:

> [!definition]
> Let $f : A\rightarrow B$ and $g : B\rightarrow C$ be functions. The **composite function** denoted by $g\circ f$ is a function from $A$ to $C$ defined as follows: $$[g \circ f](x)=g(f(x))\ \ \ \ \forall x\in  A$$
> ![[Pasted image 20240924142639.png]]

- the composition of any two [[bijective]] functions is also a bijective function
	- following this, we can also prove the composition of functions is associative
	- notably is *not* commutative unless it contains less than 3 elements

> [!proof] $f\circ(g\circ h)=(f\circ g)\circ h$
> Suppose $f:A\rightarrow A,g:A\rightarrow A$, and $h:A\rightarrow A$. We show that: $$\forall x\in A\ \ \left\{ f\circ[g\circ h] \right\}(x)=\left\{ [f\circ g]\circ h \right\}(x)$$ Now, repeatedly apply the definition of composition:
> $$
> > \begin{align}
> \left\{ f\circ[g\circ h] \right\} (x)&=f([g\circ h](x))=f(g(h(x))) \\
> &=[f\circ g](h(x))=\left\{ [f\circ g]\circ h \right\}(x).
> \end{align}
>
> $$

> [!proof] Proof of composition non-commutativity
> 1. Let $f,g\in \mathbb{R}\rightarrow \mathbb{R}$
> 2. Define $f(x)=2x$
> 3. Define $g(x)=x+1$
> 5. Observe $(f\circ g)(x)$
> 	2. $=f\left( g\left( x \right) \right)$
> 	3. $=2(x+1)$
> 	4. $=2x+2$
> 6. Observe $(g\circ f)(x)$
> 	1. $=g\left( f\left( x \right) \right)$
> 	2. $=g\left( 2x \right)$
> 	3. $=2x+1$

