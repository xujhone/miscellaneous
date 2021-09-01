# Sum To One

## Problem

On pressing a button, a random number is generated uniformly between $0$ and $1$. You keep on generating these numbers until the sum exceeds $1$. What is the probability that you need to press the button more than $n$ times? What is the expected number of times you need to press the button? 

## Solution

Let $X_1, X_2, \ldots, X_n, \ldots \overset{\underset{\mathrm{i.i.d.}}{}}{\sim} \mathrm{Unif}(0, 1) $ and $S_n = \sum_{i=1}^{n} X_i$.

For $n \geq 2$,

$\begin{align*}
P(S_n \leq 1) &= \int_{0}^{1} P(S_n \leq 1 | X_n = x) d P_{X_n}(x) \\
&= \int_{0}^{1} P(S_{n-1} \leq 1-x | X_n = x) dx \\
&= \int_{0}^{1} P(S_{n-1} \leq 1-x) dx \\
&= \int_{0}^{1} P(S_{n-1} \leq x) dx \\
\end{align*}$

This leads to define $P_{n}(x) \colon = P(S_n \leq x)$. Applying the same calculation as above, $P_{n}(x) = \int_{0}^{x} P(S_{n-1} \leq y) dy = \int_{0}^{x} P_{n-1}(y) dy$. Then $P_{n}(x)' = P_{n-1}(x)$. Thus, $P_{1}(x) = P_{n}(x)^{(n-1)}$. Since $P_1(x) = P(X_1 \leq x) = x$, $P_{n}(x) = \frac{x^n}{n!}$.

Thus, $P(S_n \leq 1) = \frac{1}{n!}$.

Let $N$ be the least number of random numbers that sum over $1$. There are two ways to compute $E(N)$:

- Note $P(N = n) = P(S_n > 1, S_{n-1} \leq 1) = P(S_{n-1} \leq 1) - P(S_n \leq 1) = \frac{1}{(n-1)!} - \frac{1}{n!}$ since $\{S_n \leq 1\} \subset \{S_{n-1} \leq 1\}$.

    Thus, 

    $\begin{align*}
    E(N) &= \sum_{n=2}^{\infty} n \cdot P(N=n) \\
    &= \sum_{n=2}^{\infty} n (\frac{1}{(n-1)!} - \frac{1}{n!}) \\
    &= \sum_{n=2}^{\infty} \frac{1}{(n-2)!} \\
    &= e
    \end{align*}$

- In fact, $P(N \geq n) = P(S_{n-1} \leq 1) = \frac{1}{(n-1)!}$.

    $\begin{align*}
    E(N) &= \sum_{n=2}^{\infty} n \cdot P(N=n) \\
    &= P(N\geq 2) + P(N \geq 2) + P(N \geq 3) + P(N \geq 4) + \cdots \\
    &= 1 + \sum_{n=1}^{\infty} \frac{1}{n!} \\
    &= e
    \end{align*}$