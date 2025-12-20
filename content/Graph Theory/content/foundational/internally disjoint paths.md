> [!definition]
> ### Internally disjoint paths
> Two $u,v$‑paths $P$ and $Q$ in a graph $G$ are internally disjoint if
> $$
> \bigl(V(P)\setminus\{u,v\}\bigr)\cap\bigl(V(Q)\setminus\{u,v\}\bigr)=\varnothing.
> $$
> That is, the only vertices the paths share are the endpoints $u$ and $v$.

### Remarks
- Internally disjoint paths are often used to measure redundancy between two vertices: two internally disjoint $u,v$‑paths give a way to connect $u$ and $v$ that remains valid even if an internal vertex on one path is removed.
- The notion generalizes to $k$ pairwise internally disjoint $u,v$‑paths.

### Relations
- [[content/theorems, lemma/theorem - 2-connected via internally disjoint paths.md]] — Characterizes 2‑connectivity in terms of the existence of two internally disjoint $u,v$‑paths for every distinct $u,v$.
- [[content/foundational/path.md]] — Definition of paths and related terminology.
- [[content/theorems, lemma/theorem - Menger / Menger-type equivalences.md]] — Internally disjoint paths appear in Menger‑style statements relating connectivity and disjoint paths.

Source: Notes by date/10-29-25.md
