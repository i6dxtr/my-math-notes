#ch4

> [!theorem]
> For all $m,n\in \mathbb{Z}$ and $a\in G$ (any group), 
> 1. $a^{m}\cdot a^{n}=a^{m+n}$
> 2. $(a^{m})^{n}=a^{m\cdot n}$

> [!remark]
> The following are true:
> - $(a^{-1}ba)^{n}=a^{-1}b^{n}a$
> - $(ab)^{n}\neq a^{n}b^{n}$, in general
> 	- $(ab)^{2}\neq a^{2}b^{2}$ unless $ab=ba$

> [!proof] Proof. (chapter 4)
> 1. Let $m,n \in \mathbb{Z}^+$. By induction:
> 	1. Basis step: $n=0$
> $$
> > \begin{align}
> a^{m}a^{0}&= a^{m}e \\
> &=a^{m} \\
> &=a^{m+0} \\
> a^{m+0}&=a^{m} \\
> \end{align}
>
> $$
> 2. Inductive step: 
> 	Suppose $a^{m}a^{n}=a^{m+n}$. 
> 	WTS $a^{m}a^{n+1}=a^{m+(n+1)}$:
> $$
> > \begin{align}
> a^{m}a^{n+1}&= a^{m}a^{n}a \\&=a^{m+n}a \\ &=a^{(m+n)+1}\\ &=a^{m+(n+1)}
> \end{align}
>
> $$

> [!proof] Proof. (chapter 10)
> - $a^{m}a^{n}=aa\cdots a$ ($m$ times) $\cdot aa\cdots a$ ($n$ times) $=a^{m+n}$
> - $(a^{m})^{n}=a^{m}a^{m}\cdots a^{m}$ ($n$ times) $=aa\cdots a$ ($mn$ times)$=a^{m}n$
> - $a^{-n}=a^{-1}\cdots a^{-1}=(a^{-1})^{n}$, 
> - so $(a^{n})^{-1}=(aa\cdots a)^{-1}=a^{-1}a^{-1}\cdots a^{-1}=a^{-n}$
> - there also exists cases where $m,n$ are $0$ or negative

link [[properties of groups]]