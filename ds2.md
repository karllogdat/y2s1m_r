# Mathematical Induction
Mathematical induction is a proof technique which is used to prove a statement, a formula, or a theorem is true for all natural numbers.

## Weak Induction
Prove the base case, assume inductive hypothesis $n = k$, then prove $k + 1$ holds (inductive step).

If $p(k)$ is true, then $p(k+1)$ is true.

## Strong Induction 
Similar to weak induction, but all previous values of $k$ are also assumed.

If $p(i)$ is true $\forall i : i \leq k$, then $p(k+1)$ is true.

## Well Ordering Property
Every non-empty set of non-negative integers has a least element. 

If $a \in A$, where $a = \{a : a = \text{ positive values of } A\}$. The least element of $A$ is 1, since it is the least positive element.

It is important to know the least element in mathematical induction since the base case always starts with the least element.

# Recursive Definitions and Structural Induction
Recursion is a method of defining a function, sequence, or object in terms of itself.

## Recursively Defined Functions
**Arithmetic Sequence** is an order of numbers that has a pattern regarding the difference of the numbers that are beside each other.

$$
\{5, 9, 13, 17, 21, \ldots\}
$$

Finding the $n$-th term of an arithmetic sequence is given by the formula:

$$
a_n = a_1 + (n - 1)d
$$

Where $d$ is the difference between the terms.

**Geometric Sequence** is an order of numbers that has a pattern regarding the ration of the numbers that are beside each other.

$$
\{2, 4, 8, 16, 32, \ldots \}
$$

Finding the $n$-th term of a geometric sequence is given by the formula: 

$$
a_n = a_1 r^{n-1}
$$

Where $r$ is the common ratio between the terms.

## Recursively Defined Sets and Structures
Assume $S$ is a set. To recursively define $S$, we use two steps to define $S$. The *basis step* defines the initial collection of elements. The *recursive step* defines a rule in forming new elements from known values in the set.

Consider $S \subseteq \mathbb{Z}$; $3 \in S$ and if $x \in S$ and $y \in S$, then $x + y \in S$.

In this example all values in $S$ are multiples of $3$.

$$
\begin{align*}
3 \in S & \\
3 + 3 \in S &\implies 6 \in S \\
3 + 6 \in S &\implies 9 \in S \\
3 + 9 \in S &\implies 12 \in S \\
6 + 9 \in S &\implies 15 \in S \\
\end{align*}
$$

## Recursive Algorithms
Algorithms are instructions or set of rules to be followed to achieve something in the field of programming. An algorithm is called recursive if a problem is solved by reducing the same problem, but its input size is getting smaller everytime the algorithm runs.

$$
\begin{align*}
f(0) &= 1, n = 0, 1, 2, 3, \ldots \\
f(n+1) &= f(n)^2 + f(n) + 1
\end{align*}
$$

# Binomial Coefficients and Identities
The number of $r$-combinations from a set of $n$ elements is often denoted by $\binom{n}{r}$. This relation is also called a binomial coefficient as it occurs as coefficients of a binomial expansion. 

## The Binomial Theorem 
The binomial theorem gives the coefficients of the expansion of powers of binomial expressions. 

Expand $(x+y)^3$.

$$
\begin{align*}
        (x+y)^3 &= (x+y)(x+y)(x+y) \\
                &= x^3 + 3x^2y + 3xy^2 + y^3 \\
\end{align*}
$$

**Theorem 1: Binomial Theorem**. Let $x$ and $y$ be variables, and $n$ be a non-negative integer. Then: 

$$
\begin{align*}
        (x+y)^n &= \sum_{j=0}^{n} \binom{n}{j} x^{n-j}y^y \\
                &= \binom{n}{0} x^{n}y^{0} + \binom{n}{1} x^{n-1}y^{1} + \cdots + \binom{n}{n-1} x^{1}y^{n-1} + \binom{n}{n} x^{0}y^{n}
\end{align*}
$$

**Corollary 1**. Let $n$ be a non-negative integer. Then

$$
\sum_{k = 0}^{n} \binom{n}{k} = 2^n
$$

**Corollary 2**. Let $n$ be a positive integer. Then

$$
\sum_{k=0}^{n}(-1)^k \binom{n}{k} = 0
$$

## Pascal's Identity and Triangle
**Theorem 2: Pascal's Identity**. Let $n$ and $k$ be positive integers where $n \geq k$. Then

$$
\binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}
$$

## Other Identities Involving Binomial Coefficients
**Theorem 3: Vandermonde's Identity**. Let $m$, $n$, and $r$ be non-negative integers with $r$ not exceeding either $m$ or $n$. Then

$$
\binom{m+n}{r} = \sum_{k=0}^{r} \binom{m}{r-k} \binom{n}{k}
$$

Corollary 4 follows from Vandermonde's Identity.

**Corollary 4**. If $n$ is a non-negative integer, then

$$
\binom{2n}{n} = \sum_{k=0}^{n} \binom{n}{k}^2
$$

**Theorem 4**. Let $n$ and $r$ be non-negative integers with $r \leq n$. Then

$$
\binom{n+1}{r+1} = \sum_{j=r}^{n} \binom{j}{r}
$$
