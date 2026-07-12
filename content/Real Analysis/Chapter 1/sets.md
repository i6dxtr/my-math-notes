#ch1 
- most of what you already know in terms of definitions
### Outline
- **Notation**
- **Properties**
- **Cartesian Product and Power Sets**
- **[[cardinality|Cardinality/Countability]]**
- **[[Equivalence]]**
- [[Index Family of Subsets|Index Family of Subsets]]
### notation review
- brief re-introduction into basic set notations ($\mathbb{N}, \mathbb{R}, ...$) and operations
	- remember that the *complement* is expressed as $x\in A / B$
	- moreover, if $B\subseteq A$ then $A / B= B^{c}$
### Properties of sets
> [!theorem]
> If $A,B,C$ are sets, then they must have the following properties:
> 1. $A\cap( B\cup C )=( A\cap B )\cup ( A \cap C )$
> 2. $A\cup ( B\cap C )= ( A\cup B )\cap ( A \cup C )$
> 3. $C / ( A \cup B )=( C / A )\cap ( C / B )$
> 4. $C / ( A \cap B )=( C / A )\cup ( C / B )$

> [!proof]
> ##### Proving 4.
> - $C / ( A \cap B )\subset( C / A )\cup ( C / B )$
> 	- Let $x\in C / ( A \cap B )$, then:
> 		- $x\in C$ *and* $x\not\in( A \cup B )$
> 		- $x\notin A$ *or* $x\not\in B$
> 		- $x\in C$ *and* $c\in C / A$ *or* $x\in C / B$
> 		- $( x\in C$ *and* $x\in C / A)$ *or* $( x\in C$ *and* $x\in A / C)$
> - $x\in ( C / A )\cup ( C / B )$
> 	- Let $y\in ( C / A ) \cup ( C / B )$, then:
> 		- $y\in ( C / A )$ *or* $( y\in C / B )$
> 		- $y\notin A$ *or* $y\notin B$
> 		- $y\notin ( A \cup C )$
> 		- so $y\in C / ( A \cap B )$.
### Power set and Cartesian product
> [!definition]
> For a given set $A$, the **power set** $\mathcal{P}( A )$ is the collection of all subsets of $A$.

> [!definition]
> The **Cartesian product** of two sets $A$ and  $B$ is the set of all $a\in A$, $b\in B$ such that:$$A  \times  B=\left\{  ( a,b ): a\in  A \wedge b\in  B \right\}$$