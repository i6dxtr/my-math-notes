> [!example]
> ### Exercise 25. Let $G$ be a $k$-connected graph.
> (i) Prove that if $k \ge 2$ and $S \subseteq V(G)$ with $|S| = k,$ then $G$ has a cycle $C$ such that $S \subseteq V(C).$
> 
> (Hint: Begin by letting $C$ be a cycle which contains as many vertices from $S$ as possible. If $C$ doesn't contain every vertex from $S,$ use the "Fan Lemma.")
> 
> (ii) Prove that if $k \ge 1$ and $S \subseteq V(G)$ with $|S| = k+1,$ then $G$ has a path $P$ such that $S \subseteq V(P).$
> 
> (Hint: When $k=1$ this is easy and when $k \ge 2,$ we can use part (i).)~~~ad-proof
**Proof of i.** Let $C$ be a cycle which contains as many vertices from $S$ as possible and suppose there exists some $x \in S \setminus V(C).$ Let $V(C)$ and let $F$ be a $x, V(C)$-fan containing $\min\{|V(C)|, k\}$-many paths. If $|V(C)| \le k-1,$ then we clearly have a cycle which contains $\{x\} \cup V(C),$ contradicting the maximality of $C.$ So suppose $|V(C)| \ge k.$ Let $P_1, \dots, P_k$ be the paths in $F$ and $x_1, \dots, x_k$ be the endpoints of $P_1, \dots, P_k$ in $V(C)$ cyclically ordered. For all $i \in [k],$ let $[x_i, x_{i+1})$ denote the vertices on the segment $x_i C x_{i+1} - x_{i+1}$ (if $i=k,$ then let $[x_k, x_{k+1})$ denote the vertices on the segment $v_k C v_1 - v_1).$ Since we are $|S \cap V(C)| < k$ and we have partitioned $V(C)$ into $k$ non-empty intervals, there exists some $i \in [k]$ such that $S \cap [x_i, x_{i+1}) = \emptyset.$ But now $x_i P_i x P_{i+1} x_{i+1} C x_i$ is a cycle which contains more vertices from $S$ than $C.$ $\square$

**Proof of ii.** Let $S = \{v_1, \dots, v_k, v_{k+1}\}.$ By Theorem 4.2.24, there exists a cycle $C = u_1 u_2 \dots u_t$ containing $v_1, \dots, v_k.$ If $v_{k+1} \in V(C),$ then we are done; so suppose not. Let $Q$ be a shortest $v_{k+1}, V(C)$-path with endpoint $u_i.$ Now $P = v_{k+1} Q u_i u_{i+1} C u_{i-1}$ is a path such that $S \subseteq V(P).$ $\square$


Relations
- [[theorem - 2-connected via internally disjoint paths]]
- [[ Menger-type equivalences]]
- [[lemma - DFST edge endpoints on same branch (Lemma 4.1.22)]]
