
> [!theorem]
> ### Theorem 3.3.3 (Detailed proof) — Tutte's theorem (induction)
> A graph $G$ has a perfect matching iff $o(G-S)\le |S|$ for every $S\subseteq V(G)$.

> [!proof]
> This file gives the detailed inductive proof and the auxiliary claims used in the lecture notes (Notes by date/10-20-25.md).
> 
> Base case. If $|V(G)|=2$ the statement is trivial.
> 
> Inductive setup. Let $n=|V(G)|$ be even and assume the statement holds for all graphs with fewer than $n$ vertices. Suppose $G$ satisfies Tutte's condition, i.e. $o(G-S)\le |S|$ for all $S\subseteq V(G)$.
> 
> If $o(G)=0$ (every component even) and $G$ is disconnected, argue componentwise: each component has even order and satisfies Tutte's condition restricted to its vertex set, so by induction each component has a perfect matching; combining them yields a perfect matching of $G$.
> 
> Otherwise (nontrivial case) choose a nonempty set $T\subseteq V(G)$ which is maximal subject to the property
> $$
> o(G-T)=|T|.
> $$
> (Existence: since $G$ satisfies Tutte's condition and $G$ has even order, there exists some nonempty $S$ with $o(G-S)=|S|$; choose a maximal one.)
> 
> Claim 1. Every component of $G-T$ is odd.
> 
> Proof. If some component $X$ of $G-T$ were even, then for any vertex $x\in X$ we would have
> $$
> o\bigl(G-(T\cup\{x\})\bigr)=o(G-T)-1=|T|-1,
> $$
> so $T\cup\{x\}$ would contradict the maximality of $T$.
> 
> Label the components of $G-T$ as $X_1,\dots,X_t$, where $t=|T|$ and each $X_i$ is odd.
> 
> Claim 2. For each $i$ and each $v_i\in X_i$, the induced subgraph $G[X_i\setminus\{v_i\}]$ satisfies Tutte's condition and hence (by induction) has a perfect matching.
> 
> Proof. Suppose for some $i$ and $v_i\in X_i$ the graph $G[X_i\setminus\{v_i\}]$ fails Tutte's condition: there exists $S_i\subseteq X_i\setminus\{v_i\}$ with
> $$
> o\bigl(G[X_i\setminus\{v_i\}]-S_i\bigr) > |S_i|.
> $$
> By parity (see parity lemma) this inequality is actually at least $|S_i|+2$, and adding $v_i$ back yields
> $$
> o\bigl(G[X_i]- (S_i\cup\{v_i\})\bigr) \ge |S_i|+1.
> $$
> Replacing $S_i$ by $T\cup S_i\cup\{v_i\}$ in the whole graph $G$ gives
> $$
> o\bigl(G-(T\cup S_i\cup\{v_i\})\bigr)\ge |T| + |S_i|+1 > |T\cup S_i\cup\{v_i\}|,
> $$
> contradicting that $G$ satisfies Tutte's condition. Hence each $G[X_i\setminus\{v_i\}]$ does satisfy Tutte's condition and by induction has a perfect matching.
> 
> Construct auxiliary bipartite graph. Form a bipartite graph $H$ with bipartition $(\mathcal{X},T)$ where $\mathcal{X}=\{X_1,\dots,X_t\}$. Join $X_i\in\mathcal{X}$ to a vertex $u\in T$ in $H$ iff there is at least one edge in $G$ between $u$ and some vertex of $X_i$.
> 
> Claim 3. $H$ satisfies Hall's condition (so $H$ has a matching saturating $\mathcal{X}$).
> 
> Proof. Suppose some $S\subseteq\mathcal{X}$ violates Hall: $|N_H(S)|<|S|$. Let $T'=N_H(S)\subseteq T$. Then consider $G-T'$. The components of $G-T'$ include all $X_i\in S$, and hence
> $$
> o(G-T') \ge |S| > |T'|,
> $$
> contradicting Tutte's condition in $G$. Thus Hall's condition holds, so there is a matching in $H$ that pairs every $X_i$ with a distinct vertex of $T$.
> 
> Finish. For each $i$, let $v_i\in X_i$ be the vertex that the matching in $H$ chooses as the neighbour in $G$ matched to the chosen vertex of $T$. From Claim 2, $G[X_i\setminus\{v_i\}]$ has a perfect matching; combine these matchings with the matching between $T$ and the chosen $v_i$'s to obtain a perfect matching of $G$.
> 
> This completes the induction and thus the proof. ∎
### Relations
- [[theorem - Tutte's theorem]] — Compact statement and short sketch.
- [[lemma - parity lemma (Tutte)]] — Parity facts used in some counting steps.
- [[claim - maximal T set claim]] — (If desired) an explicit small file extracting the maximal-T claim used above.

