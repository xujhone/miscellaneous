# Greed for an ACE

## Problem

What is the expected number of cards that need to be turned over in a regular 52-card deck in order to see the first ace? 

## Solution

First note 52 cards are divided into two groups: 4 aces and 48 others.

Let $X_i \overset{\underset{\mathrm{def}}{}}{=} \mathbb{1}_{\{i^{th} \textrm{ card is turned over before any ace}\}}$ for $1 \leq i \leq 48$.

Then the expected number of cards that need to be turned over is

$\sum_{i=1}^{48}E(X_i) + 1$.

$E(X_i) = P(X_i = 1) = 1/5$.

Thus, the final answer is $48/5 + 1 = 53/5$.

### Recursive Method

Let $X_n$ be the number of cards to be turned over in a deck of $n$ cards.

Condition on the first card Y:

$\begin{align*}
E(X_n) &= E(X_n | Y = \textrm{ace}) P(\textrm{ace}) + E(X_n | Y \neq \textrm{ace})P(\textrm{not ace}) \\
&= 1 \times \frac{4}{n} + (1 + E(X_{n-1})) \times (1 - \frac{4}{n}) \\
&= (1 - \frac{4}{n}) E(X_{n-1}) + 1
\end{align*}$

Note initial case: $E(X_4) = 1$.

Thus, $E(X_n) = (n+1) / 5$.

