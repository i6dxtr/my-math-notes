#ch2

> [!definition]
> If $*$ is an operation on $S$ with identity element $e$, then $x, y\in S$ are *inverses* such that $x*y=e$ and $y*x=e$.

- For operation $+$ on $\mathbb{R}$, $-x$ is the inverse of $x$
	- meaning, $(-x)+x=0$ and $x+(-x)=0$.
- For operation $\cdot$ on $\mathbb{R}$, $\frac{1}{x}$ is the inverse of $x$ (if $x\neq 0$)
	- meaning, $\frac{1}{x}\cdot x=1$ and $x\cdot \frac{1}{x}=1$ (identity element)

> [!remark]
> If $x,y$ are inverses of each other, we say:
> - $x$ is the inverse of $y$ $(x=y^{-1})$ 
> - $y$ is the inverse of $x$ ($y=x^{-1}$)
>
> *Exception*:
> If $*$ is $+$, then the inverse of $x$ is written $-x$, not $x^{-1}$
> - note that $-x$ is *additive notation* for inverses

> [!corollary]
> For an associative operation on $*$ on $S$ with an identity element $e$, the inverses are *unique*, when they exist.

> [!proof]
> Let $x\in S$. Suppose that $y_{1}, y_{2}$ are both inverses of $x$. 
> - WTS: $y_{1}=y_{2}$
> $$
> > \begin{align}
> (y_{1}*x)*y_{2}&=e*y_{2} \\
> &=y_{2}
> \end{align}
>
> $$
> ... because $y_{1}$ is an inverse of $x$. On the other hand,
> $$
> > \begin{align}
> y_{1}*(x*y_{2})=y_{1}*e \\
> y_{1}
> \end{align}
>
> $$
> ... because $y_{2}$ is an inverse of $x$.
> So by associativity, $y_{2}=y_{1}$ holds true.

$^{}$
Inverses might not exist:

> [!example]
> No inverse exists for $M_{2}(\mathbb{R})$ on $\cdot$
> - $\begin{pmatrix} 0 &0 \\ 0&0 \end{pmatrix}$ has no inverse
> - $\begin{pmatrix}1 & 0 \\ 0 & 0 \end{pmatrix}$ has no inverse:
> $$
> \begin{pmatrix}
>  1 & 0 \\
> 0 & 0 
> \end{pmatrix}\cdot
> \begin{pmatrix}
>  a & b \\
> c & d 
> \end{pmatrix}=
> \begin{pmatrix}
>  a & b \\
> 0 & 0 
> \end{pmatrix}\neq 
> \begin{pmatrix}
>  1 & 0 \\
> 0 & 1 
> \end{pmatrix}
> $$
> - $\begin{pmatrix} a & b \\c & d \end{pmatrix}$ has an inverse if and only if $ad-bc\neq 0$ (determinant)

