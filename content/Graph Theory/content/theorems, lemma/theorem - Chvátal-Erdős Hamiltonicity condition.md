> [!theorem]
> ### Theorem 7.2.19 *(Chvátal–Erdős 1972)*
> Let $G$ be a graph on $n\ge 3$ vertices. If $\kappa(G)\ge \alpha(G)$ (connectivity at least independence number) then $G$ has a Hamiltonian cycle.
> [!proof]
> Sketch.
> 
> Let $C$ be a longest cycle in $G$. Suppose $C$ is not Hamiltonian and let $v\in V(G)\setminus V(C)$. Using the assumption $\kappa(G)\ge \alpha(G)$ one shows that $v$ has sufficiently many neighbors on $C$ and that these neighbors are distributed around $C$ so that two of them may be used to extend $C$, contradicting maximality. The full argument uses connectivity to find disjoint paths (Menger-type arguments) and the bound $\alpha(G)$ to control independent sets that could block extensions. See lecture notes (Notes by date/11-3-25.md) for the detailed lecture sketch.
### Remarks
- This theorem is a connectivity‑versus‑independence condition implying Hamiltonicity; it complements degree‑based criteria like Dirac's theorem by using structural parameters.
- The statement is sharp in various regimes and has several refinements and related sufficient conditions in the literature.

### Relations
- [[content/foundational/independent set.md]] — Uses the independence number $\alpha(G)$.
- [[separating set, k-connectivity]] — Uses connectivity $\kappa(G)$.
- [[content/theorems, lemma/theorem - Menger / Menger-type equivalences.md]] — The proof employs Menger‑style arguments to produce disjoint paths used to extend cycles.

Source: Notes by date/11-3-25.md
