#ch4
- [[Groups]] in general have properties that are consistent with what we have seen with [[Binary Operations|operational]] properties we've seen so far
	- e.g in general we can write $a*b$ as $ab$ even if $*$ is not literally multiplication (multiplicative notation)
- these properties include:
	- [[cancellation law]]
	- [[law of exponents]]
	- [[inverse uniqueness]]
	- [[inverse product theorem]]
	- [[direct products]] (cartesian products)

##### Examples

> [!example] Example: Solving Equations in Groups
> $a \times b^{-1}c=d$, solve for $x$:
> $$
> > \begin{align}
> a \times b^{-1}c&=d \\
> a^{-1}a \times b^{-1}c&=a^{-1}d \\
> xb^{-1}c&=a^{-1}d \\
> xb^{-1}cc^{-1}&=a^{-1}dc^{-1} \\
> xb^{-1}&=a^{-1}dc^{-1} \\
> xb^{-1}b&=a^{-1}dc^{-1}b \\
> x&=a^{-1}dc^{-1}b.
> \end{align}
>
> $$
> *Check*: $a(a^{-1}dc^{-1}b)b^{-1}c=dc^{-1}c=d$

note: in a group, $ax=b$ and $xa=b$ have unique solutions
- $ax=b\longleftrightarrow x=a^{-1}b$
- $xa=b \longleftrightarrow x=ba^{-1}$
- this means in the operation table for a group, each row & column contains each group element exactly once

> [!example] Example: of $\mathbb{Z}_{4}$:
> $$
> > \begin{align}
> \left(\begin{array}{c|cccc}
> \underline{+_{4}} & \underline{0} & \underline{1} & \underline{2} & \underline{3} \\
> 0 & 0 & 1 & 2 & 3 \\
> 1 & 1 & 2 & 3 & 0 \\
> 2 & 2 & 3 & 0 & 1  \\
> 3 & 3 & 0 & 1 & 2
> \end{array}\right)
> \end{align}
>
> $$
> - row 3: 1 appears exactly once, below 3, since 3 is the unique solution $x$ to $2+_{4}x=1$

