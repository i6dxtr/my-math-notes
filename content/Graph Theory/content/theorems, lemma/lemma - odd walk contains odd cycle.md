#theorem

> [!lemma]
> ### Lemma 1.2.15
> Every closed odd walk contains an odd cycle.

> [!proof]
> Let $W$ be a closed odd walk in $G$. Among all closed odd subwalks of $W$, choose one of minimal length and call it $W'$. We show $W'$ is an odd cycle.
> 
> If $W'$ repeats a vertex other than the starting/ending vertex, say $u_i = u_j$ with $0 \le i < j \le k$ in the vertex sequence of $W'$, then $W'$ decomposes into two closed subwalks $W_1$ and $W_2$ whose lengths sum to the length of $W'$. Since $|W'|$ is odd, at least one of $W_1$ or $W_2$ is odd, contradicting minimality of $W'$. Therefore $W'$ has no repeated internal vertices and is a simple closed walk, i.e., an odd cycle.
### Relations
- Used in the proof of the bipartite characterization: [[theorem - bipartite characterization|theorem - bipartite characterization]].
- Builds on path/walk notions: [[walk, trail, path, cycle|walk, trail, path, cycle]] and [[lemma - walk contains path|lemma - walk contains path]].
- Important for parity/odd-cycle structural results and coloring arguments (see [[chromatic number|chromatic number]]).
- Also referenced in subsequent results about cycles and decomposition (see [[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)|proposition - decomposition into cycles iff even degree]]), and in matching parity lemmas used in Tutte's theorem ([[lemma - parity lemma (Tutte)|parity lemma (Tutte)]], [[theorem - Tutte's theorem|Tutte's theorem]]).
