> [!example]
> ### Remark — Blossom algorithm (Edmonds)
> The lecture notes mention the blossom algorithm as the canonical algorithmic tool for finding maximum matchings in general graphs (including non‑bipartite graphs). Informally, the blossom algorithm repeatedly finds augmenting paths; when an odd cycle ("blossom") obstructs a direct augmenting path search, the algorithm contracts the blossom, continues the search in the contracted graph, then expands blossoms and lifts augmenting paths back to the original graph.
> 
> This file is a short remark linking the algorithmic context to Tutte's theorem and the corollaries about maximum matchings discussed in lecture.
> [!remark]
> Do not treat this note as a full algorithm description. For implementation details and proofs of correctness refer to Edmonds' original paper on the blossom algorithm or standard algorithmic graph theory texts. This remark is intended to record the lecture pointer and provide links to the related concept notes.
### Relations
- [[matching]] — Basic definitions: matchings, perfect matchings, augmenting paths.
- [[theorem - Tutte's theorem]] — Tutte's theorem gives a structural characterization of perfect matchings; the blossom algorithm is the constructive procedure to find maximum matchings in practice.
- [[corollary - number of vertices saturated by maximum matching (3.3.7)]] — Practical algorithmic connection: after computing a maximum matching, the corollary quantifies saturation in terms of Tutte's obstruction parameter $d$.

