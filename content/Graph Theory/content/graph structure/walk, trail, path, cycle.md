#definition #graph-structure
> [!definition]
> ### Definition: Walk, Trail, Path
> Given a graph $G$ and $u,v\in V( G ),$ a **$uv-$ walk** is a list of vertices and edges $$v_{0}e_{1}v_{1}e_{2}v_{2}...v_{k-1}e_{k}v_{k}$$... such that $$v_{0}=u, v_{k}=v,$$... and $\forall i\in \left[ k \right],$ $$e_{i}=v_{i-1}v_{1}.$$
> - A **$uv-$trail** is a $uv-$walk with with no repeated edges.
> - A $uv-$walk is **closed** if $u=v.$
> - A **$uv-$path** is a $uv-$walk with no repeated vertices.
> 
> ![[Pasted image 20250828181445.png]]

> [!example]
> ![[Pasted image 20250902182228.png]]
### Relations
- See [[path]] for the specific object and [[lemma - walk contains path]] for the reduction from walks to paths.
- Connectedness is defined using paths (see [[connectedness]]).
- Trails appear in Eulerian circuit characterizations; see [[theorem - eulerian circuit condition]].
- Also related to cycle/odd-cycle results such as [[lemma - odd walk contains odd cycle]].
- Walks, paths, and cycles underpin search algorithms (BFS/DFs) and their trees: [[algorithm - breadth-first search (BFS)]], [[definition - breadth-first search tree (BFST)]], [[algorithm - depth-first search (DFS)]], [[definition - depth-first search tree (DFST)]].
- They also support matching theory constructions (alternating/augmenting paths) and Tutte/Hall applications: [[M-alternating path, M-augmenting path]], [[matching]], [[Hall's theorem (Theorem 3.1.11)]], [[Tutte's theorem]].
