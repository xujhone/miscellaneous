# Drunk Ant

## Problem

An ant is standing on one corner of a cube & can only walk on the edges. The ant is drunk and from any corner, it moves randomly by choosing any edge! What is the expected number of edges the ant travels, to reach the opposite corner? 

## Solution

Denote the vertices of the cube by $A, B, C, D, E, F, G, H$.

By symmetry, vertices are divided into 4 groups: $\{A\}, \{B, D, E\}, \{C, F, H\}, \{G\}$.

Let $x_1, x_2, x_3$ be the expected number of edges from $A, B, C$ to $G$ respectively.

By the first step analysis,

$\begin{equation}
    \begin{cases}
        x_1 = x_2 + 1 \\
        x_2 = (x_1 + 2 x_3) / 3 + 1 \\
        x_3 = 2 x_2 / 3 + 1 \\
    \end{cases}
\end{equation}$

$x_1 = 10, x_2 = 9, x_3 = 7$