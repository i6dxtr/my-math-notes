#theorem
> [!theorem]
> ### Theorem — Cantor–Schroeder–Bernstein
> Let $A,B$ be sets. If there exists an injective function $f:A\to B$ and an injective function $g:B\to A$, then there exists a bijection $h:A\to B$.
> [!proof]
> Interpret $f$ and $g$ as matchings between $A$ and $B$: view the bipartite graph with parts $A$ and $B$, and let $M_A$ be the matching corresponding to $f$ (which saturates $A$) and $M_B$ be the matching corresponding to $g$ (which saturates $B$). Consider the symmetric difference $F=M_A\triangle M_B$. By Lemma 3.1.9 every component of $F$ is either an isolated vertex, a finite even cycle, a one-way infinite path, or a two-way infinite path.
> 
> On each component choose every other edge to form a matching that saturates all vertices that were saturated by either $M_A$ or $M_B$; for one-way infinite paths start at the endpoint in the part saturated by $M_A$ (or choose the consistent parity) and select every other edge from there. The chosen edges define a perfect matching between $A$ and $B$ in the bipartite graph, which corresponds to the desired bijection $h:A\to B$.
### Relations
- Uses structural fact about symmetric differences of matchings: [[content/theorems, lemma/lemma - symmetric difference of matchings (Lemma 3.1.9).md|Lemma 3.1.9]].
- Argument interprets injections as matchings; see [[content/foundational/matching.md|matching]].
- Conceptually related to augmenting‑path techniques and matching theory.
