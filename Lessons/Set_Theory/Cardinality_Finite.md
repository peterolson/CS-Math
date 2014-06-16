# Cardinality of Finite Sets

<iframe width="560" height="315" src="//www.youtube.com/embed/UEOeHUmvu7A?rel=0" frameborder="0" allowfullscreen></iframe>

## Prerequisites

 - [Sets; intersection and union of sets](https://www.khanacademy.org/math/probability/independent-dependent-probability/basic_set_operations/v/intersection-and-union-of-sets)
 - [Surjective (onto) and injective (one-to-one) functions](https://www.khanacademy.org/math/linear-algebra/matrix_transformations/inverse_transformations/v/surjective--onto--and-injective--one-to-one--functions)
 
## Basic definition

For finite sets, **cardinality** is just a fancy word for "size" or "number of elements". As an example, the set $\\{1,2,3\\}$ has 3 elements, so it has a cardinality of 3.

The cardinality of a set $S$ can be denoted by $|S|$, $\\#S$, or $\text{card}(S)$. We will use $|S|$ because it is the most common notation.

### Examples

 - $|\emptyset|=0$
 - $|\\{3,5,7,11,13\\}|=5$
 - $|\\{x\\,|\\,x\text{ is a positive even integer and }x\leq100\\}|=50$
 - $|\\{\emptyset,\\{1\\},\\{2\\},\\{1,2\\}\\}|=4$
 
### Comparison of cardinalities using functions

We can compare the cardinality of small sets just by counting their elements. For example, $\\{4,5,6\\}$ has 3 elements and is *larger* (i.e. has a greater cardinality) than $\\{13,27\\}$, which only has 2 elements.

Counting elements directly is not a convenient method for comparing the cardinalities of very large sets. Instead, we will use functions that map between these sets.

For the following definitions, let $X$ and $Y$ be sets.

#### Definition 1.1: $|X|\leq|Y|$ if and only if there is an injective (one-to-one) function from $X$ to $Y$.
#### Definition 1.2: $|X|>|Y|$ if and only if there is no injective function from $X$ to $Y$.

Remember that a function $f:X\to Y$ is called injective, or one-to-one, if for all $x_1,x_2\in X$, we have $f(x_1)\neq f(x_2)$ whenever $x_1\neq x_2$.

##### Example 1.3

The following function $f:\\{9,10\\}\to\\{6,3\\}$

$$f(9)=6$$
$$f(10)=3$$

is injective, since $f(9)\neq f(10)$, and thus we know that that $|\\{9,10\\}|\leq|\\{6,3\\}|$. 

Now consider the sets $\\{9,10,11\\}$ and $\\{6,3\\}$. If we map $9$ to something, and map $10$ to something else, we have no new choices left for $11$.
This means that there is no injective function from $\\{9,10,11\\}$ to $\\{6,3\\}$, so $|\\{9,10,11\\}|>|\\{6,3\\}|$.

##### Example 1.4

A *palindrome* is a sequence that is the same forwards and backwards. Let $P_{5}$ and $P_{6}$ be palindromes of length 5 and 6, respectively, over the alphabet $\\{a,b,c\\}$. (For example, $abcba\in P_5$ and $abccba\in P_6$.)

If $w\in P_5$, then $w$ is of the form $xyz$ where $y$ is a single character, and $z$ is $x$ reversed.

The function $f:P_5\to P_6$ where $xyz\mapsto xyyz$ is injective, so $|P_5|\leq|P_6|$.


#### Definition 2.1: $|X|\geq|Y|$ if and only if there is a surjective (onto) function from $X$ to $Y$.
#### Definition 2.2: $|X|<|Y|$ if and only if there is no surjective function from $X$ to $Y$.
#### Equivalent definition 2: $|X|\geq|Y|$ if and only if $|Y|\leq|X|$, and $|X|<|Y|$ if and only if $|Y|>|X|$.

Remember that a function $f:X\to Y$ is called surjective, or onto, if for all $y\in Y$, there exists $x\in X$ such that $f(x)=y$.

##### Example 2.3

The following function $f:\\{9,10,11\\}\to\\{6,3\\}$

$$f(9)=6$$
$$f(10)=3$$
$$f(11)=3$$

is surjective, since both $6$ and $3$ are mapped to, and thus we know that $|\\{9,10,11\\}|\geq|\\{6,3\\}|$.

##### Example 2.4

A *permutation* of a string is a rearrangement of the characters in the string. For example, "read" is a permutation of "dare".

Let $A$ be the set of permutations of the string "abcde", and let $B$ be the set of permutations of the string "abcd".

The function $f:A\to B$ which removes the letter "e" from a permutation of "abcde" is surjective, so $|A|\geq|B|$.

#### Definition 3: $|X|=|Y|$ if and only if there is a bijective (one-to-one and onto) function from $X$ to $Y$.
#### Equivalent definition 3: $|X|=|Y|$ if and only if $|X|\leq|Y|$ and $|X|\geq|Y|$.

Remember that a function $f:X\to Y$ is called bijective if it is injective and surjective.

##### Example 3.1

Consider an 8x8 chessboard with a piece starting at the bottom left. The piece is only allowed to move one space up or one space right at a time. Let $A$ be the set of paths that go to the top right without going below the diagonal, 
and let $B$ the set of paths that go to the top right without going above the diagonal.

If $p\in A$, then $p$ can be expressed by a sequence of $u$s and $r$s representing "up" and "right", respectively.

The function $f:A\to B$ which takes $p\in A$ and replaces all the $u$s in $p$ with $r$s and vice versa is bijective, so $|A|=|B|$.