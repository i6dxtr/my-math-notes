#example 
> [!example]
> ### Exercise 7 — Maximal vs maximum paths
> Let $G$ be a connected graph.
> 1. Prove that if $P$ and $Q$ are paths of maximum length in $G$, then $V(P)\cap V(Q)\neq\varnothing$.
> 2. Does the previous statement remain true if we only assume that $P$ and $Q$ are maximal paths in $G$ (maximal with respect to inclusion)?> [!proof]
> (1) Let $P=v_1v_2\cdots v_k$ and $Q=w_1w_2\cdots w_\ell$ be two paths of maximum length in the connected graph $G$. Suppose, for contradiction, that $V(P)\cap V(Q)=\varnothing$. Since $G$ is connected there is a $v_i,w_j$‑walk joining some vertex $v_i\in V(P)$ to some $w_j\in V(Q)$. Take a shortest such walk and, by Lemma 1.2.5, replace it by a shortest $v_i,w_j$‑path
> $$R=r_0r_1\cdots r_t$$
> with $r_0=v_i\in V(P)$, $r_t=w_j\in V(Q)$ and interior vertices $\{r_1,\dots,r_{t-1}\}$ disjoint from $V(P)\cup V(Q)$. Concatenating the initial segment $v_1\cdots v_i$, the interior of $R$, and the terminal segment $w_j\cdots w_\ell$ yields a simple path
> $$P' := v_1\cdots v_i\, r_1\cdots r_{t-1}\, w_j\cdots w_\ell.$$
> Because $t\ge 1$ we get
> $$|V(P')| \;=\; i + (t-1) + (\ell-j+1) \;\ge\; i + (\ell-j+1) + 1 \;>\; \max\{k,\ell\},$$
> contradicting the maximality of $P$ and $Q$. Therefore $V(P)\cap V(Q)\neq\varnothing$.
> 
> (2) The statement is false for merely maximal paths. "Maximal" (by inclusion) means a path cannot be extended at either endpoint inside $G$, but two distinct maximal paths can be vertex‑disjoint. A simple construction: take two disjoint paths and join an endpoint of one to an endpoint of the other by a single edge so that each original path becomes maximal in the new graph but they remain vertex‑disjoint (see lecture notes for a concrete 6‑vertex example). Thus maximum (longest) paths must intersect in a connected graph, but maximal paths need not.
### Remarks
- The proof of (1) is a standard application of taking a shortest connector between two disjoint structures and concatenating to exceed maximal length.
- Maximal paths are useful in many structural arguments (see [[proposition - maximal paths & cycles]]), but they do not enjoy the same global-length properties as maximum paths.

### Relations
- Shortest-walk → path reduction: [[lemma - walk contains path]].
- Maximal-path techniques: [[proposition - maximal paths & cycles]].
- Path definitions and properties: [[path]], [[walk, trail, path, cycle]].
