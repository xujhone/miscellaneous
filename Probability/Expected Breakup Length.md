# Expected Breakup Length

## Problem

A stick is broken into 3 pieces, by randomly choosing two points along its unit length, and cutting it. What is the expected length of the middle part? 

## Solution

Let $X,Y \sim \mathrm{Unif}(0, 1)$. Then the length of the middle part is $\mid X-Y \mid$.

Then the expected length is

$\int_{0}^{1}\int_{0}^{1} \mid x-y \mid dx dy = \int_{0}^{1}\int_{0}^{x} (x-y) dy dx + \int_{0}^{1}\int_{0}^{y} (y-x) dx dy = 2 \times 1/6 = 1/3$.