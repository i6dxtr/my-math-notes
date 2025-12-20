#definition 
> [!definition]
> ### Definition — $M$-alternating path and $M$-augmenting path
> Let $G$ be a graph and let $M$ be a matching in $G$.
> 
> ---
> An $M$-alternating path is a path in $G$ whose edges alternate between edges in $M$ and edges in $E(G)\setminus M$.
> 
> ---
> An $M$-augmenting path is an $M$-alternating path whose endpoints are both $M$-unsaturated (i.e., neither endpoint is incident with an edge of $M$).

> [!remark]
> - If $P$ is an $M$-augmenting path, then toggling the membership of the edges of $P$ (replace $M\cap E(P)$ by $E(P)\setminus M$) yields a matching of size $|M|+1$.
> - Alternating and augmenting paths underlie classical matching algorithms (e.g., augmenting-path methods).

### Source
- lecture/438Notes_f25.pdf — Definition 3.1.6 ($M$‑alternating/$M$‑augmenting paths)
- Notes by date/9-28-25.md

### Relations
- Base matching notions: [[matching]]
- Maximal vs maximum: [[maximal matching, maximum matching]]
- Path notions: [[path]], [[walk, trail, path, cycle]]
