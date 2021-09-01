# Colored Runs of Cards

## Problem

There are 26 black(B) and 26 red(R) cards in a standard deck. A run is number of blocks of consecutive cards of the same color. For example, a sequence RRRRBBBRBRB of only 11 cards has 6 runs; namely, RRRR, BBB, R, B, R, B. Find the expected number of runs in a shuffled deck of cards.

## Solution

Let $X_1 = 1$ and $X_i = \mathbb{1}_{\{\textrm{col}(i) \neq \textrm{col}(i-1)\}}$ for $2 \leq i \leq 52$.

Let $Y$ be number of runs. Then $Y = \sum_{i=1}^{52} X_i$.

$E(Y) = E(\sum_{i=1}^{52} X_i) = \sum_{i=1}^{52} E(X_i) = \sum_{i=1}^{52} P(X_i = 1)$

For $2 \leq i \leq 52$, $P(X_i = 1) = \frac{2 \cdot 26 \cdot 26}{52 \cdot 51} = \frac{26}{51}$.

Thus, $E(Y) = 1 + 51 \times \frac{26}{51} = 27$.