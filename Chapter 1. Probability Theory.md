# Chapter 1. Probability Theory

[TOC]



## Set Theory

**Definition**: The *set*, $S$, of all possible outcomes of a particular experment is called *sample space* of the experiment.

**Definition:** An *event* is any collection of possible outcomes of an experiment, that is, any subset of $S$ (including $S$ iteself).

​	**Relationships:**

1. containment

$$
A\subset B\Leftrightarrow x\in A \Rightarrow x\in B
$$

2. equality

$$
A=B\Leftrightarrow A\subset B\;\textrm{and}\;B\subset A
$$

​	**Operations**:

1. Union

$$
A\cup B=\{x|x\in A\;\textrm{or}\;x\in B\}
$$

2. Intersection

$$
A\cap B=\{x|x\in A\;\textrm{and}\; x\in B\}
$$

3. Complementation

$$
A^C=\{x|x\notin A\}
$$

**Theorem**: For any three events $A$,$B$ and $C$ defined on a sample space $S$:

1. Commutativity

$$
A\cup B=B\cup A\\
A\cap B=B\cap A
$$

2. Associativity

$$
A\cup(B\cup C)=(A\cup B)\cup C\\
A\cap(B\cap C)=(A\cap B)\cap C
$$

3. Distributive Laws

$$
A\cap(B\cup C)=(A\cap B)\cup(A\cap C)\\
A\cup(B\cap C)=(A\cup B)\cap(A\cup C)
$$

4. DeMorgan's Laws

$$
(A\cup B)^C=A^C\cap B^C\\
(A\cap B)^C=A^C\cup B^C
$$

**Definition:** Two events $A$ and $B$ are disjoint (or mutually exclusive) if $A\cap B=\emptyset$. The events $A_1,A_2,\dots$ are pairwise disjoint (or mutually exclusive) if $A_i\cap A_j=\emptyset$ for all $i\neq j$.

**Definition**: If $A_1,A_2,\dots$ are pairwise disjoint and $\bigcup_{i=1}^{\infty}A_i=S$, then the collection $A_1, A_2,\dots$ forms a partition of $S$.

## Basics of Probability Theory

### Axiomatic Foundations

**Definition:**	A collection of subsets of S is called a *sigma algebra* (or *Borel field*), denoted by $\beta$, if it satifies the following three properties:

1. $\emptyset\in\beta$, the empty set is an element of $\beta$.
2. If $A\in B$, then $A^c\in\beta$, $\beta$ is closed under complementation.
3. If $A_1,A_2\cdots\in\beta$, then $\bigcup_{i=1}^\infty A_i\in\beta$, $\beta$ is closed under countable unions

**Definition:** 	Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a *probability function* is a function $P$ with domain $\mathcal{B}$ that satisfies:

1. $P(A)\ge0$ for all $A\in B$
2.  $P(S)=1$
3. If $A_1 A_2,\cdots\in\mathcal{B}$ are pairwise disjoiont, then $P(\bigcup_{i=1}^{\infty}A_i)=\sum_{i=1}^{\infty}P(A_i)$

