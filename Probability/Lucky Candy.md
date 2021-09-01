# Lucky Candy

## Problem

How do you place 50 good candies and 50 rotten candies in two boxes such that if you choose a box at random and take out a candy at random, it better be good!
That means probability of choosing a good candy should be highest. 

## Solution

Let $x$ ($y$) be number of good (rotten) candies in Box $A$. Then there are $50-x$ ($50-y$) good (rotten) candies in Box $B$.

$P(x, y) \colon = P(\textrm{choose good}) = \frac{x}{x+y} \times \frac{1}{2} + \frac{50-x}{100-x-y} \times \frac{1}{2} = (\frac{1}{1+\frac{y}{x}} + \frac{1}{1+\frac{50-y}{50-x}}) \times \frac{1}{2}$

Note $1 \leq x \leq 25$. Want $\frac{y}{x}$ and $\frac{50-y}{50-x}$ to be small. Try $x = 1$, $y = 0$ and $P_{max} = 3/4$.