# Breaking Stick

## Problem

The stick drops and breaks at a random point distributed uniformly across the length. What is the expected length of the smaller part? 

## Solution

Let $X \sim \textrm{Unif}(0, l)$. Let $f(x) = \min (x, l-x)$.

Then $E(f(X)) = \int_{x \leq l/2} x \cdot 1/l dx + \int_{l/2 < x < l} (l-x) \cdot 1/l dx = 1/l \cdot 1/2 \cdot l \cdot l/2 = l/4$.