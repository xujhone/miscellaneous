# Single Bid

## Problem

You have an opportunity to make one bid on an object, whose value to its owner is, as far as you know, uniformly random integer between \$0 and \$100. What you do know is that you are so much better at operating the widget than he is, that its value to you is 80% greater than its value to him. If you offer more than the widget is worth to the owner, he will sell it. But you get only one shot. How much should you bid? For example, if its actual value is \$10, you bid and win at \$11, and sell it for \$18, making profit. But if you bid more than \$18, you make loss! But since you don't know how much its actual price is, how do you bid in order to make some profit?

## Solution

Let $X \sim \textrm{Unif}(0, 1, 2, \ldots, n-1)$ and $P(X = i) = 1 / n$ for $0 \leq i \leq n-1$. Let $Y$ be bid and suppose $p_i = P(Y = i)$ for $0 \leq i \leq n-1$. Let $Z$ be the profit.

If $Y < X$, $Z = 0$. If $Y \geq X$, $Z = 1.8 \cdot X - Y$.

$\begin{align*}
E(Z) &= \sum_{i=0}^{n-1} E(Z | X=i) \cdot \frac{1}{n} \\
&= \sum_{i=0}^{n-1} (\sum_{j=0}^{n-1} E(Z | X=i, Y=j) \cdot p_j) \cdot \frac{1}{n} \\
&= \sum_{i=0}^{n-1} \sum_{j=i}^{n-1} (1.8 \cdot i - j) \cdot p_j \cdot \frac{1}{n} \\
&= \frac{1}{n} \sum_{j=0}^{n-1} \sum_{i=0}^{j} (1.8 \cdot i - j) \cdot p_j \\
&= \frac{1}{n} \sum_{j=0}^{n-1} -\frac{1}{10} j(j+1) p_j \\
&= 0 \cdot p_0 - \frac{1}{10 n} \sum_{j=1}^{n-1} j(j+1) p_j \\
&\leq 0 
\end{align*}$

Note equality holds if and only if $p_0 = 1$. Thus, I should not bid.

### Another Method

Note the expected profit when I bid $j$ and win the widget is

 $E(Z|Y = j, X \leq Y) = E(1.8 \cdot X-j|X\leq j) = 1.8 \cdot E(X | X \leq j) - j = -0.1j$.
 
 And if I did not get the widget, the profit is 0. Thus, I should not bid.


