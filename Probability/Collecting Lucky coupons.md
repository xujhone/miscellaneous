# Collecting Lucky coupons

## Problem

A soda company is holding a contest where everyone who collects one each of N different coupons wins some prize. You get a coupon with each purchase of a soda, and each coupon is equally likely. What’s the expected number of soda bottles you have to buy in order to collect all the coupons? 

## Solution

Let $X_n$ be number of soda bottles to collect $n$ coupons.

Let $Y$ be the number of soda bottles to collect $n$^th coupon after collecting $n-1$ coupons. Thus, $Y \sim \mathrm{Geom}(\frac{N-n+1}{N})$ and $X_n = X_{n-1} + Y$.

Then $E(X_n) = E(X_{n-1}) + E(Y) = E(X_{n-1}) + \frac{N}{N-n+1}$.

Thus, $E(X_N) = \sum_{n=1}^{N} \frac{N}{N-n+1} = \sum_{n=1}^{N} \frac{N}{n}$.



