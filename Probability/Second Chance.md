# Second Chance

## Problem

Roll a die, and you get paid what the dice shows. But if you want, you can request a second chance & roll the die again; get paid what the second roll shows instead of the first. What is the expected value? 

## Solution

Expected value of second roll is $3.5$. So if the outcome of first roll is less than $3.5$, request a second chance. 

Thus, the expected value is

$E(X | X1 < 3.5) P(X1 < 3.5) + E(X | X1 > 3.5) P(X1 > 3.5) \\
= 3.5 \times 1/2 + 5 \times 1/2 = 17/4$