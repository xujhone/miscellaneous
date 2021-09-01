# Distinct Number Draws

## Problem

Given the set of numbers from $1$ to $n: \{ 1, 2, 3, \ldots, n \}$. We draw $n$ numbers randomly (with uniform distribution) from this set (with replacement). What is the expected number of distinct values that we would draw? 

## Solution

Let $X_i = \mathbb{1}_{\{\textrm{number i is drew at least once}\}}$ for $1 \leq i \leq n$. 

Let $Y$ be number of distinct values. Then $Y = \sum_{i=1}^{n} X_i$.

Thus, $E(Y) = \sum_{i=1}^{n} E(X_i) = \sum_{i=1}^{n} P(X_i = 1)$.

$P(X_i = 1) = 1 - P(X_i = 0) = 1 - (\frac{n-1}{n})^n$.

Thus, $E(Y) = n (1 - (\frac{n-1}{n})^n)$.




 
 