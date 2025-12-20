> [!lemma]
> ### Parity lemma (Tutte)
> Let $G$ be a graph on $n$ vertices. For every $S\subseteq V(G)$ the integers $n$ and $o\bigl(G-S\bigr)-\lvert S\rvert$ have the same parity; equivalently
> $$
> o\bigl(G-S\bigr)-\lvert S\rvert \equiv n \pmod{2}.
> $$
> [!proof]
> Write $V(G)=S\sqcup T$ where $T=V(G)\setminus S$. Each component of $G-S$ has some number of vertices; summing the orders of the components of $G-S$ equals $|T|=n-|S|$. Let the odd components contribute an odd number each and even components contribute even numbers; hence
> $$
> |T|\equiv o(G-S) \pmod{2}.
> $$
> Therefore
> $$
> n-|S|\equiv o(G-S)\pmod{2},
> $$
> so rearranging gives $o(G-S)-|S|\equiv n\pmod{2}$, as claimed.
### Relations
- [[content/foundational/odd components.md]] — Uses the notation $o(\cdot)$ and is a direct parity property of component counts.
- [[content/theorems, lemma/theorem - Tutte's theorem.md]] — Parity lemma is used in arguments within the proof of Tutte's theorem (e.g. when adding vertices to adjust parity).
- [[content/foundational/order, size.md]] — Relates parity of vertex counts to order/size considerations.

Source: Notes by date/10-17-25.md
