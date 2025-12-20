# Graph Theory — Map of Content (MOC)

This MOC links the concept notes extracted from lecture notes and "Notes by date". It is organized chronologically by lecture date; under each date are the concept files introduced (atomic concept notes). Use this as the entry point for the concept-first vault.

---

## 2025-08-25
- [[content/foundational/graph.md]] — Definition: Graph
- [[content/foundational/degree.md]] — Degree; min / max degree
- [[content/foundational/neighbor, adjacent.md]] — Neighbor / adjacency / incidence
- [[content/foundational/handshake lemma.md]] — Handshake lemma (degree sum)

## 2025-08-27
- [[content/foundational/order, size.md]] — Order & size
- [[content/graph structure/walk, trail, path, cycle.md]] — Walk / Trail / Path / Cycle
- [[content/graph structure/path.md]] — Path / Cycle (detailed)
- [[content/foundational/graph complement.md]] — Graph complement
- [[content/graph structure/connectedness.md]] — Connectedness
- [[content/foundational/components (graph).md]] — Components (equivalence classes)
- [[content/graph structure/(induced) subgraphs.md]] — Subgraphs / induced subgraphs
- [[content/theorems, lemma/lemma - walk contains path.md]] — Lemma 1.2.5 (walk contains path)
- [[content/foundational/isomorphism (graph).md]] — Graph isomorphism (if present)

## 2025-08-29
- [[content/graph structure/vertex & edge deletion.md]] — Operations: $G-v$, $G-e$
- [[content/graph structure/cut-vertex, cut-edge.md]] — Cut-vertex / Cut-edge
- [[content/theorems, lemma/theorem - edge is cut iff no cycle.md]] — Theorem 1.2.14 (edge is cut ⇔ no cycle)

## 2025-09-03
- [[content/theorems, lemma/lemma - odd walk contains odd cycle.md]] — Lemma 1.2.15 (closed odd walk ⇒ odd cycle)
- [[content/foundational/independent set.md]] — Independent set, $\alpha(G)$
- [[content/foundational/clique.md]] — Clique, $\omega(G)$
- [[content/foundational/chromatic number.md]] — Chromatic number, $k$-partite
- [[content/foundational/distance, diameter.md]] — Distance, diameter, radius

## 2025-09-05
- [[content/theorems, lemma/theorem - bipartite characterization.md]] — Bipartite ⇔ no odd cycles (Theorem 1.2.18)
- [[content/theorems, lemma/theorem - eulerian circuit condition.md]] — Eulerian circuit characterization (Theorem 1.2.26)
- Exercises and examples on diameter / complements

## 2025-09-08
- [[content/theorems, lemma/lemma - minimum degree 2 implies cycle.md]] — Lemma 1.2.25 (min degree $\ge$ 2 ⇒ cycle)
- [[content/theorems, lemma/proposition - decomposition into cycles iff even degree (Proposition 1.2.27).md]] — Decomposition into cycles ⇔ every vertex even degree

## 2025-09-10
- [[content/theorems, lemma/theorem - minimum degree & path-cycle length.md]] — Min-degree implies long paths & cycles (Prop / Dirac prelude)
- [[content/theorems, lemma/proposition - maximal paths & cycles.md]] — Maximal paths & cycles
- Dirac-style / Hamiltonicity remarks (refer to Dirac theorem files)

## 2025-09-12
- Trees (spanning trees, leaves)
  - [[content/foundational/tree.md]] — Tree / Forest / Spanning tree (if present)
  - [[content/theorems, lemma/lemma - tree has two leaves.md]] — Lemma (tree has $\ge$ 2 leaves)
  - [[content/theorems, lemma/theorem - trees characterization.md]] — Equivalent definitions of trees

## 2025-09-15
- Maximal vs maximum paths, propositions on intersections of longest paths
- Related exercises and propositions in [[content/theorems, lemma/proposition - maximal paths & cycles.md]]

## 2025-09-17
- (Lecture notes continued — exercises on trees, decomposition)

## 2025-09-19 to 2025-09-24
- Review, quizzes, and continuation of tree / connectivity exercises
- BFS algorithm / BFST preparation:
  - [[content/graph structure/algorithm - breadth-first search (BFS).md]] — BFS algorithm
  - [[content/graph structure/definition - breadth-first search tree (BFST).md]] — BFST (distance preserving)
  - [[content/theorems, lemma/theorem - BFS preserves distances (Theorem 2.3.8).md]] — BFS preserves distances

