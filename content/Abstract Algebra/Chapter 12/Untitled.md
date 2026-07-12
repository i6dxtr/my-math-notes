
## Set Partitions
- separating a set into distinct parts
- two sets $A_{i}, A_{j}$ are *disjoint* if they have no elements in common
	- if they are each a subset of a different set, they are partitions of the set

> [!definition]
> A **partition** $\left\{ A_{i}:i\in I \right\}$ of nonempty subsets of $A$ which are mutually disjoint and whose union is all of $A$.

> [!remark]
> By a **partition** of a set $A$ we mean a family $\left\{ A_{i}:i\in I \right\}$ of nonempty subsets of $A$ such that:
> 1. If any two classes $A_{i}$ and $A_{j}$ have a common element $x$ (non-disjoint) then $A_{i}=A_{j}$
> 2. Every element of $x$ of $A$ lies in one of the classes

- A *relation* on a set $A$ is T/F for each $\left( x,y \right)\in A$
	- *e.g.* $x<y$, $x=y$, $x$ parallel to $y$, etc.
	- denoted $\sim$
- An *equivalence relation* on $A$ is a special relation:

> [!definition]
> An **equivalence relation** on $A$ has the following properties:
> 1. *Reflexivity:* $x\sim x\ \ \forall x\in A$
> 2. *Symmetry:* $x\sim y\longrightarrow y\sim x$
> 3. *Transitive:* $x\sim y\ \wedge\ y\sim z\longrightarrow x\sim z$

- most obvious being equality
- may arise out of partitions
	- $\left\{ A_{i}:i\in I \right\}$ partitions $A$ implies $x\sim y \Longleftrightarrow x,y$ in same partition
		- aka, equivalency if members of same class
		- *e.g.* $x\sim x$ since obv in same class
		- leads to definition

> [!definition]
> Let $\sim$ be an equivalence relation on $A$ and $x$ an element of $A$. the set of all the elements equivalent to $x$ is called the *equivalence* class of $x$, denoted $\left[ x \right]$. Symbolically, $$\left[ x \right]=\left\{ y\in  A: y\sim x \right\}$$

> [!corollary] Lemma.
> If two elements are equivalent, they have the same equivalence class.$$x\sim y\longrightarrow\left[ x \right]=\left[ y \right]$$

- *e.g.* coins in a jar = $A$
	- $x_{1}$ a nickel in a jar
	- if $x_{1}\sim x_{2}$ then $x_{1}, x_{2}$ have same value'
	- thus $x_{2}$ is a nickel
		- $\left[ x \right]=$ the set of all nickels

> [!theorem]
> If $\sim$ is an equivalence relation on $A$, the family of all the equivalence classes, that is, $\left\{ \left[ x \right]:x\in A\right\}$, is a partition of $A$.

- each equivalence class family forms a partition of its set
- *pf.* *1.* show it's nonempty. *2.* show any two classes are disjoint. *3.* if $\left[ x \right]=\left[ y \right]$ then $x=y$ (common element), shown thru symmetry, transivity. *4.* $\forall a\in A$, there exists $\left[ a \right]\in A$
- *partition determined by equivalence relation*: the partition formed when $\sim$ is equiv. relation on $A$ & $A$ is partitioned into equiv. classes
- ==remark==. partitions and equivalence classes are twin aspects of the same structure on sets
	- $\exists x,y\in A$, $x$ equiv. to $y$ $\Longleftrightarrow$ lie in same class of partition
	- can also def partition on $A$: $x\equiv y\longrightarrow x\in \left[ f \right], y\in \left[ f \right]$
- there are several ways to partition sets, and all are defined by *exactly one specific equivalence relation* on the set
	- *e.g.* $A=\left\{ a,b,c \right\}$ means 5 ways of partitioning, exactly ![[Pasted image 20241023204402.png]]