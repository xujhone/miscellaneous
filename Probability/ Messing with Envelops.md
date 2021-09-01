#  Messing with Envelops

## Problem

There are n letters and n envelopes. Your servant puts the letters randomly in the envelopes so that each letter is in one envelope and all envelopes have exactly one letter. (Effectively a random permutation of n numbers chosen uniformly). Calculate the expected number of envelopes with correct letter inside them. 

## Solution

Let $X_i = \mathbb{1}_{\{i^{th} \textrm{ envelop with correct letter}\}}$ for $1 \leq i \leq n$.

Let $Y$ be the number of envelops with correct letter.

Then $E(Y) = E(\sum_{i=1}^{n} X_i) = \sum_{i=1}^{n} E(X_i) = \sum_{i=1}^{n} P(X_i = 1)$.

Note $P(X_i = 1) = 1/n$.

Then $E(Y) = 1$.