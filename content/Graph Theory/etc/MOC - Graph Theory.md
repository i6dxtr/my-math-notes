# Graph Theory — Map of Content (MOC)

This MOC links the concept notes extracted from lecture notes and "Notes by date". It is organized chronologically by lecture date; under each date are the concept files introduced (atomic concept notes). Use this as the entry point for the concept-first vault.

---

## 2025-08-25
- [[graph]] — Definition: Graph
- [[degree]] — Degree; min / max degree
- [[neighbor, adjacent]] — Neighbor / adjacency / incidence
- [[handshake lemma]] — Handshake lemma (degree sum)

## 2025-08-27
- [[order, size]] — Order & size
- [[walk, trail, path, cycle]] — Walk / Trail / Path / Cycle
- [[path]] — Path / Cycle (detailed)
- [[graph complement]] — Graph complement
- [[connectedness]] — Connectedness
- [[components (graph)]] — Components (equivalence classes)
- [[(induced) subgraphs]] — Subgraphs / induced subgraphs
- [[lemma - walk contains path]] — Lemma 1.2.5 (walk contains path)
- [[isomorphism (graph)]] — Graph isomorphism (if present)

## 2025-08-29
- [[vertex & edge deletion]] — Operations: $G-v$, $G-e$
- [[cut-vertex, cut-edge]] — Cut-vertex / Cut-edge
- [[theorem - edge is cut iff no cycle]] — Theorem 1.2.14 (edge is cut ⇔ no cycle)

## 2025-09-03
- [[lemma - odd walk contains odd cycle]] — Lemma 1.2.15 (closed odd walk ⇒ odd cycle)
- [[independent set]] — Independent set, $\alpha(G)$
- [[clique]] — Clique, $\omega(G)$
- [[chromatic number]] — Chromatic number, $k$-partite
- [[distance, diameter]] — Distance, diameter, radius

## 2025-09-05
- [[theorem - bipartite characterization]] — Bipartite ⇔ no odd cycles (Theorem 1.2.18)
- [[theorem - eulerian circuit condition]] — Eulerian circuit characterization (Theorem 1.2.26)
- Exercises and examples on diameter / complements

## 2025-09-08
- [[lemma - minimum degree 2 implies cycle]] — Lemma 1.2.25 (min degree $\ge$ 2 ⇒ cycle)
- [[proposition - decomposition into cycles iff even degree (Proposition 1.2.27)]] — Decomposition into cycles ⇔ every vertex even degree

## 2025-09-10
- [[theorem - minimum degree & path-cycle length]] — Min-degree implies long paths & cycles (Prop / Dirac prelude)
- [[proposition - maximal paths & cycles]] — Maximal paths & cycles
- Dirac-style / Hamiltonicity remarks (refer to Dirac theorem files)

## 2025-09-12
- Trees (spanning trees, leaves)
  - [[tree]] — Tree / Forest / Spanning tree (if present)
  - [[lemma - tree has two leaves]] — Lemma (tree has $\ge$ 2 leaves)
  - [[theorem - trees characterization]] — Equivalent definitions of trees

## 2025-09-15
- Maximal vs maximum paths, propositions on intersections of longest paths
- Related exercises and propositions in [[proposition - maximal paths & cycles]]

## 2025-09-17
- (Lecture notes continued — exercises on trees, decomposition)

## 2025-09-19 to 2025-09-24
- Review, quizzes, and continuation of tree / connectivity exercises
- BFS algorithm / BFST preparation:
  - [[algorithm - breadth-first search (BFS)]] — BFS algorithm
  - [[definition - breadth-first search tree (BFST)]] — BFST (distance preserving)
  - [[theorem - BFS preserves distances (Theorem 2.3.8)]] — BFS preserves distances

## 2025-09-29
- Depth-First Search (DFS) and DFST:
  - [[algorithm - depth-first search (DFS)]] — DFS (Algorithm 4.1.21)
  - [[definition - depth-first search tree (DFST)]] — DFST definition
  - [[lemma - DFST edge endpoints on same branch (Lemma 4.1.22)]] — DFST same-branch property

