# The Noodles

## Problem

You have $100$ noodles in your soup bowl. You are told to take two ends of some noodles (each end on any noodle has the same probability of being chosen) in your bowl and connect them. You continue until there are no free ends. What is the expected number of loops? What is the probability of making one large loop which includes every noodle?

## Solution

Let $X_i$ be the number of loops for $i$ noodles.

Condition on the first two ends. If the first two ends come from the same noodle, number of loops increases by $1$; else, we end up with $i-1$ noodles.

$E(X_i) = (1 + E(X_{i-1})) \times i / \binom{2i}{2} + E(X_{i-1}) \times (1 - i / \binom{2i}{2}) = E(X_{i-1}) + \frac{1}{2i-1}$.

Thus, $E(X_n) = \sum_{i=1}^{n} \frac{1}{2i-1}$.

$P(\textrm{one loop}) = \prod_{i=2}^{n} (1-\frac{1}{2i-1})$.
