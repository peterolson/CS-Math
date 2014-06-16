# Cantor's Theorem
## Prerequisites

 - [Cardinality of Infinite Sets](?Set_Theory/Cardinality_Infinite)
 - [Subsets and Power Sets](?Set_Theory/Powerset)
 
## Theorem statement

Let $S$ be a set. $|S|<|\mathcal P(S)|$.

That is, there is no surjective function from $S$ to $\mathcal P(S)$.

## Proof

Suppose for a contradiction that there is a surjective function $f:S\to\mathcal P(S)$.

Consider the set $T=\\{x\in S : x\notin f(x)\\}$.

Since $T\subseteq S$, we know by definintion of power set that $T\in\mathcal P(S)$. 

Since $f$ is surjective, $T=f(a)$ for some $a\in S$.

Either $a\in T$ or $a\notin T$.

 - If $a\in T$, then $a\notin f(a)$. Since $T=f(a)$, we get $a\notin T$, which is a contradiction.
 - If $a\notin T$, then $a\in f(a)$. Since $T=f(a)$, we get $a\in T$, which is a contradiction.
 
By contradiction, our initial assumption that a surjective function $f:S\to\mathcal P(S)$ exists is false.