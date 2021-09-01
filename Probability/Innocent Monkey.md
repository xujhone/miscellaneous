# Innocent Monkey

## Problem

A very innocent monkey throws a fair die. The monkey will eat as many bananas as are shown on the die, from 1 to 5. But if the die shows '6', the monkey will eat 5 bananas and throw the die again. This may continue indefinitely. What is the expected number of bananas the monkey will eat? 

## Solution

Let X be number of bananas.

Then $E(X) = (1+2+3+4+5)/6 + (5 + E(X)) / 6$. Thus, $E(X) = 4$.