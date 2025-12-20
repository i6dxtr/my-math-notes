#theorem 
> [!theorem]
> ### Theorem (Dirac, 1952) — Sufficient condition for Hamiltonicity
> Let $G$ be a graph on $n\ge 3$ vertices. If $\delta(G)\ge n/2$ then $G$ contains a **Hamiltonian cycle** (equivalently, $G$ is **Hamiltonian**).
- sufficient, not necessary
> [!proof]
> Let $P=v_1v_2\ldots v_\ell$ be a longest path in $G$. By Proposition 1.2.28 we have $\ell\ge n/2+1$.  
> Define
> $$
> S=\{v_{i-1} : v_i\in N(v_1)\}\quad\text{and}\quad T=N(v_\ell).
> $$
> Note that $S\subseteq\{v_1,\dots,v_{\ell-1}\}$ and $T\subseteq\{v_1,\dots,v_{\ell-1}\}$. Since $|N(v_1)|\ge n/2$ and $|N(v_\ell)|\ge n/2$ we get $|S|\ge n/2$ and $|T|\ge n/2$. Therefore
> $$
> |S\cap T| = |S|+|T|-|S\cup T| \ge \frac{n}{2}+\frac{n}{2}-(\ell-1) \ge 1,
> $$
> so there exists an index $i$ with $v_{i-1}\in S\cap T$. Thus $v_{i-1}\in N(v_1)$ and $v_{i-1}\in N(v_\ell)$, and the cycle
> $$
> v_1v_2\ldots v_{i-1}v_\ell v_{\ell-1}\ldots v_i v_1
> $$
> has length $\ell$. If $\ell=n$ we are done. Otherwise, since $|V(G)\setminus V(C)|<n/2$ there must be an edge from some vertex $w\in V(G)\setminus V(C)$ to $C$, which yields a path longer than $P$, contradicting the maximality of $P$. Hence $\ell=n$ and $G$ has a Hamiltonian cycle.
### Relations
- See [[theorem - minimum degree & path-cycle length]] and [[proposition - maximal paths & cycles]] for related minimum-degree and maximal-path results.
- Uses path notation and maximal-path arguments; see [[path]] and [[walk, trail, path, cycle]].