**Theorem:** 	Let $S=\{s_1,s_2,\cdots,s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S$. Let $p_1,\cdots,p_n$ be nonnegative numbers that sum to $1$. For any $A\in \mathcal{B}$, define $P(A)$ by
$$
P(a)=\sum_{\{i:s_i\in A\}}p_i
$$
(The sum over an empty set is defined to be $0$.) Then $P$ is a probability function on $\mathcal{B}$. This remains true if $S=\{s_1,s_2,\cdots\}$ is a countable set.

### The Calculus of Probability

**Theorem:** 	If $P$ is a probability function and $A$ is any set in $B$, then

1. $P(\emptyset)=0$, where $\emptyset$ is the empty set
2. $P(A)\le1$
3. $P(A^{C})=1-P(A)$

**Theorem:** 	If $P$ is a probability function and $A$ and $B$ are any sets in $\mathcal{B}$, then 

1. $P(B\bigcap A^c)=P(B)-P(A\bigcap B)$
2. $P(A\bigcup B)=P(A)+P(B)-P(A\bigcap B)$
3. If $A\subset B$, then $P(A)\le P(B)$

**Theorem:** 	If $P$ is a probability function, then

1. $P(A)=\sum_{i=1}^{\infty}P(A\bigcap C_i)$ for any partition $C_1,C_2,\cdots$
2. $P(\bigcup_{i=1}^{\infty}A_i)\le\sum_{i=1}^{\infty}P(A_i)$ for any sets $A_i,A_2,\cdots$       (Boole's Inequality)
   

### Counting

**Theorem:** If a job consists of $k$ sepperate tasks, the $i$th of which can be done in $n_i$ ways, $i=1,\cdots,k$, then the entire job can be done in $n_1\times n_2\times \cdots\times n_k$ ways.

**Definition:** For a positive integer $n$, $n!$ (read $n$ factorial) is the product of all of the  positive integers less than or equal to $n$. That is
$$
n!=n\times (n-1) \times(n-2)\times\cdots\times3\times2\times1.
$$
Furthermore, we define $0!=1$.

**Definition:** For nonnegative integers $n$ and $r$, where $n\ge r$, we define the symbol$\begin{pmatrix}n\\r\end{pmatrix}$, read *$n$ choose $r$*, as 
$$
\begin{pmatrix}n\\r\end{pmatrix}=\frac{n!}{r!(n-r)!}
$$

|           |        Without replacement         |            With replacement            |
| --------- | :--------------------------------: | :------------------------------------: |
| Ordered   |        $\frac{n!}{(n-r)!}$         |                 $n^r$                  |
| Unordered | $\begin{pmatrix}n\\r\end{pmatrix}$ | $\begin{pmatrix}n+r-1\\r\end{pmatrix}$ |



## Conditional Probability and Independence

**Definition:** If $A$ and $B$ are events in $S$, and $P(B)>0$, then the *conditional probability* of *$A$ given $B$*, written $P(A|B)$, is
$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$
**Theorem: (Bayes' Rule)** Let $A_1,A_2,\dots$ be a partition of the sample space, and let $B$ be any set. Then, for each $i=1,2,\dots$,
$$
P(A_i|B)=\frac{P(B|A_i)P(A_i)}{\sum_{j=1}^{\infty}P(B|A_j)P(A_j)}
$$
**Definition:** Two events, $A$ and $B$, are *statistically independent* if 
$$
P(A\cap B) = P(A)P(B)
$$
**Theorem:** If $A$ and $B$ are independent, then the following pairs are also independent:

1. $A$ and $B^C$
2. $A^C$ and $B$
3. $A^C$ and $B^C$

> **Proof:** We will prove only 1. To prove 1 we mush know that $P(A\cap B^C)=p(A)P(B^C)$. From Theorem we hava
> $$
> \begin{align}
> P(A\cap B^C) &= P(A)-P(A\cap B)\\
> 			 &= P(A) - P(A)P(B)\\
> 			 &= P(A)(1-P(B))\\
> 			 &= P(A)P(B^C)
> \end{align}
> $$

**Definition:** A collection of events $A_1,\dots,A_n$ are *mutually independence* if for any subcollection $A_{i_1},\dots,A_{i_k}$, we have
$$
P\left(\bigcap_{j=1}^{k}A_{i_j}\right)=\prod_{j=1}^kP(A_{i_j})
$$

 ## Random Variables

**Definition:** A *random variable* is a function from a sample space $S$ into the real numbers.

## Distribution Functions

**Definition:**  The *cumulative distribution function* or *cdf* of a random variable $X$, denoted by $F_X(x)$, is defined by
$$
F_X(x)=P_X(X\le x),\qquad \mathrm{for\;all\;}x.
$$
**Theorem:** The function $F(x)$ is a *cdf* iif and only if the following three conditions hold:

1. $\lim_{x\rightarrow-\infty}F(x)=0$ and $\lim_{x\rightarrow \infty}F(x)=1$
2. $F(x)$ is a nondecreasing function of x
3. $F(x)$ is *right-continuous*; that is, for every number $x_0$, $\lim_{x\rightarrow x_0}F(x)=F(x_0)$

**Definition:** A random variable $X$ is *continuous* if $F_X(x)$ is a continuous function of x. A random variable $X$ is *discrete* if $F_X(x)$ is a step function of $x$.

**Definition**: The random variable $X$ and $Y$ are *identically distributed* if, for every set $A\in\mathcal{B}^1，P(X\in A)=P(Y\in A)$.

**Theorem:** The following two statements are equivalent:

1. The random variables $X$ and $Y$ are identically distributed.
2. $F_X(x)=F_Y(x)$ for every $x$.

## Density and Mass Functions

**Definition:** The *probability mass function (pmf)* of a discrete random variable $X$ is given by
$$
f_X(x)=P(X=x)\qquad\mathrm{for\;all\;}x
$$
**Definition:** The *probability density function* or *pdf*, $f_X(x)$, of a continuous random variable $X$ is the function that satisfies
$$
F_X(x)=\int_{-\infty}^\infty f_X(t)dt\qquad\mathrm{for\;all\;}x.
$$


**Theorem:** A function $f_X(x)$ is a pdf (or pmf) of a random variable $X$ if and only if

1. $f_X(x)\ge0$ for all $x$.
2. $\sum_xf_X(x)=1 (pmf)$ or $\int_{-\infty}^\infty f_X(x)dx=1 (pdf)$