## 2025-09-29
- Depth-First Search (DFS) and DFST:
  - [[content/graph structure/algorithm - depth-first search (DFS).md]] — DFS (Algorithm 4.1.21)
  - [[content/graph structure/definition - depth-first search tree (DFST).md]] — DFST definition
  - [[content/theorems, lemma/lemma - DFST edge endpoints on same branch (Lemma 4.1.22).md]] — DFST same-branch property

## 2025-10-01
(Matchings — introduction and structural lemma)
- [[content/foundational/matching.md]] — Matching, perfect, saturated
- [[content/foundational/maximal matching, maximum matching.md]] — Maximal vs maximum
- [[content/foundational/M-alternating path, M-augmenting path.md]] — Alternating / augmenting paths
- [[content/theorems, lemma/lemma - symmetric difference of matchings (Lemma 3.1.9).md]] — Lemma 3.1.9 (symmetric difference structure)
- [[content/theorems, lemma/theorem - Cantor-Schroeder-Bernstein.md]] — Cantor–Schroeder–Bernstein (matching viewpoint)
- Exercises: Exercise 14A (statements introduced)

## 2025-10-03
(Matchings — augmenting paths, Hall, applications)
- [[content/theorems, lemma/theorem - augmenting path characterization.md]] — Maximum matching ⇔ no M-augmenting path
- [[content/theorems, lemma/theorem - Hall's theorem (Theorem 3.1.11).md]] — Hall's marriage theorem
- [[content/theorems, lemma/theorem - KÃ¶nigâ€“EgervÃ¡ry (1931).md]] — König–Egerváry theorem (maximum matching = minimum vertex cover in bipartite graphs)
- [[content/examples/exercise - 14a.md]] — Exercises 14a (symmetric difference consequences)
- Examples: deck-of-cards application, bipartite matching constructions

## 2025-10-15
- [[content/foundational/edge cover.md]] — Definition: Edge cover, $\beta'(G)$
- [[content/theorems, lemma/lemma - star forest.md]] — Lemma: Star forest for minimum edge cover
- [[content/theorems, lemma/theorem - matching + edge cover = n.md]] — Theorem: $\alpha'(G)+\beta'(G)=n$
- [[content/examples/example - hall via konig-egervary.md]] — Example: Hall via Kőnig–Egerváry
- [[content/examples/example - non-bipartite alpha equals beta.md]] — Example: non-bipartite graph with $\alpha'(G)=\beta(G)$

## 2025-10-17
- [[content/foundational/odd components.md]] — Definition: odd components & Tutte's condition (from Notes by date/10-17-25.md)
- [[content/theorems, lemma/theorem - Tutte's theorem.md]] — Tutte's theorem (Theorem 3.3.3) — statement + proof sketch (from Notes by date/10-17-25.md)
- [[content/theorems, lemma/lemma - parity lemma (Tutte).md]] — Parity lemma: relation between $n$ and $o(G-S)-|S|$ (short lemma extracted from 10-17-25.md)

## 2025-10-20
- [[content/theorems, lemma/theorem - Tutte's theorem (detailed proof).md]] — Full induction proof and auxiliary claims (from Notes by date/10-20-25.md). (Create as an expanded proof file that links to the main theorem file.)
- [[content/theorems, lemma/claim - maximal T set claim.md]] — Claim used in the inductive proof (definition and proof of maximal set $T$ with $o(G-T)=|T|$)

## 2025-10-22
- [[content/theorems, lemma/corollary - number of vertices saturated by maximum matching (3.3.7).md]] — Corollary 3.3.7 (definition of $d=\max\{o(G-S)-|S|:S\subseteq V(G)\}$ and proof that a maximum matching saturates exactly $n-d$ vertices) (from Notes by date/10-22-25.md)
- [[content/theorems, lemma/corollary - Petersen 3-regular perfect matching (3.3.8).md]] — Corollary 3.3.8 (Petersen 1891): every 3-regular graph with no cut-edge has a perfect matching — statement and proof using Tutte's theorem (from Notes by date/10-22-25.md)

## 2025-10-24
- [[separating set, k-connectivity]] — Definitions: separating set (vertex cut), connectivity $\kappa(G)$, $k$-connected graphs; include the complete-graph connectivity remark and short proof (from Notes by date/10-24-25.md)
- [[content/theorems, lemma/remark - connectivity of K_n.md]] — Short remark/proof: $\kappa(K_n)=n-1$ (lifted from 10-24-25.md)

## 2025-10-27
- [[content/foundational/disconnecting set, edge-connectivity.md]] — Definitions and core results: disconnecting set of edges, $k$-edge-connected, edge-connectivity $\kappa'(G)$. This file also contains the lemma that every minimal disconnecting set is an edge-cut and Whitney's inequality $\kappa(G)\le\kappa'(G)\le\delta(G)$ (from Notes by date/10-27-25.md)

## 2025-10-29
- [[content/foundational/internally disjoint paths.md]] — Definition: internally disjoint $u,v$-paths (from 10-29-25.md)
- [[content/theorems, lemma/theorem - 2-connected via internally disjoint paths.md]] — Theorem: $G$ is 2-connected iff every pair $u,v$ has two internally disjoint $u,v$-paths (with proof) (from 10-29-25.md)

## 2025-10-31
- [[content/theorems, lemma/theorem - equivalent conditions for 2-connected graphs.md]] — Expanded list of equivalent conditions for 2-connectivity (items i–iv from Notes by date/10-31-25.md), plus proofs and examples
- [[content/theorems, lemma/prop - cycle-edge equivalences.md]] — Support propositions relating cycles and edges used in equivalence proofs (from 10-31-25.md)

## 2025-11-03
- [[content/foundational/X,Y-paths and fans.md]] — Definitions: $X,Y$-path, $x-Y$ fan, precise fan definition and small examples (from Notes by date/11-3-25.md)
- [[content/theorems, lemma/theorem - Menger / Menger-type equivalences.md]] — Menger/Mangels theorem style equivalences ($k$-connectivity ⇔ $k$ internally disjoint paths ⇔ fans ⇔ disjoint $X-Y$ paths) with statements and references (from 11-3-25.md)
- [[content/theorems, lemma/theorem - ChvÃ¡tal-ErdÅ‘s Hamiltonicity condition.md]] — Theorem 7.2.19 (Chvátal–Erdős 1972): if $\kappa(G) \ge \alpha(G)$ then $G$ is Hamiltonian — statement and sketch (from Notes by date/11-3-25.md)

## 2025-11-05
- [[content/theorems, lemma/theorem - Chvátal-Erdős Hamiltonicity condition.md]] — Theorem 7.2.19 (Chvátal–Erdős 1972): $\kappa(G)\ge\alpha(G)$ ⇒ $G$ has a Hamiltonian cycle (proof details from Notes by date/11-5-25.md)
- [[content/theorems, lemma/theorem - min degree implies connectivity vs independence.md]] — Theorem: If $\delta(G)\ge n/2$ then $\kappa(G)\ge\alpha(G)$ (proof from Notes by date/11-5-25.md)

## 2025-11-12
- [[content/foundational/X,Y-barrier.md]] — Definition 4.2.15: $X,Y$-barrier and definitions of $\lambda(X,Y)$ and $\kappa(X,Y)$ (from Notes by date/11-12-25.md)
- [[content/theorems, lemma/theorem - Menger local sets (Pym 1969).md]] — Menger’s theorem (local sets version / Pym 1969): $\lambda(X,Y)=\kappa(X,Y)$ with proof outline (from Notes by date/11-12-25.md)

## 2025-11-19
- [[content/examples/exercise - greedy coloring ordering.md]] — Exercise 27: vertex orderings for the greedy coloring algorithm (existence of an ordering achieving $\chi(G)$ and counterexamples where a bad ordering uses more colors) (from Notes by date/11-19-25.md)
- [[content/theorems, lemma/theorem - Mycielski construction.md]] — Mycielski (1955): for all $k\ge 2$ there exists $G$ with $\omega(G)=2$ and $\chi(G)=k$ (construction and proof sketch from Notes by date/11-19-25.md)

## 2025-11-21
- [[content/theorems, lemma/theorem - Mycielski construction.md]] — Theorem 5.2.3 (Mycielski 1955): Mycielski's construction preserves triangle-free property and increases chromatic number by 1 (proof details from Notes by date/11-21-25.md)
- [[content/theorems, lemma/theorem - Gallai-Roy-Vitaver (1968).md]] — Theorem 5.1.21 (Gallai–Roy–Vitaver): orientation-length bound on chromatic number and existence of an orientation realizing equality (from Notes by date/11-21-25.md)

## 2025-12-01
- [[content/examples/example - chromatic bound by edges.md]] — Bound: $\chi(G)<1+\sqrt{2m}$ (from Notes by date/12-1-25.md)
- [[content/theorems, lemma/corollary - Rédei tournament Hamiltonian path.md]] — Rédei (1934): every tournament has a Hamiltonian path (Corollary of Gallai–Roy–Vitaver)
- [[content/theorems, lemma/corollary - Erdös-Szekeres subsequence.md]] — Erdős–Szekeres subsequence theorem (1935) — combinatorial subsequence result (application of Gallai–Roy–Vitaver)

---
Sources / Lecture mapping
- Primary: lecture/438Notes_f25.pdf (lecture statements & proofs)
- Supplementary: Notes by date/* (10-17-25.md → 11-3-25.md)
