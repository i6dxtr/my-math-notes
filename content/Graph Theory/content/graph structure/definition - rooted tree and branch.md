#definition 
> [!definition]
> ### Definition — Rooted tree and $x$-branch
> Let $T$ be a tree and let $x\in V(T)$. We say that $T$ is rooted at $x$ (a rooted tree).
> Given a tree rooted at $x$, an $x$-branch (or simply branch when the root is clear) is a path in $T$ from $x$ to a leaf $z$ with $z\ne x$.
> [!remark]
> - Each leaf $z$ determines a unique $x$-branch; an internal vertex may lie on multiple $x$-branches. For every vertex $v$, the $x$-$v$ path in $T$ is unique.
> - DFS naturally constructs $x$-branches by exploring as far as possible before backtracking.
### Source
- lecture/438Notes_f25.pdf — Rooted tree/branch (Sept 29, 2025)
- Notes by date/9-28-25.md (branch notion; corrected incomplete sentence)

### Relations
- DFS process and output: [[content/graph structure/algorithm - depth-first search (DFS).md]], [[content/graph structure/definition - depth-first search tree (DFST).md]]
- Same-branch property (DFS): [[content/theorems, lemma/lemma - DFST edge endpoints on same branch (Lemma 4.1.22).md]]
- Trees and spanning trees: [[content/foundational/tree.md]]
