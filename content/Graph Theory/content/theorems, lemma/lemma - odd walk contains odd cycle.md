#theorem

> [!lemma]
> ### Lemma 1.2.15
> Every closed odd walk contains an odd cycle.
> [!proof]
> Let $W$ be a closed odd walk in $G$. Among all closed odd subwalks of $W$, choose one of minimal length and call it $W'$. We show $W'$ is an odd cycle.
> 
> If $W'$ repeats a vertex other than the starting/ending vertex, say $u_i = u_j$ with $0 \le i < j \le k$ in the vertex sequence of $W'$, then $W'$ decomposes into two closed subwalks $W_1$ and $W_2$ whose lengths sum to the length of $W'$. Since $|W'|$ is odd, at least one of $W_1$ or $W_2$ is odd, contradicting minimality of $W'$. Therefore $W'$ has no repeated internal vertices and is a simple closed walk, i.e., an odd cycle.
### Relations
- Used in the proof of the bipartite characterization: [[content/theorems, lemma/theorem - bipartite characterization.md|theorem - bipartite characterization]].
- Builds on path/walk notions: [[content/graph structure/walk, trail, path, cycle.md|walk, trail, path, cycle]] and [[content/theorems, lemma/lemma - walk contains path.md|lemma - walk contains path]].
- Important for parity/odd-cycle structural results and coloring arguments (see [[content/foundational/chromatic number.md|chromatic number]]).
- Also referenced in subsequent results about cycles and decomposition (see [[content/theorems, lemma/proposition - decomposition into cycles iff even degree (Proposition 1.2.27).md|proposition - decomposition into cycles iff even degree]]), and in matching parity lemmas used in Tutte's theorem ([[content/theorems, lemma/lemma - parity lemma (Tutte).md|parity lemma (Tutte)]], [[content/theorems, lemma/theorem - Tutte's theorem.md|Tutte's theorem]]).
