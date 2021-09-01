# Consecutive Heads

## Problem

What is the expected number of coin tosses required to get $n$ consecutive heads? 

## Solution

Let $p$ be the probability of Head.

Let $X_n$ be the number of tosses required to get $n$ consecutive heads. Let $Y$ be toss after $X_{n-1}$.

Then 

$E(X_n) = E(X_n | Y = \mathrm{Head}) p + E(X_n | Y = \mathrm{Tail}) (1-p) \\
= (E(X_{n-1}) + 1) p + (E(X_{n-1}) + 1 + E(X_n)) (1-p) \\
= E(X_{n-1}) + 1 + (1-p) E(X_n)$

$p E(X_n) = E(X_{n-1}) + 1$.

Note $E(X_1) = 1 / p$.

Thus, $E(X_n) = \sum_{i=1}^{n} 1/p^i$.
