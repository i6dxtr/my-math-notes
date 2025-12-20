> [!theorem]
> ### Equivalent conditions for 2‑connected graphs
> Let $G$ be a graph on at least three vertices. The following statements are equivalent.
> 1. $G$ is connected and has no cut‑vertex (i.e. $G$ is 2‑connected).
> 2. For every pair of distinct vertices $u,v\in V(G)$ there exist two internally disjoint $u,v$‑paths.
> 3. For every pair of distinct vertices $u,v\in V(G)$ there exists a cycle $C$ with $u,v\in V(C)$.
> 4. For every pair of distinct edges $e,f\in E(G)$ there exists a cycle $C$ with $e,f\in E(C)$.
> [!proof]
> Sketch of implications (see Notes by date/10-31-25.md for details).
> 
> (1)⇔(2) is Theorem 4.3.2 (characterization via internally disjoint paths).
> 
> (2)⇒(3). Given two internally disjoint $u,v$‑paths $P,Q$, their union contains a cycle passing through $u$ and $v$.
> 
> (3)⇒(4). If for every pair of vertices there is a cycle through them, then by a standard augmentation argument one can arrange cycles to cover any two edges: add auxiliary vertices if necessary and apply (3) to obtain a cycle containing endpoints of the edges which can be converted into a cycle containing the edges themselves (see lecture construction).
> 
> (4)⇒(2). Given distinct vertices $u,v$, pick incident edges $e$ at $u$ and $f$ at $v$ (if needed, choose distinct incident edges). By (4) there is a cycle containing $e$ and $f$; removing the edges $e$ and $f$ from that cycle produces two internally disjoint $u,v$‑paths.
> 
> Collecting these implications yields equivalence of the four statements.
### Relations
- [[theorem - 2-connected via internally disjoint paths]] — Item (2) is the same statement as that theorem.
- [[prop - cycle-edge equivalences]] — Supports the (3)⇔(4) style implications (create/consult proposition file if more details are required).
- [[ Menger-type equivalences]] — Strengthened k‑connectivity statements generalize these equivalences.

