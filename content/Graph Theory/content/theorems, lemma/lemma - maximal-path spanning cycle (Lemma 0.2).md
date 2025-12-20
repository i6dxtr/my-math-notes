#lemma 
> [!theorem]
> ### Lemma — Maximal-path spanning cycle and path existence (Lemma 0.2)
> Let $G$ be a graph and let $P$ be a maximal path in $G$ with vertex sequence $x_1x_2\ldots x_\ell$.
> 
> ---
> **(i).** If $|V(P)|=\ell \le 2\delta(G)$, then the graph induced by $V(P)$ contains a spanning cycle (a cycle visiting every vertex of $P$).
> 
> ---
> **(ii).** For all $1\le k\le \frac{n-1}{2}$, if $G$ is connected and $\delta(G)\ge k$, then $G$ contains a path with at least $2k+1$ vertices.
> [!proof]
> **(i).** Let $P=x_1x_2\ldots x_\ell$ be a maximal path with $\ell\le 2\delta(G)$. Set
> $$
> S=\{x_{i-1} : x_i\in N(x_1)\}\quad\text{and}\quad T=N(x_\ell).
> $$
> Note $|S|=|N(x_1)|\ge\delta(G)$ and $|T|=|N(x_\ell)|\ge\delta(G)$, while $S\cup T\subseteq\{x_1,\dots,x_{\ell-1}\}$ so $|S\cup T|\le \ell-1\le 2\delta(G)-1$. Hence
> $$
> |S\cap T| = |S|+|T|-|S\cup T| \ge 2\delta(G)-(2\delta(G)-1)=1,
> $$
> so there exists an index $i$ with $x_{i-1}\in S\cap T$. Then
> $$
> x_1x_2\ldots x_{i-1}x_\ell x_{\ell-1}\ldots x_i x_1
> $$
> is a cycle that spans $V(P)$.
> 
> 
> ---
> **(ii).** Suppose $G$ is connected and $\delta(G)\ge k$ but every path has fewer than $2k+1$ vertices. Let $P$ be a maximum-length path; then $|V(P)|\le 2k$. By part (i) the subgraph induced by $V(P)$ contains a spanning cycle. Since $G$ is connected and $|V(P)|\le n-1$, there is an edge from some vertex of the cycle to $V(G)\setminus V(P)$, and following that edge yields a path longer than $P$, contradicting maximality. Therefore $G$ contains a path with at least $2k+1$ vertices.
### Source
- Notes by date/9-12-25.md (figures referenced)

### Figures
![[Pasted image 20250912134553.png]]
![[Pasted image 20250912140559.png]]

### Relations
- Maximal path and cycle techniques: [[proposition - maximal paths & cycles]]
- Minimum-degree consequences and Dirac-type results: [[theorem - minimum degree & path-cycle length]], [[theorem - dirac (hamiltonian)]]
- Uses path/cycle definitions: [[walk, trail, path, cycle]], [[path]]