## 2025-10-01
(Matchings — introduction and structural lemma)
- [[matching]] — Matching, perfect, saturated
- [[maximal matching, maximum matching]] — Maximal vs maximum
- [[M-alternating path, M-augmenting path]] — Alternating / augmenting paths
- [[lemma - symmetric difference of matchings (Lemma 3.1.9)]] — Lemma 3.1.9 (symmetric difference structure)
- [[theorem - Cantor-Schroeder-Bernstein]] — Cantor–Schroeder–Bernstein (matching viewpoint)
- Exercises: Exercise 14A (statements introduced)

## 2025-10-03
(Matchings — augmenting paths, Hall, applications)
- [[theorem - augmenting path characterization]] — Maximum matching ⇔ no M-augmenting path
- [[theorem - Hall's theorem (Theorem 3.1.11)]] — Hall's marriage theorem
- [[theorem - KÃ¶nigâ€“EgervÃ¡ry (1931)]] — König–Egerváry theorem (maximum matching = minimum vertex cover in bipartite graphs)
- [[exercise - 14a]] — Exercises 14a (symmetric difference consequences)
- Examples: deck-of-cards application, bipartite matching constructions

## 2025-10-15
- [[edge cover]] — Definition: Edge cover, $\beta'(G)$
- [[lemma - star forest]] — Lemma: Star forest for minimum edge cover
- [[theorem - matching + edge cover = n]] — Theorem: $\alpha'(G)+\beta'(G)=n$
- [[example - hall via konig-egervary]] — Example: Hall via Kőnig–Egerváry
- [[example - non-bipartite alpha equals beta]] — Example: non-bipartite graph with $\alpha'(G)=\beta(G)$

## 2025-10-17
- [[odd components]] — Definition: odd components & Tutte's condition (from Notes by date/10-17-25.md)
- [[theorem - Tutte's theorem]] — Tutte's theorem (Theorem 3.3.3) — statement + proof sketch (from Notes by date/10-17-25.md)
- [[lemma - parity lemma (Tutte)]] — Parity lemma: relation between $n$ and $o(G-S)-|S|$ (short lemma extracted from 10-17-25.md)

## 2025-10-20
- [[theorem - Tutte's theorem (detailed proof)]] — Full induction proof and auxiliary claims (from Notes by date/10-20-25.md). (Create as an expanded proof file that links to the main theorem file.)
- [[claim - maximal T set claim]] — Claim used in the inductive proof (definition and proof of maximal set $T$ with $o(G-T)=|T|$)

## 2025-10-22
- [[corollary - number of vertices saturated by maximum matching (3.3.7)]] — Corollary 3.3.7 (definition of $d=\max\{o(G-S)-|S|:S\subseteq V(G)\}$ and proof that a maximum matching saturates exactly $n-d$ vertices) (from Notes by date/10-22-25.md)
- [[corollary - Petersen 3-regular perfect matching (3.3.8)]] — Corollary 3.3.8 (Petersen 1891): every 3-regular graph with no cut-edge has a perfect matching — statement and proof using Tutte's theorem (from Notes by date/10-22-25.md)

## 2025-10-24
- [[separating set, k-connectivity]] — Definitions: separating set (vertex cut), connectivity $\kappa(G)$, $k$-connected graphs; include the complete-graph connectivity remark and short proof (from Notes by date/10-24-25.md)
- [[remark - connectivity of K_n]] — Short remark/proof: $\kappa(K_n)=n-1$ (lifted from 10-24-25.md)

## 2025-10-27
- [[disconnecting set, edge-connectivity]] — Definitions and core results: disconnecting set of edges, $k$-edge-connected, edge-connectivity $\kappa'(G)$. This file also contains the lemma that every minimal disconnecting set is an edge-cut and Whitney's inequality $\kappa(G)\le\kappa'(G)\le\delta(G)$ (from Notes by date/10-27-25.md)

## 2025-10-29
- [[internally disjoint paths]] — Definition: internally disjoint $u,v$-paths (from 10-29-25.md)
- [[theorem - 2-connected via internally disjoint paths]] — Theorem: $G$ is 2-connected iff every pair $u,v$ has two internally disjoint $u,v$-paths (with proof) (from 10-29-25.md)

## 2025-10-31
- [[theorem - equivalent conditions for 2-connected graphs]] — Expanded list of equivalent conditions for 2-connectivity (items i–iv from Notes by date/10-31-25.md), plus proofs and examples
- [[prop - cycle-edge equivalences]] — Support propositions relating cycles and edges used in equivalence proofs (from 10-31-25.md)

## 2025-11-03
- [[X,Y-paths and fans]] — Definitions: $X,Y$-path, $x-Y$ fan, precise fan definition and small examples (from Notes by date/11-3-25.md)
- [[theorem - Menger \ Menger-type equivalences]] — Menger/Mangels theorem style equivalences ($k$-connectivity ⇔ $k$ internally disjoint paths ⇔ fans ⇔ disjoint $X-Y$ paths) with statements and references (from 11-3-25.md)
- [[theorem - ChvÃ¡tal-ErdÅ‘s Hamiltonicity condition]] — Theorem 7.2.19 (Chvátal–Erdős 1972): if $\kappa(G) \ge \alpha(G)$ then $G$ is Hamiltonian — statement and sketch (from Notes by date/11-3-25.md)

## 2025-11-05
- [[theorem - Chvátal-Erdős Hamiltonicity condition]] — Theorem 7.2.19 (Chvátal–Erdős 1972): $\kappa(G)\ge\alpha(G)$ ⇒ $G$ has a Hamiltonian cycle (proof details from Notes by date/11-5-25.md)
- [[theorem - min degree implies connectivity vs independence]] — Theorem: If $\delta(G)\ge n/2$ then $\kappa(G)\ge\alpha(G)$ (proof from Notes by date/11-5-25.md)

## 2025-11-12
- [[X,Y-barrier]] — Definition 4.2.15: $X,Y$-barrier and definitions of $\lambda(X,Y)$ and $\kappa(X,Y)$ (from Notes by date/11-12-25.md)
- [[theorem - Menger local sets (Pym 1969)]] — Menger’s theorem (local sets version / Pym 1969): $\lambda(X,Y)=\kappa(X,Y)$ with proof outline (from Notes by date/11-12-25.md)

## 2025-11-19
- [[exercise - greedy coloring ordering]] — Exercise 27: vertex orderings for the greedy coloring algorithm (existence of an ordering achieving $\chi(G)$ and counterexamples where a bad ordering uses more colors) (from Notes by date/11-19-25.md)
- [[theorem - Mycielski construction]] — Mycielski (1955): for all $k\ge 2$ there exists $G$ with $\omega(G)=2$ and $\chi(G)=k$ (construction and proof sketch from Notes by date/11-19-25.md)

## 2025-11-21
- [[theorem - Mycielski construction]] — Theorem 5.2.3 (Mycielski 1955): Mycielski's construction preserves triangle-free property and increases chromatic number by 1 (proof details from Notes by date/11-21-25.md)
- [[theorem - Gallai-Roy-Vitaver (1968)]] — Theorem 5.1.21 (Gallai–Roy–Vitaver): orientation-length bound on chromatic number and existence of an orientation realizing equality (from Notes by date/11-21-25.md)

## 2025-12-01
- [[example - chromatic bound by edges]] — Bound: $\chi(G)<1+\sqrt{2m}$ (from Notes by date/12-1-25.md)
- [[corollary - Rédei tournament Hamiltonian path]] — Rédei (1934): every tournament has a Hamiltonian path (Corollary of Gallai–Roy–Vitaver)
- [[corollary - Erdös-Szekeres subsequence]] — Erdős–Szekeres subsequence theorem (1935) — combinatorial subsequence result (application of Gallai–Roy–Vitaver)

---
Sources / Lecture mapping
- Primary: lecture/438Notes_f25.pdf (lecture statements & proofs)
- Supplementary: Notes by date/* (10-17-25.md → 11-3-25.md)
