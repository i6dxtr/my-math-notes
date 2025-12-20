> [!example]
> ### Exercise 14a.
> 1. Prove that if $M$ and $M'$ are perfect matchings in $G$, then every component of $G'=(V(G),\;M\triangle M')$ is an isolated vertex or an even cycle.
> 
> 2. Prove that every forest has at most one perfect matching.
> [!proof]
> 1. Let $M$ and $M'$ be perfect matchings and set $F=M\triangle M'$. By Lemma 3.1.9 every component of $F$ is a path or an even cycle. Because $M$ and $M'$ are perfect they saturate every vertex of $G$, so no component of $F$ can be a path with unmatched endpoints (an augmenting path) — every vertex is incident with exactly one edge from each matching on the component. Hence the only possible components are isolated vertices (where the two matchings agree by using no edge) or even cycles (where edges alternate between $M$ and $M'$).![[Pasted image 20251019125954.png]]
> 
> 2. Let $F$ be a forest and suppose, for contradiction, that $F$ has two distinct perfect matchings $M$ and $M'$. Consider $M\triangle M'$. By part 1 every component of $M\triangle M'$ is an isolated vertex or an even cycle. But a forest contains no cycles, so every component must be an isolated vertex. Therefore $M\triangle M'=\varnothing$, so $M=M'$, contradicting that they were distinct. Thus every forest has at most one perfect matching.
### Relations
- Uses the symmetric-difference structural lemma: [[content/theorems, lemma/lemma - symmetric difference of matchings (Lemma 3.1.9).md|Lemma 3.1.9]].
- Builds on matching definitions: [[content/foundational/matching.md|matching]] and maximal/maximum distinctions ([[content/foundational/maximal matching, maximum matching.md|maximal vs maximum matching]]).
- Related files: [[content/theorems, lemma/theorem - augmenting path characterization.md|augmenting-path characterization]] and [[content/theorems, lemma/theorem - Cantor-Schroeder-Bernstein.md|Cantor–Schroeder–Bernstein]] (matching constructions).
