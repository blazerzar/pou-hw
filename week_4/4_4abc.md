# Exercise 4.4abc

## Problem

Let $X_k, k = 1, \ldots, n$ be random variables with the Bernoulli measure as
the PMF. Let $X = \sum_{k=1}^n X_k$.

a) We cal $X_k$ a Bernoulli random variable with parameter $p \in (0, 1)$. Find
   the CDF of $X_k$.

b) Find PMF of $X$. This is a Binomial random variable with support in
   $\{0, 1, 2, \ldots, n\}$ and parameters $p \in (0, 1)$ and
   $n \in \mathbb{N}_0$. We denote

$$
X|n,p \sim \text{binomial}(n, p).
$$

c) Find CDF of X.

## Solution

a) Since $P(X_k = 0) = 1 - p$, the CDF increases by $1 - p$ at $0$. The second
   jump is at $1$, since $P(X_k = 1) = p$.

$$
F_{X_k}(x) = \begin{cases}
    0,     & x < 0, \\
    1 - p, & 0 \le x < 1, \\
    1,     & x \ge 1.
\end{cases}
$$

b) For $X$ to have value $k$, $k$ Bernoulli random variables have to have value
   $1$ and the others $0$:

$$
p_X(k) = \binom{n}{k} p^k (1-p)^{n-k}.
$$

c) To get CDF to $X$, we sum values of PMF up to the closest lower integer:

$$
F_X(x) = \sum_{k=0}^{\lfloor x \rfloor} \binom{n}{k} p^k (1-p)^{n-k}.
$$
