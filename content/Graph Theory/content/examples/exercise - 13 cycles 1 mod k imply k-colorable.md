#example 
> [!example]
> ### Exercise 13 — No cycles of length $1\pmod{k}$ implies $\le k$-colorable
> Let $k\ge 2$ be an integer and let $G$ be a connected graph. If $G$ has no cycles of length $1\text{ mod }k$, then $G$ has a partition of $V(G)$ into at most $k$ independent sets (equivalently, $\chi(G)\le k$).
> [!remark]
> Hints (from lecture):
> - This generalizes the $k=2$ case: if $G$ has no odd cycles, then $G$ is bipartite (i.e., 2-colorable).
> - Choose a Depth‑First Search Tree (DFST) of $G$ rooted at some $x$ and consider “levels” modulo $k$ along $x$‑branches. Use the DFST same‑branch property to rule out conflicts that would otherwise create a cycle of length $1\pmod{k}$.
### Source
- lecture/438Notes_f25.pdf — Exercise 13 (Sept 29, 2025)
- Notes by date/9-28-25.md

### Relations
- DFST and same‑branch property: [[content/graph structure/definition - depth-first search tree (DFST).md]], [[content/theorems, lemma/lemma - DFST edge endpoints on same branch (Lemma 4.1.22).md]]
- Rooted tree and branches: [[content/graph structure/definition - rooted tree and branch.md]]
- Chromatic number and $k$‑partite: [[content/foundational/chromatic number.md]]
