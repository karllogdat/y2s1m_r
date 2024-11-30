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

The sum of an arithemtic sequence of the first $n$-terms is given by:

$$
S_n = \frac{n}{2}[2a_1 + (n - 1)d]
$$

**Geometric Sequence** is an order of numbers that has a pattern regarding the ration of the numbers that are beside each other.

$$
\{2, 4, 8, 16, 32, \ldots \}
$$

Finding the $n$-th term of a geometric sequence is given by the formula: 

$$
a_n = a_1 r^{n-1}
$$

Where $r$ is the common ratio between the terms.

The sum of the first $n$-terms in a geometric series is given by: 

$$
S_n = \frac{a_1(1 - r^n)}{1 - r}
$$

## Recursively Defined Sets and Structures
Assume $S$ is a set. To recursively define $S$, we use two steps to define $S$. The *basis step* defines the initial collection of elements. The *recursive step* defines a rule in forming new elements from known values in the set.

Consider $S \subseteq \mathbb{Z}$; $3 \in S$ and if $x \in S$ and $y \in S$, then $x + y \in S$.

In this example all values in $S$ are multiples of $3$.

\begin{align*}
3 \in S & \\
3 + 3 \in S &\implies 6 \in S \\
3 + 6 \in S &\implies 9 \in S \\
3 + 9 \in S &\implies 12 \in S \\
6 + 9 \in S &\implies 15 \in S \\
\end{align*}

## Recursive Algorithms
Algorithms are instructions or set of rules to be followed to achieve something in the field of programming. An algorithm is called recursive if a problem is solved by reducing the same problem, but its input size is getting smaller everytime the algorithm runs.

\begin{align*}
f(0) &= 1, n = 0, 1, 2, 3, \ldots \\
f(n+1) &= f(n)^2 + f(n) + 1
\end{align*}

# Binomial Coefficients and Identities
The number of $r$-combinations from a set of $n$ elements is often denoted by $\binom{n}{r}$. This relation is also called a binomial coefficient as it occurs as coefficients of a binomial expansion. 

## The Binomial Theorem 
The binomial theorem gives the coefficients of the expansion of powers of binomial expressions. 

Expand $(x+y)^3$.

\begin{align*}
        (x+y)^3 &= (x+y)(x+y)(x+y) \\
                &= x^3 + 3x^2y + 3xy^2 + y^3 \\
\end{align*}

**Theorem 1: Binomial Theorem**. Let $x$ and $y$ be variables, and $n$ be a non-negative integer. Then: 

\begin{align*}
        (x+y)^n &= \sum_{j=0}^{n} \binom{n}{j} x^{n-j}y^y \\
                &= \binom{n}{0} x^{n}y^{0} + \binom{n}{1} x^{n-1}y^{1} + \cdots + \binom{n}{n-1} x^{1}y^{n-1} + \binom{n}{n} x^{0}y^{n}
\end{align*}

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

# Generalized Permutation and Combinations 

## Permutations with Repetition 
**Example**. How many string of length $r$ can be formed from the uppercase letters of the English alphabet?

Using the product rule, since there are $26$ letters in the English alphabet (and each letter can be used repeteadly), there are $26^r$ strings of uppercase letters with length $r$. 

**Theorem 1**. The number of $r$-permutations of a set of $n$ objects with repetition allowed is given by $n^r$.

## Combinations with Repetition 
**Example**. How many ways are there to select five bills from a cash box containing $1, $2, $5, $10, and $100 bills? Assume that the order in which the bills are chosenn does not matter, that the bills of each denomination are indistinguishable, and that there are at least five bills of each type.

\begin{align*}
\binom{11}{5} = \frac{11!}{5!6!} = 462
\end{align*}

This formula will be given in Theorem 2.

**Theorem 2**. There are $\binom{n+r-1}{r} = \binom{n+r-1}{n-1}$ $r$-combinations from a set with $n$ elements when repetition of elements is allowed.

| Type | Repetition? | Formula |
| ---- | ----------- | ------- |
| r-permutations | yes | $\frac{n!}{(n - r)!}$ |
| r-combinations | yes | $\frac{n!}{r!(n-r)!}$ |
| r-permutations | no  | $n^r$ |
| r-combinations | no  | $\frac{(n+r-1)!}{r!(n-1)!}$ |

## Permutations with Indistinguishable Objects 
**Example**. How many different strings can be made by reordering letters of the word `SUCCESS`. 

\begin{align*}
\binom{7}{3} \cdot \binom{4}{2} \cdot \binom{2}{1} \cdot \binom{1}{1} &= 420
\end{align*}

**Theorem 3**. The number of different permutations of $n$ objects, where there are $n_1$ indistinguishable objects of type $1$, $n_2$ indistinguishable objects of type $2$, ..., and $n_k$ indistinguishable objects of type $k$, is 

$$
\frac{n!}{n_1!\,n_2!\,\cdots\,n_k!}
$$

