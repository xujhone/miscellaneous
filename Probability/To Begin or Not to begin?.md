# To Begin or Not to begin?

## Problem

A and B are alternately picking balls from a bag without replacement. The bag has k black balls and 1 red ball. Winner is the one who picks the red ball. Who is more likely to win, the one who starts first, or second? 

## Solution

Let $X$ be the number of turns for the one who starts first and wins. Note $X$ can only be odd number.

$\begin{align*}
P(\textrm{first win}) &= \sum_{i=0}^{\left \lfloor k/2 \right \rfloor} P(X = 2i+1) \\
&= \sum_{i=0}^{\left \lfloor k/2 \right \rfloor} \frac{k}{k+1} \frac{k-1}{k} \cdots \frac{k+1-2i}{k+2-2i} \frac{1}{k+1-2i}\\
&= \sum_{i=0}^{\left \lfloor k/2 \right \rfloor} \frac{1}{k+1} \\
&= \frac{1+\left \lfloor k/2 \right \rfloor}{k+1}
\end{align*}$

There are two cases:

- $k$ is even, $\frac{1+\left \lfloor k/2 \right \rfloor}{k+1} > \frac{1}{2}$
- $k$ is odd, $\frac{1+\left \lfloor k/2 \right \rfloor}{k+1} = \frac{1}{2}$