# Drunk Passenger

## Problem

A line of 100 airline passengers is waiting to board a plane. They each hold a ticket to one of the 100 seats on that flight. For convenience, let's say that the nth passenger in line has a ticket for the seat number 'n'. Being drunk, the first person in line picks a random seat (equally likely for each seat). All of the other passengers are sober, and will go to their proper seats unless it is already occupied; If it is occupied, they will then find a free seat to sit in, at random.
What is the probability that the last (100th) person to board the plane will sit in their proper seat (#100)?

## Solution

If there are only two passengers, then $P_2 = 1/2$.

If there are three passengers, then $P_3 = 1/3 + 1/3 \times P_2 + 1/3 \times 0 = 1/2$.

Let $P_n$ be the probability that the last person will sit in the last seat.

$P_n = \sum_{i = 2}^{n-1} 1/n \times P_{n-i} = 1/2$.
