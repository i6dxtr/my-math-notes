#definition 
> [!definition]
> ### Definition — Combinatorial notation (bracket sets, k-subsets, power set, binomial coefficients)
> We record common combinatorial notation used throughout these notes.
> 
> - For a non-negative integer $k$, write $[k]=\{1,2,\dots,k\}$.
> - For a set $V$ and integer $k\ge 0$ write
> $$
> \binom{V}{k}=\{S\subseteq V : |S|=k\},
> $$
> the set of all $k$-element subsets of $V$. (When $V=[n]$ this is often written $\binom{[n]}{k}$.)
> - The power set of $V$, the collection of all subsets of $V$, is denoted $2^V$.
> - For integers $n\ge 0$ and $0\le r\le n$ the binomial coefficient
> $$
> \binom{n}{r}=\frac{n!}{r!(n-r)!}
> $$
> counts the number of $r$-element subsets of an $n$-element set. In particular
> $$
> \binom{n}{2}=\frac{n(n-1)}{2}.
> $$

> [!remark]
> Use this notation consistently for statements about edge counts, choices of vertex subsets, and combinatorial arguments (e.g. counting edges in complete graphs or selecting endpoint pairs). All math uses MathJax delimiters: $...$ for inline and $$...$$ for display math.

### Relations
- Order and size: [[content/foundational/order, size.md]] (uses $\binom{n}{2}$ when counting edges of complete graphs).
- Graph definition and complete graphs: [[content/foundational/graph.md]], [[content/foundational/clique.md]].
- Exercises and combinatorial counting: [[content/examples/exercise - 1 degree pigeonhole.md]], [[content/examples/exercise - 8 hamiltonicity bounds.md]].
