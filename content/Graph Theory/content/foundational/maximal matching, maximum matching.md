#definition 
> [!definition]
> ### Definition — Maximal matching vs Maximum matching
> Let $G$ be a graph and let $\mathcal{M}$ denote the family of all matchings in $G$ (partially ordered by $\subseteq$).
> 
> ---
> A maximal matching is a matching $M\in\mathcal{M}$ such that there is no matching $M'\in\mathcal{M}$ with $M\subsetneq M'$.
> 
> ---
> A maximum matching is a matching $M\in\mathcal{M}$ of maximum cardinality; that is, for all $M'\in\mathcal{M}$ we have $|M'|\le |M|$.

> [!remark]
> - Every maximum matching is maximal, but not every maximal matching is maximum.
> - “Maximal” refers to inclusion; “maximum” refers to size.

### Source
- lecture/438Notes_f25.pdf — Definition 3.1.4 (Maximal vs Maximum matching)
- Notes by date/9-28-25.md

### Relations
- Base matching notions: [[content/foundational/matching.md]]
- Alternating and augmenting paths (tool for finding larger matchings): [[content/foundational/M-alternating path, M-augmenting path.md]]
- Independent sets interplay: [[content/foundational/independent set.md]]
