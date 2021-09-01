# Chess Tournament

## Problem

A chess tournament has $K$ levels and $2^K$ players with skills $1 > 2 > ... >2^K$. At each level, random pairs are formed and one person from each pair proceeds to next level. When two opponents play, the one with better skills always wins. What is the probability that players 1 and 2 will meet in the final level? 

## Solution

### Conditional Method

By the law of total probability,

$
P(\textrm{meet in the final}) \\
= P(\textrm{not meet from 1 to } K-1) \\
= P(\textrm{not meet }K-1 | \textrm{ not meet }K-2) \times P(\textrm{not meet }K-2 | \textrm{ not meet }K-3) \times \\
\cdots \times P(\textrm{not meet 3 | not meet 2}) \times P(\textrm{not meet 2 | not meet 1}) \times P(\textrm{not meet 1})
$

$P(\textrm{not meet 1}) = 1 - \frac{(2^K-2) ! \times 2^{K-1} \times 2}{2^K !} = 1 - \frac{1}{2^K - 1} = \frac{2^K - 2}{2^K - 1}$

$P(\textrm{not meet } K-k+1 | \textrm{ not meet } K-k) = \frac{2^k - 2}{2^k - 1}$

$P(\textrm{meet in the final}) = \frac{2^K - 2}{2^K - 1} \times \prod_{k=2}^{K-1} \frac{2(2^{k-1} - 1)}{2^k - 1} = \frac{2^K - 2}{2^K - 1} \times 2^{K-2} \times \frac{2^1-1}{2^{K-1}-1} = \frac{2^{K-1}}{2^K - 1}$

### Combinatorial Method

Think of the whole process as a tree. The root is player 1. Then his left and right children are 1 and 2 or 2 and 1. This means that at the leaf level, player 1 and 2 are separated in two groups of $2^{K-1}$ players in each group.

How many ways to divide player 1 and 2 into two groups?

When $K = 2$, there are ways in total: 1,2 | 3, 4; 1



