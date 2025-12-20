#example 
> [!example]
> ### Exercise 3 — Closed odd walks contain an odd cycle
> Let $G$ be a (multi)graph. Prove that every closed odd walk in $G$ contains an odd cycle.> [!proof]
> Let $W$ be a closed odd $v_0v_0$‑walk in $G$. Among all closed odd subwalks of $W$ choose one of minimal length and call it $W'$. We claim $W'$ is an odd cycle.
> 
> If $W'$ has a repeated vertex other than the start/end vertex, say the same vertex appears at positions $i<j$ along $W'$, then $W'$ decomposes into two closed subwalks $W_1$ and $W_2$ whose lengths sum to $|W'|$. Since $|W'|$ is odd, exactly one of $|W_1|,|W_2|$ is odd; that odd subwalk is strictly shorter than $W'$, contradicting the minimality of $W'$. Hence $W'$ has no repeated internal vertices and is therefore a cycle. As $W'$ is odd, it is an odd cycle contained in $W$, proving the claim.
### Relations
- Uses walk → path reduction and minimality arguments: [[lemma - walk contains path]], [[walk, trail, path, cycle]].
- Formal version appears as: [[lemma - odd walk contains odd cycle]].
- Connected concepts: [[theorem - bipartite characterization]] (odd cycles obstruct bipartiteness), [[graph]].
