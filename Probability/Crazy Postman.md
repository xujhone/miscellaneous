# Crazy Postman

## Problem

A postman brought N letters to a house with two letter-boxes. Since the two boxes were empty, he puts 1 mail in each of the two mail boxes. Then he chooses one of boxes with probability proportional to number of letters present in that box, and puts the 3rd letter in it. He does this for all subsequent letters. What is the expected number of letters in the box with lower letters? 

## Solution

Let $X_n$ be the number of letters in the box with lower letter after $n$ letters for $2 \leq n \leq N$. Then $X_n \leq \left \lfloor n/2 \right \rfloor$.

For $1 \leq k \leq \left \lfloor n/2 \right \rfloor - 1$, $E(X_{n+1} | X_n = k) = (k+1) \frac{k}{n} + k \frac{n-k}{n} = \frac{n+1}{n} \cdot k$.

When $X_n = \left \lfloor n/2 \right \rfloor$, there are two cases. If $n$ is even, then $X_{n+1} = X_{n} = n / 2$. If $n$ is odd, the box with lower letter does not change after $(n+1)^{th}$ letter. Thus, $E(X_{n+1} | X_n = \left \lfloor n/2 \right \rfloor) = (\left \lfloor n/2 \right \rfloor+1) \frac{\left \lfloor n/2 \right \rfloor}{n} + \left \lfloor n/2 \right \rfloor \frac{n-\left \lfloor n/2 \right \rfloor}{n}$.

Thus, when $n$ is odd,

$\begin{align*}
E(X_{n+1}) &= \sum_{k=1}^{\left \lfloor n/2 \right \rfloor} E(X_{n+1} | X_n = k) \times P(X_n = k) \\
&= \sum_{k=1}^{\left \lfloor n/2 \right \rfloor} \frac{n+1}{n} \cdot k \cdot P(X_n=k) \\
&= \frac{n+1}{n} E(X_n).
\end{align*}$

When $n$ is even,

$\begin{align*}
E(X_{n+1}) &= \sum_{k=1}^{n/2 - 1} E(X_{n+1} | X_n = k) \times P(X_n = k) + \frac{n}{2} \times P(X_n = n/2)\\
&= \sum_{k=1}^{n/2} ((k+1) \frac{k}{n} + k \frac{n-k}{n}) \times P(X_n = k) - \frac{1}{2} P(X_n=n/2)\\
&= \frac{n+1}{n} E(X_n) - \frac{1}{2} P(X_n=n/2)\\
&= \frac{n+1}{n} E(X_n) - \frac{1}{2} \prod_{i=1}^{n/2-1} \frac{i}{2i+1}.
\end{align*}$

Note $X_2 = 1$ and $P(X_2 = 1) = 1$.

Now consider the sequence $\{E(X_n)/n\}_{n=2}^{\infty}$. Note $|\frac{E(X_{n+1})}{n+1} - \frac{E(X_n)}{n}| \leq \frac{1}{n+1} \frac{1}{2} \prod_{i=1}^{n/2-1} \frac{i}{2i+1}$. Thus $E(X_n)/n$ is a Cauchy sequence.

To compute $\lim_{n\rightarrow \infty} E(X_n)/n \overset{\underset{\mathrm{?}}{}}{=} \pi/4-1/2$, consider the odd sequence $a_n \colon = E(X_{2n+1})/(2n+1)$ and $a_0 = 1/2$. Thus, $a_{n+1} = a_{n} - \frac{1}{4n+6} \prod_{i=1}^{n} \frac{i}{2i+1}$.

