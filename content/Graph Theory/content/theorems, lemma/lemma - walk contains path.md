#theorem
> [!theorem]
> ### Lemma 1.2.5.
> Let $G$ be a graph and $u,v \in V(G)$. Every $uv$‑walk contains a $uv$‑path.
> [!proof]
> Take a $uv$‑walk of minimal length among all $uv$‑walks.  
> If this walk repeats any vertex, then a shorter walk between $u$ and $v$ can be obtained by deleting the closed segment between the repetitions.  
> By minimality this is impossible — hence the minimal $uv$‑walk is a $uv$‑path.
### Relations   
- Directly ties [[content/graph structure/walk, trail, path, cycle.md|walk, trail, path, cycle]] concepts together.
- Used in the proof of [[content/theorems, lemma/theorem - edge is cut iff no cycle.md|theorem - edge is cut iff no cycle]] to guarantee existence of replacement paths.
- A foundational lemma for connectivity arguments ([[content/graph structure/connectedness.md|connectedness]], [[content/foundational/components (graph).md|components (graph)]]).
