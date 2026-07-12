



- 1,2,3 done alr


















# Problem 3
Let $U$ be a set and $V\subseteq U$. Define $\mathcal{P}( U )\rightarrow \mathcal{P}( V )$ by $f( A )=A\cap V$.
1. Show that $f$ is a surjective homomorphsim (of rings.) You may use Venn diagrams to argue that it is a homomorphism.
	1. ==Proof.== 
		1. $f$ is a homomorphism if it satisfies the homomorphic property: 
			1. $f( a )f( b )=f( ab )$
		2. Considering $\mathcal{P}( U )$ is a ring, such operations are:
			1. *symmetric difference:* $A + B=( A / B )\cup ( B / A )$
			2. *intersection*: $AB=A\cap B$
		3. Drawing a Venn diagram, we see that both the operations satisfy the homomorphic property.
		4. We also show that $f$ is surjective:
			1. $f$ is surjective if $\forall A\in \mathcal{P}( V )$ $\exists B\in \mathcal{P}( V )$ such that $f( A )=A\cap V$.
		

	3. Recall the definition of a *quotient ring*:
		1. Let $A$ be a ring and $J$ an ideal  of $A$. Define their quotient ring to be $$A / J =\left\{ J + x\ |\ x\in  A \right\}$$... a ring of quotient groups closed under the operations of *addition*: $( J+x )+( J+y )=J+( x+y )$... and *multiplication*: $( J+x )( J+y )=J+xy$.
2. What is its kernel?
	1. Recall the definition of kernel: if 

4. What can you conclude using the FHT?