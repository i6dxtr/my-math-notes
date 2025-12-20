> [!example]
> ### Exercise 17.
> (i) We proved part of Theorem 3.1.22 by showing that $\beta'(G) \le n - \alpha'(G).$ Now finish the proof by proving that $\beta'(G) \ge n - \alpha'(G).$ (Hint: Start by letting $L$ be a minimum edge cover and then apply the Star Forest Lemma.)
> 
> (ii) Prove that if $G$ is a bipartite graph with no isolated vertices, then $\alpha(G) = \beta'(G).$ (Hint: What is implied by Lemma 3.1.21 and Theorem 3.1.22?)~~~ad-proof
**Proof of i.**

Let $M$ be a maximum matching in $G.$ Since $M$ is maximum, every other edge has at least one endpoint in $M$ and since $G$ has no isolated vertices, every vertex not incident with an edge in $M$ is incident with some edge having exactly one endpoint in $M.$ Thus there exists an edge cover of size $|M| + (n - 2|M|) = n - |M| = n - \alpha'(G).$ i.e. $\beta'(G) \le n - \alpha'(G).$

Next we show that $\beta'(G) \ge n - \alpha'(G).$ Let $L$ be a minimum edge cover of $G.$ By the Star Forest Lemma, every component of $L$ is a star. Say that $L$ has $k$ components. So there is a matching with $k$ edges (one from each component). There are $k$ center vertices and thus $n-k$ leaf vertices, so the number of edges in $L$ is $n-k.$ Thus $|L| = n-k = n - |M|$ and thus $\beta'(G) = n - |M| \ge n - \alpha'(G).$ Thus $\alpha'(G) + \beta'(G) = n.$ $\square$

**Proof of ii.**

By Lemma 3.1.21 and Theorem 3.1.22 we have

$$\alpha(G) + \beta(G) = n = \alpha'(G) + \beta'(G)$$

and since $G$ is bipartite we have $\alpha'(G) = \beta(G).$ Together, this implies that $\alpha(G) = \beta'(G).$ $\square$

Relations
- [[content/theorems, lemma/lemma - star forest.md]]
- [[content/theorems, lemma/theorem - matching + edge cover = n.md]]
- [[content/foundational/edge cover.md]]
