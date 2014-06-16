# Cardinality of Infinite Sets

<iframe width="560" height="315" src="//www.youtube.com/embed/tmyL-AOfIWY?rel=0" frameborder="0" allowfullscreen></iframe>

## Prerequisites

 - [Cardinality of Finite Sets](?Set_Theory/Cardinality_Finite)
 
## Basic definition

Unlike finite sets, it is impossible to count the number of elements in an infinite set: you would never stop counting!

However, the methods of [comparing comparing cardinalities using functions](?Cardinality_Finite#Comparison_of_cardinalities_using_functions) can be applied to infinite sets as well as finite sets.

We will compare everything to the set of natural numbers, i.e. the set of non-negative integers $\\{0,1,2,\ldots\\}$. The set of natural numbers is commonly written with the symbol $\mathbb{N}$.

The cardinality of the natural numbers $|\mathbb{N}|$ is commonly denoted by the symbol $\aleph_0$ ("aleph naught").

Let $X$ be a set.

 - If $|X|<\aleph_0$, then $X$ is called a **finite set**.
 - If $|X|=\aleph_0$, then $X$ is called a **countably infinite set**.
 - If $|X|>\aleph_0$, then $X$ is called an **uncountably infinite set**.
 
### Example of a finite set

The set $X=\\{5,6,7\\}$ is finite, because there is no surjective mapping from $X$ to $\mathbb{N}$: once you choose natural numbers to map $5$, $6$, and $7$ to, there are still lots of (i.e. infinitely many) natural numbers that have not been mapped to.

### Examples of countably infinite sets

We can show that a set $X$ is countably infinite by showing a bijection between $X$ and $\mathbb{N}$.

#### Example: removing or adding finitely many elements to $\mathbb{N}$

Adding or removing finitely many elements to $\mathbb{N}$ preserves its cardinality.

Consider the natural numbers with the first $100$ elements removed, i.e. the set $X=\\{100,101,102,\ldots\\}$.

The function $f:\mathbb N\to X$ defined by $f(n)=n+100$ is a bijection, so $|X|=|\mathbb{N}|=\aleph_0$.

Similarly, consider the natural numbers with $100$ elements added to it, e.g. the set $Y=\\{-100,-99,-98,\ldots\\}$.

The function $g:\mathbb N\to Y$ defined by $g(n)=n-100$ is a bijection, so $|Y|=|\mathbb{N}|=\aleph_0$.

#### Example: removing infinitely many elements from $\mathbb{N}$

Perhaps surprisingly, one can remove infinitely many elements from $\mathbb{N}$ while preserving the cardinality.

Consider the even natural numbers, i.e. the set $X=\\{0,2,4,6,8,\ldots\\}$.

The function $f:\mathbb N \to X$ defined by $f(n)=2n$ is a bijection, so $|X|=\aleph_0$.

#### Example: finite strings over an alphabet

Let $X$ be the set of finite strings over the alphabet $\\{a,b,c,d,e,f,\ldots,x,y,z\\}$.

Enumerate the elements of $X$ in lexicographic order: $\\{a,b,c,\ldots,z,aa,ab,\ldots,zy,zz,aaa,aab,\ldots,zzy,zzz,aaaa\ldots\\}$.

Define the function $f:\mathbb N\to X$ by assigning the natural numbers to the elements of $X$ in lexicographic order, i.e. $$f(0)=a,f(1)=b,\ldots,f(25)=z,f(26)=aa,\ldots$$ and so on. Since $f$ is a bijection, $|X|=\aleph_0$.

### Examples of a uncountably infinite sets

We can show that a set $X$ is uncountably infinite by showing that $|X|>\mathbb N$, that is, there is no surjective function from $\mathbb N$ to $X$.

#### Example: infinite sequences of $1$s and $0$s

Let $X$ be the set of infinite sequences of $1$s and $0$s. Suppose for a contradiction that there was a surjective map $f:\mathbb N \to X$. Then we could enumerate the elements of $X$, e.g.

$$f(0)=(0,0,0,0,0,0,0,0,\ldots)$$
$$f(1)=(1,1,1,1,1,1,1,1,\ldots)$$
$$f(2)=(1,0,1,0,1,0,1,0,\ldots)$$
$$f(3)=(0,1,0,1,0,1,0,1,\ldots)$$
$$f(4)=(1,1,0,1,1,0,1,1,\ldots)$$
$$f(5)=(0,0,1,0,0,1,0,0,\ldots)$$
$$f(6)=(1,0,0,1,0,0,1,0,\ldots)$$
$$f(7)=(1,0,0,0,0,0,0,0,\ldots)$$
$$\vdots$$

Now create the sequence $s$ formed by taking the first element of $f(0)$, the second element of $f(1)$, and so on (i.e. the elements on the diagonal). Then consider the sequence $s'$ by taking the inverse of every element in $s$ (i.e. change $0$ to $1$ and vice versa).

$$f(0)=(\underline 0,0,0,0,0,0,0,0,\ldots)$$
$$f(1)=(1,\underline 1,1,1,1,1,1,1,\ldots)$$
$$f(2)=(1,0,\underline 1,0,1,0,1,0,\ldots)$$
$$f(3)=(0,1,0,\underline 1,0,1,0,1,\ldots)$$
$$f(4)=(1,1,0,1,\underline 1,0,1,1,\ldots)$$
$$f(5)=(0,0,1,0,0,\underline 1,0,0,\ldots)$$
$$f(6)=(1,0,0,1,0,0,\underline 1,0,\ldots)$$
$$f(7)=(1,0,0,0,0,0,0,\underline 0,\ldots)$$
$$\vdots$$
$$s=(0,1,1,1,1,1,1,0,\ldots)$$
$$s'=(1,0,0,0,0,0,0,1,\ldots)$$

On one hand, $s'$ is an infinite sequence of $1$s and $0$s, $s'\in X$. On the other hand, we defined $s'$ in such a way that it is different than every element of $X$ in at least one place, so $s'\notin X$. This is a contradiction, so there cannot be a surjective function from $\mathbb N$ to $X$.

#### Example: the powerset of natural numbers

Consider the powerset of natural numbers, $\mathcal P (\mathbb N)$. We will show that $|\mathcal P (\mathbb N)|=|X|$, where $X$ is the set of infinite sequences of $1$s and $0$s.

Define $f:\mathcal P (\mathbb N)\to X$ to be the function, which, given a subset of natural numbers $S$, returns the sequence formed by taking the sequence of all zeros $(0,0,0,0\ldots)$ and changing the $s+1$th element to $1$ for each $s\in S$. For example,
$$f(\emptyset)=(0,0,0,0,0,0,0,0,0,0,\ldots)$$
$$f(\\{0,1,2\\})=(1,1,1,0,0,0,0,0,0,0,\ldots)$$
$$f(\\{0,2,4,6,\ldots\\})=(1,0,1,0,1,0,1,0,1,0,\ldots)$$
Since $f$ is a bijection, $|\mathcal P (\mathbb N)|=|X|>|\mathbb N|$