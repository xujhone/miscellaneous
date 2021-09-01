# Witches at the coffee shop

## Problem

Two witches make a nightly visit to an all-night coffee shop. Each arrives at a random time between 0:00 and 1:00. Each one of them stays for exactly 30 minutes. On any one given night, what is the probability that the witches will meet at the coffee shop? 

## Solution

Let X, Y be the arrival time for two witches. 

Then $P(\mathrm{meet}) = P(\mid X-Y \mid \leq 0.5) = \int_{\{\mid x-y \mid \leq 0.5, 0 \leq x, y \leq 1\}} dx dy = 1 - 0.5 \times 0.5 = 0.75$ 
