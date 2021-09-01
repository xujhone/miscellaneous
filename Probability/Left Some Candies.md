# Left Some Candies

## Problem

You are taking out candies one by one from a jar that has 10 red candies, 20 blue candies, and 30 green candies in it. What is the probability that there are at least 1 blue candy and 1 green candy left in the jar when you have taken out all the red candies? (Candies of same color are indistinguishable!) 

## Solution

Let $T_r$, $T_b$ and $T_g$ be the position number of the last red, blue and green candies respectively. Then the set of events that at least $1$ blue and $1$ green left when all red are taken out can be denoted as $\{T_r < T_b$, $T_r < T_g\}$. Note $\{T_r < T_b, T_r < T_g\} = \{ T_r < T_b < T_g = 60 \} \sqcup \{ T_r < T_g < T_b = 60 \}$ is a disjoint union.

$P(T_r < T_b < T_g) = P(T_r < T_b |  T_g = 60) \times P(T_g = 60)$

$P(T_g = 60) = P(\textrm{last one is green}) = 30/60$.

Now compute $P(T_r < T_b |  T_g = 60)$. Consider $10$ red, $20$ blue and $29$ green candies. Then the original conditional probability is equal to $P(T_r < T_b)'$ in this new setting. Note green candies are not relevant any more. So we can further assume there are only $10$ red and $20$ blue candies. Thus, $P(T_r < T_b)' = P(\textrm{last one is blue}) = 20/30$. Thus, $P(T_r < T_b |  T_g = 60) = 20/30$.

Thus, $P(T_r < T_b < T_g) = \frac{20}{30} \times \frac{30}{60} = \frac{1}{3}$.

Similarly, $P(T_r < T_g < T_b) = \frac{30}{40} \times \frac{20}{60} = \frac{1}{4}$.

Hence, $P(T_r < T_b, T_r < T_g) = \frac{1}{3} + \frac{1}{4} = \frac{7}{12}$.



