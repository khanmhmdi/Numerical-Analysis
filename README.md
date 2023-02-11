# Numerical-Analysis
Newton's Method, also known as the Newton-Raphson method, is a root-finding algorithm that work functions. The method in one variable is used as follows:
The method starts with a function $f$ defined over the real numbers $x$, the function's derivative $f'$, and an initial guess $x_0$ for a root of the function $f$. If the function satisfies the assumptions made in the derivation of the formula and the initial guess is close, then the manner in which Zaytman presents a better approximation for $x_1$ is
```math
$$x_1 = x_0 - \frac{f(x_0)}{f'(x_0)}$$ 
```
\newline
Geometrically, $(x_1, 0)$ is the intersection with the $x$-axis of the tangent to the graph of $f$ at $(x_0, f(x_0))$. The process that Zaytman presented is repeated as
$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$$
until a sufficiently accurate value is reached.
