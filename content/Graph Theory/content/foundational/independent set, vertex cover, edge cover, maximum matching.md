#foundational
canonical definition files (follow these links)
- [[content/foundational/independent set.md|Independent set]] — Definition of independent (stable) sets and the independence number $\alpha(G)$.
- [[content/foundational/vertex cover.md|Vertex cover]] — Definition of vertex covers and the vertex cover number $\beta(G)$; complementary relation with independent sets and standard bounds.
- [[content/foundational/edge cover.md|Edge cover]] — Definition of edge covers and $\beta'(G)$; star‑forest structure for minimum edge covers and relation to matchings.
- [[content/foundational/matching.md|Matching]] — Basic matching definitions (matching, saturated/unsaturated vertices, perfect matching).
- [[content/foundational/maximal matching, maximum matching.md|Maximal vs Maximum matching]] — Precise distinction and properties of maximal and maximum matchings.
- [[content/foundational/M-alternating path, M-augmenting path.md|M‑alternating and M‑augmenting paths]] — Alternating/augmenting paths and Berge’s augmenting‑path theorem.
- [[content/theorems, lemma/theorem - K ̈onig 1931, Egerv ́ary 1931.md|König–Egerváry theorem]] — Exact cover–matching equality for bipartite graphs.
- [[content/theorems, lemma/theorem - Tutte's theorem.md|Tutte’s theorem]] — Characterization of perfect matchings in general graphs (odd components condition).

### Notes on organization
- The detailed definitions and proofs were intentionally kept in small, atomic files to match the vault conventions described in etc/system prompt.md.
- If you want this file to contain short extracts (e.g., one‑sentence summaries or key identities such as $\alpha(G)+\beta(G)=n$) I can add those, but I avoided duplication to keep the vault single‑source for each concept.

### Relations / quick references
- Cover–matching relations: see [[content/foundational/vertex cover.md|vertex cover]] and [[content/foundational/matching.md|matching]].
- Edge cover ↔ matching identity: see [[content/foundational/edge cover.md|edge cover]] and [[content/theorems, lemma/theorem - matching + edge cover = n.md|matching + edge cover = n]].
- Algorithmic notes: for algorithmic matching methods (Hopcroft–Karp, Edmonds’ blossom) see [[content/examples/example - blossom algorithm remark.md|blossom algorithm remark]].

If you want me to:
- Insert short proof sketches in the atomic files (e.g., α + β = n, α' + β' = n), say which identities you want expanded and I will add ~~~ad-proof blocks.
- Remove this index file entirely and rely only on the MOC links, say so and I will delete it.
