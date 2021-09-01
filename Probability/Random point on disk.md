# Random point on disk

## Problem

$x$ and $y$ are two random points selected uniformly between $0$ and $1$. Using them, create a point uniformly random in the disk of radius $1$. (uniform means that the probability density is constant) 

## Solution

### Computation

Think of $x$ and $y$ as coordinate variables on $xy-$plane. Then $x$ and $y$ being uniformly random is equivalent to $1 dx dy$ being the area form.

Let $r = f(x)$ and $\theta = g(y)$. Then the point in disk is given by $(p, q) \overset{\underset{\mathrm{def}}{}}{=} (r\mathrm{cos}(\theta), r\mathrm{sin}(\theta)) = (f(x)\mathrm{cos}(g(y)), f(x)\mathrm{sin}(g(y)))$. If $p$, $q$ are randomly uniformly, $\frac{1}{\pi} dp dq = dx dy$.

Thus, $\frac{1}{\pi} f'(x)f(x)g'(y) = 1$. Thus, $g'(y)$ and $f'(x)f(x)$ are constant.

Note $g'(y) = 2 \pi$. Then $f'(x)f(x) = 1/2$. Thus, $f(x) = \sqrt{x}$.

Hence, the point $(\sqrt{x}\mathrm{cos}(2\pi y), \sqrt{x}\mathrm{sin}(2\pi y))$ is uniformly random.

### Rigorous Proof

Let $X, Y \overset{\underset{\mathrm{i.i.d.}}{}}{\sim} \mathrm{Unif}(0, 1)$.

First note for each point $p$ in the disk, it has the polar parametrization $p = (r\mathrm{cos}(\theta), r\mathrm{sin}(\theta))$ where $r \in (0, 1)$ and $\theta \in (0, 2\pi)$. 

Also note $x$ and $y$ are independent and so are $r$ and $\theta$. Thus, let $R = f(X)$ and $\Theta = g(Y)$ such that $0 < R < 1$ and $0 < \Theta < 2 \pi$. Then the point in the disk is given by $(R\mathrm{cos}(\Theta), R\mathrm{sin}(\Theta)) = (f(X)\mathrm{cos}(g(Y)), f(X)\mathrm{sin}(g(Y)))$.

### Reversely

First note for each point $p$ in disk, it has the polar parametrization $p = (r\mathrm{cos}(\theta), r\mathrm{sin}(\theta))$ where $r \in (0, 1)$ and $\theta \in (0, 2\pi)$. And the area form is $d(r\mathrm{cos}(\theta)) \wedge d(r\mathrm{sin}(\theta))) = r dr d\theta$.

Also note $x$ and $y$ are independent and so are $r$ and $\theta$. Thus, we let $x = f(r)$ and $y = g(\theta)$. Then the area form defined by $x$ and $y$ is $dx dy = f'(r) g'(\theta) dr d\theta$.

Thus, $f'(r) g'(\theta) dr d\theta = \frac{1}{\pi} r dr d\theta$. Thus, $f'(r) g'(\theta) = \frac{r}{\pi}$. 

Thus, $g'(\theta) = c$ for some constant $c$. Then $y = c \theta$. Since $\theta \in (0, 2\pi)$ and $y \in (0, 1)$, $c = \frac{1}{2\pi}$.

Thus, $f'(r) = 2r$ and $f(r) = r^2$.

Thus, $r = f^{-1}(x) = \sqrt{x}$ and $\theta = g^{-1}(y) = 2\pi y$.

