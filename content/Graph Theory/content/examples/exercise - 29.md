> [!example]
> ### Exercise 29.
> (i) If $G$ is a graph with $m$ edges, then $\chi(G) < 1 + \sqrt{2m}.$ (Hint: Use Lemma Z)
> 
> (ii) Let $G$ be a graph on $n$ vertices and let $k, \ell$ be positive integers such that $n \le k\ell.$ Prove that if $G$ is triangle-free (i.e. $\omega(G) \le 2$), then $\chi(G) \le k + \ell - 1.$
> 
> (Hint 1: Induction on $\ell$)
> 
> (Hint 2: What does being triangle-free tell us about the neighborhood of every vertex? In particular, what happens if $G$ has a vertex of degree at least $k$?)~~~ad-proof
(i) By Lemma Z we have $m \ge \binom{\chi(G)}{2} > \frac{(\chi(G)-1)^2}{2}$ and thus $\chi(G) < 1 + \sqrt{2m}.$

(ii) First suppose $\ell = 1.$ We have $\chi(G) \le n \le k.$

So let $\ell \ge 2,$ let $G$ be a graph with $n \le k\ell$ vertices, and suppose the result holds for triangle-free graphs with at most $k(\ell - 1)$ vertices.

If $\Delta(G) \le k - 1,$ then $\chi(G) \le k \le k + \ell - 1$ as desired, so suppose $G$ contains a vertex of degree at least $k.$ Since $G$ is triangle-free, this gives us an independent set $A$ with at least $k$ vertices. Since $G - A$ is triangle-free and has at most $k\ell - k = k(\ell - 1)$ vertices, $\chi(G - A) \le k + (\ell - 1) - 1.$ Using a new color on $A$ gives us a $k + \ell - 1$ coloring of $G.$ $\square$


Relations
- [[example - chromatic bound by edges]]
- [[corollary - Erdös-Szekeres subsequence]]
- [[theorem - Mycielski construction]]
