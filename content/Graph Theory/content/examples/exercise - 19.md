> [!example]
> ### Exercise 19.
> Let $G$ be a graph such that $\beta(G) = 2\alpha'(G).$
> 
> (i) Prove that $\max\{o(G-S) - |S| : S \subseteq V(G)\} = \alpha(G).$ (Hint: Lemma 3.1.21 says something about $n - \alpha(G)$ and Corollary 3.3.7 says something about $n - \max\{o(G-S) - |S| : S \subseteq V(G)\}.)$
> 
> (ii) Prove that every component of $G$ is a clique with an odd number of vertices. (Hint: Begin by choosing a set $S$ achieving the maximum in part (i).)~~~ad-proof
By Lemma 3.1.21 and the assumption, we have $n - \alpha(G) = \beta(G) = 2\alpha'(G).$ So by Corollary 3.3.7, we have $n - \alpha(G) = 2\alpha'(G) = n - \max\{o(G-S) - |S| : S \subseteq V(G)\}$ and thus $\max\{o(G-S) - |S| : S \subseteq V(G)\} = \alpha(G).$ Let $S$ be a set achieving the maximum; i.e. let $S \subseteq V(G)$ such that $o(G-S) - |S| = \alpha(G).$

- If $|S| \ge 1,$ then $o(G-S) \ge \alpha(G) + |S| > \alpha(G),$ but choosing exactly one vertex from each odd component of $G-S$ gives us an independent set in $G-S$ (which is an independent set in $G$) with more than $\alpha(G)$ vertices, a contradiction.
    
- So suppose $S = \emptyset.$ In this case we have $o(G) = \alpha(G),$ which also implies that $G$ has no even components because again, this would give a larger independent set. * So every component of $G$ is odd. Furthermore, every component of $G$ is a clique, because otherwise we would have two non-adjacent vertices in some component of $G$ which would again give us an independent set of order larger than $\alpha(G)$ which is impossible.
    
- Thus every component of $G$ is an odd clique. $\square$


Relations
- [[content/theorems, lemma/corollary - number of vertices saturated by maximum matching (3.3.7).md]]
- [[content/foundational/independent set.md]]
- [[content/foundational/odd components.md]]
