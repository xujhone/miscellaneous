# Father of lies

## Problem

A father claims about snowfall last night. First daughter tells that the probability of snowfall on a particular night is 1/8. Second daughter tells that **5 out of 6 times the father is lying**! What is the probability that there actually was a snowfall? 

## Solution

Let $S$ = snowfall and $C$ = claim.

Note that 5 out 6 times the father is lying **is a conditional probability**. 

$P(C|S) = 1/6$ and $P(C|~S) = 5/6$.

$
P(S|C) = P(S, C) / P(C) = P(C|S) \times P(S) / (P(C|S) \times P(S) + P(C|~S) \times P(~S)) \\
= 1/6 \times 1/8 / (1/6 \times 1/8 + 5/6 \times 7/8) \\
= 1/36$

Need to carefully to differentiate the general probability statement and conditional probability statement and to translate the sentences to probability condition.