#ch2
- a [[Groups|group]] whose operation is [[operation commutativity|commutative]] $(x*y=y*x)$ (after Mels Abel)
	- ex. $(\mathbb{Z}, +)$, $(\mathbb{Z}_{n}+_{n})$ are abelian, while $(GL_{n}(\mathbb{R}), \cdot)$ is not for $n\geq 2$
- Commutativity of the abelian groups also means the associated [[group table]] is symmetric across the main diagonal.

> [!example]
> **An example of a non-abelian group**:
> $SL_{n}(\mathbb{R})$= the set of all $n \times n$ matrices whose determinant is $1$.
> Proof that this is a group under matrix multiplication:
> 1. Let $A,b\in SL_{n}(\mathbb{R})$. WTS $AB\in SL_{n}(\mathbb{R})$
> 	   $\text{det}(AB)=\text{det}(A)\text{det}(B)=1\cdot1=1$
> 2. Matrix multiplication is associative in general
> 3. There is an identity element $I_{n}$
> 	   $I_{n}\in SL_{n}(\mathbb{R})$ since $\text{det}(I_{n})=1$
> 4. Let $A\in SL_{n}(\mathbb{R})$. WTS $\underline{A}^{-1}\in SL_{n}(\mathbb{R})$ (ud: exists since $\text{det}(A)\neq0$)
> 	   $\text{det}(A^{-1})=\frac{1}{\text{det}(A)}=\frac{1}{1}=1$

