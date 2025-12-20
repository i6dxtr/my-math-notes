#example 
> [!example]
> ### Exercise 2 — Complements and connectivity
> Let $G$ be a graph.
> 1. Prove: If $G$ is disconnected then $\overline{G}$ is connected.
> 2. Is the converse true? (If $G$ is connected then $\overline{G}$ is disconnected.)> [!proof]
> (1) Let $G=(V,E)$ and suppose $G$ is disconnected. Let $A$ be the vertex set of some nonempty component of $G$ and let $B=V\setminus A$ (so $B$ is the union of the remaining components). Take arbitrary $u,v\in V$.
> 
> - If $u\in A$ and $v\in B$ then $uv\notin E(G)$, hence $uv\in E(\overline{G})$ and $u,v$ are adjacent in $\overline{G}$.
> 
> - If $u,v\in A$ then pick any $w\in B$. Since $w$ is in a different component of $G$ we have $uw, vw\notin E(G)$, so $uw, vw\in E(\overline{G})$ and $u$ and $v$ are joined by the path $u-w-v$ in $\overline{G}$.
> 
> The same argument applies when $u,v\in B$ (use a vertex of $A$). Thus every pair of vertices of $\overline{G}$ is connected by a path of length at most $2$, so $\overline{G}$ is connected.
> 
> (2) The converse is false. For a counterexample take the path $P_4$ on vertices $\{1,2,3,4\}$ with edges $\{12,23,34\}$. Then $P_4$ is connected, and a short check shows its complement has edges $\{13,14,24\}$ which form a connected graph as well. Therefore connectivity of $G$ does not imply $\overline{G}$ is disconnected.
### Remarks
- The proof for (1) shows in fact $\operatorname{diam}(\overline{G})\le 2$ when $G$ has exactly two components; more generally $\overline{G}$ is often quite dense when $G$ is disconnected.
- The counterexample $P_k$ vs $\overline{P_k}$ for small $k$ illustrates why the converse fails in general.

### Relations
- Definition: [[content/foundational/graph complement.md]].
- Connectivity and components: [[content/graph structure/connectedness.md]], [[content/foundational/components (graph).md]].
- Useful for diameter/complement arguments: [[content/foundational/distance, diameter.md]].
