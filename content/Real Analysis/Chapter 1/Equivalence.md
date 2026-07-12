#ch1 
### Outline/Relations
- [[sets|Sets]]


### Definition
> [!definition]
> Two sets $A$ and $B$ are **equivalent** ($A \sim B$) if there exists a one-to-one [[function]] from $A$ onto $B$.

> [!corollary]
> Equivalence of sets satisfies the following:
> 1. **Reflexive**: $A\sim A$
> 2. **Symmetric**: $A\sim B \longrightarrow B\sim A$
> 3. **Transitive**: $A\sim B \wedge B\sim C \longrightarrow A\sim C$
#### Examples
> [!example]
> $$
> \begin{align} A&= \left\{ 1,2,3,4 \right\} \\ B&= \left\{ 100, 101, 200, 500 \right\} \end{align}
> $$
> - $1\rightarrow 500$, $2\rightarrow 101$, $3 \rightarrow 100$, $4 \rightarrow 200$
> - so $A\sim B$

> [!example]
> $$
> \begin{align} A&= \mathbb{N} \\ B&= \left\{ 2k: k\in  \mathbb{N} \right\} \end{align}
> $$
> - A is equivalent to $B$ ($A\sim B$)
> 	- $A\longrightarrow B$
> 	- $k \longmapsto 2k$