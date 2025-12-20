> [!example]
> ### Exercise 26. _For all graphs $G$ and all $xy \in E(G),$ $\kappa(G) \ge \kappa(G-xy) \ge \kappa(G) - 1.$_
> **Lemma 4.2.20.** _For all graphs $G$ and all $xy \in E(G),$ $\kappa(G) \ge \kappa(G-xy) \ge \kappa(G)-1.$_~~~ad-proof
Let $xy \in E(G).$ If $S$ is a vertex cut of $G,$ then $S$ is a vertex cut of $G-xy.$ So $\kappa(G-xy) \le \kappa(G).$

Let $G' = G-xy$ and let $S'$ be a minimum vertex cut of $G'$ (which exists since $G'$ cannot be complete).

- If $x \in S'$ or $y \in S',$ then we have $G' - S' = G - S',$ and thus $S'$ is a vertex cut of $G$ which implies $\kappa(G') = |S'| \ge \kappa(G).$
    
- So suppose $x, y \notin S'.$
    
    - If $(G' - S') - x$ has more than one component, then $S' \cup \{x\}$ is a vertex cut of $G$ which implies $|S'| + 1 = |S' \cup \{x\}| \ge \kappa(G)$ and thus $\kappa(G') = |S'| \ge \kappa(G) - 1.$
        
    - Likewise if $(G' - S') - y$ has more than one component.
        
- So the only possibility is that $G' - S'$ has two components, each consisting of a single vertex. But then $\kappa(G') = |S'| = n-2 = n-1-1 \ge \kappa(G) - 1.$ $\square$


Relations
- [[separating set, connectivity]]
- [[lemma - connectivity equivalence relation]]
- [[lemma - minimal disconnecting set is edge cut]]
