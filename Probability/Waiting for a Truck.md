# Waiting for a Truck

## Problem

On a given highway, trucks arrive at the station according to a Poisson process with Lambda = 0.1/minute. This means that after a truck is just passed, the time for the next truck to arrive is an exponential random number with average arrival time of 10 minutes. Your car just broke on this highway, and you are waiting for the next truck for hitchhiking, what is your expected waiting time? On average how many minutes ago the last truck left? 

## Solution

Let $X \sim \textrm{Possion}(0.1)$, i.e., $P(X=k) = \frac{0.1^k e^{-0.1}}{k!}$ for $k = 0, 1, 2, \ldots$

