1. Let $G$ be the subset of $S_{4}$ consisting of the permutations:
	$$
	\begin{align}
	\epsilon=
	\begin{pmatrix}
	1 & 2 & 3 & 4 \\
	1 & 2 & 3 & 4
	\end{pmatrix}&& f=
	\begin{pmatrix}
	1 & 2 & 3 & 4 \\
	2 & 1 & 4 & 3
	\end{pmatrix} \\
	g=
	\begin{pmatrix}
	1 & 2 & 3 & 4 \\
	3 & 4 & 1 & 2
	\end{pmatrix}&&h=
	\begin{pmatrix}
	1 & 2 & 3 & 4 \\
	4 & 3 & 2 & 1
	\end{pmatrix}
	\end{align}
	$$
	... Show that $G$ is a group of permutations, and write its table.
#### Soln
- Making Table:
$$
\left(\begin{array}{c|cccc}
  \underline\circ&\underline\epsilon&\underline g&\underline f&\underline h \\
\underline\epsilon &\epsilon&g&f&h \\
\underline g&g&\epsilon&h&f \\
\underline f&f&h&\epsilon&g \\
\underline h&h&f&g&\epsilon \\
\end{array}\right)
$$
- $G$ contains subgroups, each with a one-to-one correspondence under the composition operation, and all contain only the elements $\left\{ 1,2,3,4 \right\}$. SO it is a group of permutations, by definition of permutation.



Make a table for the group $G=\left\{ e,f,g,h \right\}$ where $e(x)=x,\ f(x)=-x,\ g(x)=1x,\ h(x)=-1x$.




2. Make a table for the group $G=\left\{ e,f,g,h \right\}$ where $e(x)=x,\ f(x)=-x,\ g(x)=1x,\ h(x)=-1x$. Then say what the inverse of each element is.
	- These are functions from the set of all nonzero real numbers to itself.





1. In $D_{4}$ let $r$ be a rotation by $90$ degrees and let $s$ be a reflection. Find positive integers $m,n,p$ such that $r^{m}=e$, $s^{n}=e$, and $sr=r^{P}s$







1. In dihedral groups: do rotations commute with rotations? Do rotations commute with reflections? Do reflections commute with reflections? If yes, briefly explain why. If not, give a counterexample.

2. Fill in each blank with the word "rotation" or "reflection" to describe how rotations and reflections interact in dihedral groups.
	1. rotation $\circ$ rotation
	2. rotation $\circ$ reflection $=$
	3. reflection $\circ$ rotation $=$
	4. reflection $\circ$ reflection $=$
	

6.  In this problem we consider the group $D_{5}$ again, but this time we number the vertices of the pentagon $\left\{ 0,1,2,3,4 \right\}$ instead of $\left\{ 1,2,3,4,5 \right\}$.  This is convenient for doing modular arithmetic on the vertices.  For each of the following functions, write it in two-line notation as a permutation of ${0,1,2,3,4}$ and then describe it geometrically as an element of $D_{5}$:  Is it a rotation?  If so, by what angle?  Is it a reflection?  If so, across what axis? 
7. 1. The function $f:\left\{ 0,1,2,3,4 \right\}\rightarrow \left\{ 0,1,2,3,4 \right\}$ defined by $f(n)=n+2\text{ mod }5$
8. The function $g:\left\{ 0,1,2,3,4 \right\}\rightarrow\left\{ 0,1,2,3,4 \right\}$ defined by $g(n)=-n\text{ mod }5$
9. The function $k:\left\{ 0,1,2,3,4 \right\}\rightarrow\left\{ 0,1,2,3,4 \right\}$ defined by unknown node type $\text{brk}(n)=2-n\text{mod }$

### Exam
#### P1
1. Which one of the following is NOT an operation on the set $S=\left\{ \frac{m}{2^{n}}\ |\ m\in \mathbb{Z} \text{ and }n\in \mathbb{N}\right\}$?
- $+$
- $-$
- $\cdot$
- $\big /$
Explain why it is not an operation on $S$.

2. Consider the operation $*$ on $\mathbb{R}$ defined by $a*b=\sqrt{a^{2}+b^{2}}$. 
	- Is it commutative? Explain
	- Is it associative? Explain


3. The operation $*$ on $\mathbb{R}$ defined by $a*b=\frac{ab}{2}$ has an identity element. What is it? Explain

4. Make a table for the group $(\left\{ 1,5,7,11 \right\}, \cdot_{12})$, then write what the inverse of each element is


#### P2
1. Letting $a,b,c,d,r,s,x$ be group elements, solve the equation $a b x c d=r s$ for $x$. Show work.
2. Letting $a,x$ be group elements, which one of the following must be equal to $e$?
	1. $axa^{-1}x^{-1}$
	2. $axx^{-1}a^{-1}$
3. Give an example of a group $G$ and elements $a,b\in G$ such that $a^{2}=e$ and $b^{2}=e$ but $(ab)^{2}\neq e$. Show a calculation of $(ab)^{2}$.
4. For each of the following sets, determine whether or not it is a group with the operation of multiplication. If not, explain.
	1. $\mathbb{Z}^{+}$
	2. $\mathbb{Q}^{*}$
	3. $\mathbb{R}$
	4. $\left\{ -1,1 \right\}$

#### P5b
1. Choose two different reflections $f$ and $g$ in $D_{5}$.
	1. Describe them geometrically (showing axis of reflection) and write them in two-line notation.
	2. Compute $fg$ and $gf$ in two-line notation
	3. Describe $fg$ and $gf$ geometrically
2. Which group has elements, $A_{6}$ or $D_{6}$? Explain