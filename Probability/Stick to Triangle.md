# Stick to Triangle

## Problem

A stick is broken into 3 parts, by choosing 2 points randomly along its length. With what probability can it form a triangle? 


## Solution

Let X, Y ~ Unif(0, 1). Then the length of three sides are: min(X, Y), max(X, Y) - min(X, Y), 1 - max(X, Y).

To form a triangle, max > 1/ 2; max - min  < 1/2, min < 1/2. Note max - min = |X - Y|.

Thus, P = 1/4.