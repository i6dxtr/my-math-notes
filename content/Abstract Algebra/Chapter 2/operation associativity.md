#ch2

> [!definition]
> An operation $*$ on $S$ is **associative** means:
> $$\forall x,y,z\in S\text{   }(x*y)*z=x*(y*z)$$
> - $(x*y)$ and $(y*z)$ computed first

> [!example]
> **On $\mathbb{R}$, which of $+, -, \cdot, /$ are associative?**
> - $+$ is: $(x+y)+z=x+(y+z)=x+y+z$
> - $\cdot$ is: $x(yz)=(xy)z=xyz$
> - $-, /$ are *not*, obviously.
>
>
> **Are there operations that are associative but not commutative?**
>
> *Solution*: Yes:
> - Concatenation, denoted $*$ :
> 	- $\text{tree}*\text{nut}=\text{treenut}$, not commutative
> 	- $\text{nut}*\text{tree}=nuttree$, not commutative
> 	- $(\text{tree}*\text{nut})*\text{squirrel}=\text{treenutsquirrel}$
> 	- $\text{tree}*(\text{nut}*\text{squirrel})=treenutsquirrel$
> 	- ... more generally, $(x*y)*z=x*(y*z)$

- Matrix multiplication on $M_{2}(\mathbb{R})$ (or $M_{3}(\mathbb{R})$, etc.), we saw was not commutative.
- However, it *is* associative: $(AB)C=A(BC)$
- Note: $\cap,\text{ }\cup$ are associative as well as commutative.