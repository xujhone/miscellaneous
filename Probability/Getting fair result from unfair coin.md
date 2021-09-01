# Getting fair result from unfair coin

## Problem

We have a weighted coin which shows a Head with probability p, (0.5<p<1). How do we get a fair toss from this? That is, how do we toss this coin in such a way that we can have probability of winning = loosing = 50%? 

## Solution

Let win = {head, tail} and loose = {tail, head}. Then P(win) = P(lose).

Use naive rejection, toss the weighted coin twice. If not {head, tail} or {tail, head}, discard the result. Thus, P(win) = P(loose) = 0.5.

## Follow up

I proposed a faster method, "lets keep tossing the coin to form a sequence of H's & T's . I win if HT appears before TH" . Was I bluffing?

## Solution

Yes. Note if the first toss is H, then I always win; and if the first toss is T, then I always loose.