#example 
> [!example]
> ### Exercise 9 — Forest decomposition into paths
> Let $F$ be a forest. By the Handshake Lemma there exists a nonnegative integer $k$ such that $F$ has exactly $2k$ vertices of odd degree. Prove that $F$ has a decomposition into $k$ paths.> [!proof]
> Let $F$ be a forest and suppose $F$ has exactly $2k$ vertices of odd degree (the Handshake Lemma guarantees the number of odd-degree vertices is even). We prove by induction on $k$ that $F$ can be decomposed into $k$ edge‑disjoint paths whose union is $E(F)$.
> 
> Base case ($k=0$). If $k=0$ then every vertex of $F$ has even degree. Since a forest contains no cycles, the only forest with all degrees even is the edgeless graph; hence $E(F)=\varnothing$ and the empty decomposition (zero paths) satisfies the claim.
> 
> Inductive step. Assume the statement holds for all forests with $2(k-1)$ odd vertices. Let $F$ have $2k$ odd vertices. If $F$ has multiple components deal with each component separately (the number of odd-degree vertices in each component is even), so we may assume $F$ is a tree.
> 
> Pick two vertices $u,v$ of odd degree in $F$ (possible since there are $2k\ge 2$ such vertices). In a tree there is a unique $u,v$‑path $P$. Remove the edges of $P$ from $F$ to obtain a (possibly disconnected) forest $F'$. Removing $P$ reduces the degree of $u$ and $v$ by $1$ (making them even) and reduces by $2$ the degree of each internal vertex of $P$ (preserving parity). Therefore the number of odd-degree vertices in $F'$ is $2k-2$. By the inductive hypothesis $F'$ decomposes into $k-1$ paths. Adding back the path $P$ yields a decomposition of $F$ into $k$ paths, as required.
> 
> This completes the induction and the proof.
### Remarks
- The argument pairs odd vertices and uses the unique path between them in a tree; removing that path reduces the odd-vertex count by two and allows induction.
- The decomposition is into edge‑disjoint paths whose union is $E(F)$. In algorithms, finding such a decomposition can be done by repeatedly pairing odd vertices within components and removing connecting paths.

### Relations
- Handshake Lemma and parity: [[handshake lemma]].
- Trees and forests: [[tree]].
- Paths and unique path property in trees: [[path]], [[walk, trail, path, cycle]].
