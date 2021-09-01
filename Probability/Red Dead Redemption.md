# Red Dead Redemption

## Problem

In a room stand $n$ armed and angry people. At each chime of a clock, everyone simultaneously spins around and shoots a random other person. The persons shot fall dead and the survivors spin and shoot again at the next chime. Eventually, either everyone is dead or there is a single survivor.

As $n$ grows, what is the limiting probability that there will be a survivor.

## Solution

Let $X_n$ be the number of survivors for $n$ people. Then $0 \leq X_n \leq n-2$. Let $p_{n,k} = P(X_n = k)$ for $0 \leq k \leq n-2$.

Let $Y_n$ be the probability that there will be one survivor.

$\begin{align*}
P(Y_n) &= \sum_{k=0}^{n-2} P(Y_n | X_n = k) \cdot p_{n,k} \\
&= \sum_{k=0}^{n-2} P(Y_k) \cdot p_{n,k} \\
&= \sum_{k=0}^{n-2} \sum_{l=0}^{k-2} P(Y_l) \cdot p_{k,l} \cdot p_{n,k}
\end{align*}$



