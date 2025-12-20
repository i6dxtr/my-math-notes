#theorem
> [!theorem]
> ### Lemma 3.1.9.
> Every component of the symmetric difference of two (finite) matchings is a path or an even cycle. More formally, every component of $(V(G),\;M\triangle M')$ is a path or an even cycle.
> [!proof]
> Let $M$ and $M'$ be matchings and let $F=M\triangle M'$. Note that every vertex is incident with at most one edge of each of $M$ and $M'$, so every vertex has degree at most $2$ in $F$. Hence every component of $F$ is a path or a cycle. Further, no cycle in $F$ can have odd length: an odd cycle would force two incident edges to both belong to $M$ or both belong to $M'$, contradicting the matching property.
### Relations
- Base concept: [[matching|matching]].
- Alternating/augmenting path definitions: [[M-alternating path, M-augmenting path|M-alternating path, M-augmenting path]].
- Used in the proof of the augmenting-path characterization of maximum matchings and in proofs such as Cantor–Schroeder–Bernstein via matching constructions ([[theorem - Cantor-Schroeder-Bernstein|Cantor–Schroeder–Bernstein]]).
- Useful when analyzing differences between two matchings (e.g., to find augmenting paths or improve a matching).