## Distinguishable Objects and Distinguishable Boxes
**Example**. How many ways are there to distribute hands of $5$ cards to each of four players from the standard deck of $52$ cards.

$$
\binom{52}{5} \binom{47}{5} \binom{42}{5} \binom{37}{5}
$$

**Theorem 4**. The numer of ways to distribute $n$ distinguishable objects into $k$ distinguishable boxes so that $n_i$ objects are placed into box $i$, $i = 1, 2, \ldots, k$, equals

$$
\frac{n!}{n_1!\,n_2!\,\cdots n_k!}
$$

## Indistinguishable Objects and Distinguishable Boxes 
Counting the number of ways of placing $n$ indistinguishable objects into $k$ distinguishable boxes is the same as counting the number of $n$-combinations for a set with $k$ elements when repetitions are allowed.

$$
\binom{n+r-1}{r} = \binom{n+r-1}{n-1}
$$

## Distinguishable Objects and Indistinguishable Boxes
Let $S(n, j)$ denote the number of ways to distribute $n$ distinguishable objects into $j$ indistinguishable boxes so that no box is empty. The number $S(n, j)$ are called Stirling numbers of the second kind.

$$
S(n,j) = \frac{1}{j!} \sum_{i=0}{j-1} (-1)^1 \binom{j}{i} (j-i)^n
$$

Consequently, the number of ways to distribute $n$ distinguishable objects into $k$ indistinguishable boxes equals

$$
\sum_{j=1}^{k} S(n,j) = \sum_{j=1}^{k} \frac{1}{j!} \sum_{i=0}^{j-1} (-1)^1 \binom{j}{i} (j-i)^n
$$

## Indistinguishable Objects and Indistinguishable Boxes 
Distributing $n$ indistinguishable objects into $k$ indistinguishable boxes is the same as writing $n$ as a sum of at most $k$ positive integers in non-increasing order. There is no simple closed formula for this number.

# Discrete Probability 
The sample space of an experiment is the set of all possible outcome. An event is a subset of the sample space. 

If $S$ is a is a finite non-empty sample space of equally likely outcomes, and $E$ is an event, that is, a subset of $S$, then the probability of $E$ is $p(E) = \frac{|E|}{|S|}$.

## Probability Theory
### Assigning Probabilities
Let $S$ be the sample space of an experiment with a finite or countable number of outcomes. We assign the probability $p(s)$ to each outcome $s$. We require that two conditions be met: 

1. $0 \leq p(s) \leq 1, \forall s \in S$
2. $\sum p(s) = 1$

**Definition 1**. Suppose $S$ is a set with $n$ elements. The uniform distribution assigns the probability $\frac{1}{n}$ to each element of $S$.

**Definition 2**. The probability of an event $E$ is the sum of the probabilities of the outcomes in $E$. That is,

$$
p(E) = \sum p(s); s \in E 
$$

### Probabilities of Unions and Events 
For the complementary of an event $E$ $\overline{E}$, $p(\overline{E}) = 1 - p(E)$.

$$
\sum_{s \in S} p(s) = 1 = p(E) + p(\overline{E})
$$

## Conditional Probability 
To find the *conditional probability* of $E$ given $F$, we use $F$ as the sample space. For an outcome from $E$ to occur, this outcome must also belong to $E \cap F$.

Let $E$ and $F$ be events with $p(F) > 0$. The conditional probability of $E$ given $F$, denoted by $p(E | F)$, is defined as 

$$ 
p(E|F) = \frac{p(E \cap F)}{p(F)}
$$

The events $E$ and $F$ are independent if and only if $p(E \cap F) = p(E)p(F)$.

## Bernoulli Trials and the Binomial Distribution 
An experiment with only two possible outcome, *success* and *failure* is called a **Bernoulli trial**, after James Bernoulli. 

**Example**. A coin is biased so that the probability of heads is $\frac{2}{3}$. What is the probability that four heads come up when the coin is flipped seven times, assuming the flips are independent.

$$
\binom{7}{4} (\frac{2}{3})^4 (\frac{1}{3})^3 = \frac{560}{2187}
$$

The probability of $k$ successes in $n$ independent Bernoulli Trials is denoted by $B(k; n,p)$, where $p$ is the probability for success and $q = 1 - p$ is the probability of failure. Considered as a function of $k$, we call this function the **binomial distribution**.

$$
b(k; n,p) = \binom{n}{k} p^k q^{(n-k)}
$$

## Bayes Theorem
Let $A$ and $B$ be events and $p(B) \neq 0$.

$$
p(A|B) = \frac{p(B|A)p(A)}{p(B)}
$$

## Expected Value and Variance
**Example**. Let $X$ be the number that comes up when a fair die is rolled. What is the expected value of $X$?

$$
E(X) = \frac{1}{6} \times 1 + \frac{1}{6} \times 2 + \frac{1}{6} \times 3 + \frac{1}{6} \times 4 + \frac{1}{6} \times 5 + \frac{1}{6} \times 6 = \frac{21}{6} = \frac{7}{2}
$$
