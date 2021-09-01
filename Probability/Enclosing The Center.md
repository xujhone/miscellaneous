# Enclosing The Center

## Problem

$n$ points are chosen at random on the circumference of a circle. A convex $n$-gon ($n$ sided polygon) is drawn by joining these $n$ points. What is the probability that the center of circle lies inside the region of $n$-gon? 

## Solution

First note that the center of circle lies inside the $n$-gon is when the $n$ points are not in common semi-circle.

Let the $n$ points be $x_1, x_2, \ldots, x_n$. Let $A_i$ be the set of events that all other $n-1$ points are in the semi-circle started from $x_i$ counter-clockwise. 

Then $\{n \textrm{ points in semi-circle}\} = \bigsqcup_{i=1}^{n} A_i$ is a disjoint union.

$P(A_i) = \int_{\textrm{cirlce}} P(A_i|x_i = x) dP_{x_i}(x) = \int_{\textrm{cirlce}} (\frac{1}{2})^{n-1} dP_{x_i}(x) = (\frac{1}{2})^{n-1}$

Thus, $P(n \textrm{ points in semi-circle}) = \sum_{i=1}^{n} P(A_i) = \frac{n}{2^{n-1}}$.

Thus, $P(\textrm{center of circle lies inside }n\textrm{-gon}) = 1 - \frac{n}{2^{n-1}}$.


