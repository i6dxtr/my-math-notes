#example 
> [!example]
> ### Exercise 1 — Degree pigeonhole
> Prove that in every finite simple graph on $\ge 2$ vertices there are two vertices with the same degree.> [!proof]
> Let $G=(V,E)$ have $n\ge 2$ vertices. The possible degrees of a vertex are the integers
> $$0,1,\dots,n-1.$$
> If some vertex has degree $0$ then no vertex can have degree $n-1$, so the set of attainable degree values has size at most $n-1$. In general there are at most $n-1$ distinct degree values available for the $n$ vertices of $G$, so by the pigeonhole principle two vertices share the same degree.
### Relations
- Related foundational material: [[content/foundational/degree.md]], [[content/foundational/order, size.md]].
- Useful parity/degree results: [[content/foundational/handshake lemma.md]].
- See also: [[content/theorems, lemma/lemma - minimum degree 2 implies cycle.md]] for minimum-degree arguments in other contexts.
