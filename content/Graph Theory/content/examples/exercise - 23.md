> [!example]
> ### Exercise 23. Let $G$ be a graph with at least four vertices. Prove that the following are equivalent:
> (i) $G$ is 2-connected
> 
> (ii) for every $x \in V(G)$ and every $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2,$ there exists two paths $P$ and $Q$ such that $x$ is an endpoint of $P$ and $Q$ and the other endpoint of $P$ and $Q$ is in $Y$ and $(V(P) \setminus \{x\}) \cap (V(Q) \setminus \{x\}) = \emptyset$
> 
> (iii) for all disjoint $X, Y \subseteq V(G)$ with $|X|, |Y| \ge 2,$ there are two disjoint paths $P$ and $Q$ such that $P$ and $Q$ each have one endpoint in $X$ and the other in $Y.$
> 
> (Hint: As I mentioned in class, the Expansion Lemma will be helpful in proving (i) $\Rightarrow$ (ii) $\Rightarrow$ (iii))~~~ad-proof

(i) $\Rightarrow$ (ii) Suppose $G$ is 2-connected. Let $x \in V(G)$ and $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2.$ Add a vertex $y'$ such that $y'$ has 2 neighbors in $Y$ to get a graph $G'$ which is still 2-connected by the Expansion Lemma. By Theorem 4.2.2, $G'$ has two internally disjoint $x, y'$-paths $P', Q.'$ Now $P = P' - y'$ and $Q = Q' - y'$ are the paths we are looking for.

(i) $\Leftarrow$ (ii) Suppose that for every $x \in V(G)$ and every $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2,$ there exists two $x, Y$-paths $P$ and $Q$ such that $(V(P) \setminus \{x\}) \cap (V(Q) \setminus \{x\}) = \emptyset.$ Suppose for contradiction $\kappa(G) \le 1.$ If $\kappa(G) = 0,$ let $\{x, y, y'\}$ be chosen so that $x$ is in a different component from $y$ and $y'.$ Now let $Y = \{y, y'\}.$ Using the property of $G,$ there is a path from $x$ to $y$ and $y',$ a contradiction. So suppose $\kappa(G) = 1$ and let $y$ be a cut vertex of $G.$ Let $x$ and $y'$ be chosen so that $x$ is in a different component of $G-y$ from $y'.$ Now let $Y = \{y, y'\}.$ So there is an $x, y$-path $P$ and $x, y'$-path $Q$ such that $P-x$ is disjoint from $Q-x,$ but every path from $x$ to $y'$ goes through $y,$ a contradiction.

(ii) $\Rightarrow$ (iii) Suppose that for every $x \in V(G)$ and every $Y \subseteq V(G) \setminus \{x\}$ with $|Y| \ge 2,$ there exists two $x, Y$-paths $P$ and $Q$ such that $(V(P) \setminus \{x\}) \cap (V(Q) \setminus \{x\}) = \emptyset.$ Since we know that (i) $\Leftrightarrow$ (ii), we have that $G$ is 2-connected. Let $X, Y \subseteq V(G)$ be disjoint with $|X|, |Y| \ge 2.$ Add a vertex $x'$ such that $x'$ has two neighbors in $X.$ By the Expansion Lemma, $G'$ is still 2-connected and thus (ii) holds for $G'.$ So there are two $x', Y$-paths $P'$ and $Q'$ such that $P'-x'$ is disjoint from $Q'-x'$ and thus $P = P' - x'$ and $Q = Q' - y'$ are two disjoint $X, Y$-paths.

(iii) $\Rightarrow$ (i) Suppose for contradiction $\kappa(G) \le 1.$ If $\kappa(G) = 0,$ let $\{x, x', y, y'\}$ be chosen so that $x'$ is in a different component from $y$ and $y'.$ Now let $X = \{x, x'\}$ and $Y = \{y, y'\}.$ Using the property there are two completely disjoint $X, Y$-paths, there is a path from $x'$ to $y$ or $y',$ a contradiction. So suppose $\kappa(G) = 1$ and let $x$ be a cut vertex of $G.$ Let $x', y, y'$ be chosen so that $x'$ is in a different component of $G-x$ from $y$ and $y'.$ Now let $X = \{x, x'\}$ and $Y = \{y, y'\}.$ The property there are two completely disjoint $X, Y$-paths contradicts the fact that every path from $x'$ to $Y$ must contain the cut vertex $x.$ So $G$ is 2-connected. $\square$


Relations
- [[theorem - 2-connected via internally disjoint paths]]
- [[lemma - maximal-path spanning cycle (Lemma 0.2)]]
- [[theorem - 2-connected via internally disjoint paths]]
