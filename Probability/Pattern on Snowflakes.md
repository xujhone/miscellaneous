# Pattern on Snowflakes

## Problem

Snow-particles are falling on the ground one after another. A particular snowflake turns out to be of type "Stellar Dendrite" with probability 'p' if its previous particle was also Stellar Dendrite, and with probability 'q' if previous one was something else. If a snowflake is picked from ground, what is the probability that it is Stellar Dendrite?

PS:Although no two snowflakes are alike, yet there are various crystalline structures to categorize their interesting shapes. The image depicts the most popular shape, called Stellar Dendrites, which means star-like particles with tree-like branches.

## Solution

Let $Curr$ be type of current snowflake and $Prev$ be type of previous snowflake, and let $1$ be Stellar Dendrite and $0$ otherwise.

$P(Curr = 1 | Prev = 1) = p$ and $P(Curr = 1 | Prev = 0) = q$.

$P(Curr = 1) \\
= P(Curr = 1 | Prev = 1) P(Prev = 1) + P(Curr = 1 | Prev = 0) P(Prev = 0) \\
= p P(Prev = 1) + q P(Prev = 0)$

Now what is $P(Prev = 1)$ ?

Suppose $P(Prev = 1) = P(Curr = 1)$. Then $P(Curr = 1) = q / (1-p+q)$.

Consider the recursive relation: $P_{n+1} = p P_n + q (1 - P_n) = (p-q) P_n + q$.

Note $\lim P_n = q / (1-p+q)$.

If assume the snow falls for enough long time, then $P(Curr = 1) = q / (1-p+q)$.