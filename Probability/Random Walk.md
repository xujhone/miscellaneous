# Random Walk

## Problem

You are initially located at origin in the $x$-axis. You start a random walk with equal probability of moving left or right one step at a time. What is the probability that you will reach point $a$ before reaching point $-b$? What is the expected number of steps to reach either $a$ or $-b$? ($a$, $b$ are natural numbers) 

## Solution

Let $X_0 = 0$ and $X_n$ be position after $n$ steps. Then $E(X_{n+1} | X_n, \ldots, X_0) = (X_n + 1) \cdot 1/2 + (X_n - 1) \cdot 1/2 = X_n$. Thus, $\{X_n\}$ is a martingale.

Let $Y_n = X_n^2 - n$. Then $E(Y_{n+1} | Y_n, \ldots, Y_0) = (X_n + 1)^2 \cdot 1/2 + (X_n - 1)^2 \cdot 1/2 - n - 1 = Y_n$. Thus, $\{Y_n\}$ is also a martingale.

Let $N = \min \{n > 0 \colon X_n = a \textrm{ or } -b \}$. Let $P_a \colon = P(X_N = a)$ and $P_b \colon = P(X_N = -b) = 1 - P_a$. Then $E(X_N) = a \cdot P_a + (-b) \cdot P_b$.

By Doob's Optional Stopping Theorem, $E(X_N) = E(X_0) = 0$. Thus, $P_a = b / (a+b)$.

By the same argument, $E(Y_N) = E(X_N^2 - N) = a^2 \cdot b / (a+b) + (-b)^2 \cdot a / (a+b) - E(N) = 0$. Thus, $E(N) = ab$.