# Number of Double Heads

## Problem

A coin is tossed 10 times and the output written as a string. What is the expected number of HH? Note that in HHH, number of HH = 2. (eg: expected number of HH in 2 tosses is 0.25, 3 tosses is 0.5) 

## Solution

Let $X_n$ be the number of HH in $n$ tosses.

$E(X_1) = 0, E(X_2) = P(HH) = 0.25$.

Condition on the first toss:

$\begin{align*}
E(X_n) &= E(X_n | T) \times P(T) + E(X_n | H) \times P(H) \\
       &= E(X_{n-1}) \times 1/2 + E(X_n | H) \times 1/2
\end{align*}$

Compute $E(X_n | H)$:

Consider the following $n-1$ tosses. Then it has two groups depending on the second toss. Let $T?$ be the set of tosses that start with $T$ and $H?$ be the set of tosses that start with $H$. For any toss $t$, let $HH(t)$ be number of $HH$ in $t$. 

Then by definition, $E(X_{n-1}) = \sum_{t \in T?} HH(t) \cdot P(t) + \sum_{t \in H?} HH(t) \cdot P(t)$.

Thus, 

$\begin{align*}
E(X_n | H) &= \sum_{t \in T?} HH(t) \cdot P(t) + \sum_{t \in H?} (HH(t) + 1) \cdot P(t) \\
&= \sum_{t \in T?} HH(t) \cdot P(t) + \sum_{t \in H?} HH(t) \cdot P(t) + \sum_{t \in H?} P(t) \\
&= E(X_{n-1}) + 1/2.
\end{align*}$

Thus, $ E(X_n) = E(X_{n-1}) \times 1/2 + (E(X_{n-1}) + 1/2) \times 1/2 = E(X_{n-1}) + 1/4$.

Thus, $E(X_n) = (n-1) / 4$.


