# Distance from North Pole

## Problem

What is the expected distance of any point on Earth and the north pole? Take Earth radius 1.

Clarification: Shortest distance cuts through the sphere, instead of lying on surface.

Further thinking: Is this question same as choosing two random points on unit sphere and asking their expected distance?

## Solution

### Shortest distance cuts through the sphere

Let $\theta$ be the angle between a point and $z$ axis. Then the shortest distance cuts through the sphere from the point to the north pole is $\sqrt{2-2\mathrm{cos}(\theta)} = 2 \mathrm{sin}\frac{\theta}{2}$.

Thus, the expected distance is $\frac{1}{4\pi}\int_{0}^{\pi} 2 \mathrm{sin}\frac{\theta}{2} \cdot 2 \pi \mathrm{sin} \theta d\theta = 4/3$.

Condition on the first point, the expected distance is $4/3$. Then since the first point is uniformly random, the expected distance of two random points is also $4/3$.

### Shortest distance on surface

Then the shortest distance on surface from the point to the north pole is $\theta$.

Thus, the expected distance is $\frac{1}{4\pi}\int_{0}^{\pi} \theta \cdot 2 \pi \mathrm{sin} \theta d\theta = \pi / 2$.

