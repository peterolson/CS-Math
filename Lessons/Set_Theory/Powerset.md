# Subsets and Power Sets

<iframe width="560" height="315" src="//www.youtube.com/embed/dJffn298coo?rel=0" frameborder="0" allowfullscreen></iframe>

## Prerequisites

 - [Sets; intersection and union of sets](https://www.khanacademy.org/math/probability/independent-dependent-probability/basic_set_operations/v/intersection-and-union-of-sets)
 
## Basic definition

Let $X$ and $Y$ be sets.

### Definition of subset

$X$ is called a *subset* of $Y$, denoted by $X\subseteq Y$, if every element in $X$ is also in $Y$.

$X$ is called a *proper subset* of $Y$, denoted by $X\subsetneq Y$, if $X\subseteq Y$ and there exists an element in $Y$ that is not in $X$.

#### Example

Let $X=\\{2,4,6\\}$ and $Y=\\{2,4,6,8\\}$. Every element in $X$ is also in $Y$, so $X\subseteq Y$. Also $X\subsetneq Y$, since $8\in Y$ but $8\notin X$.

#### Example

Let $X=\\{1,2,3\\}$ and $Y=\\{1,2,3\\}$. Then $X\subseteq Y$ and $Y\subseteq X$ because every element in one set is also in the other. In this case, we say $X=Y$.

#### Example

Let $X=\emptyset$. Since there are no elements in $X$, it is [vacuously true](http://en.wikipedia.org/wiki/Vacuous_truth) that every element in $X$ is also in $Y$, no matter what set $Y$ is. Thus, $X\subseteq Y$.

### Definition of power set

The power set of a set $X$, denoted by $\mathcal P(X)$ or $2^X$, is the set of all subsets of $X$.

#### Example

Let $X=\\{1,2,3\\}$. Then $\mathcal P(X)=\\{\emptyset, \\{1\\}, \\{2\\}, \\{3\\}, \\{1,2\\}, \\{1,3\\}, \\{2,3\\}, \\{1,2,3\\}\\}$.

#### Example

Let $X=\emptyset$. Then $\mathcal P(X) = \\{\emptyset\\}$.

#### Size of the power set

If $X$ has $n$ elements, how many elements does $\mathcal P(X)$ have?

A subset of $X$ is determined by which elements of $X$ are included and which are excluded. For each element in $X$, you have two options: you can either choose to include it or to not include it. All of these options can be made independently of each other, so there are $2^n$ ways to choose a subset of $X$. This is the reason behind the notation $2^X$ for a power set.