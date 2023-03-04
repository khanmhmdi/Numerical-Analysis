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
# Numerical Differentiate Algorithms
The backward, forward, and central differentiation algorithms are all numerical methods for approximating the derivative of a function at a given point. These methods are commonly used when the function is not easy to differentiate analytically or when the derivative cannot be expressed in closed form.

Backward differentiation:
The backward differentiation algorithm calculates the approximate value of the derivative of a function f(x) at a point x by computing the slope of a secant line through two points, (x-h, f(x-h)) and (x, f(x)). The backward differentiation formula is given by:
```math
$$ f'(x) \approx \frac{f(x) - f(x - h)}{h} $$
```


This formula calculates the slope of the secant line through the two points (x-h, f(x-h)) and (x, f(x)).

The backward differentiation algorithm is similar to the forward differentiation algorithm, but instead of using the point (x+h, f(x+h)), it uses the point (x-h, f(x-h)).

Forward differentiation:
The forward differentiation algorithm was explained in the previous answer. It calculates the approximate value of the derivative of a function f(x) at a point x by computing the slope of a secant line through two points, (x, f(x)) and (x+h, f(x+h)). The forward differentiation formula is given by:

```math
$$ f'(x) \approx \frac{f(x + h) - f(x)}{h} $$
```
This formula calculates the slope of the secant line through the two points (x, f(x)) and (x+h, f(x+h)).

Central differentiation:
The central differentiation algorithm calculates the approximate value of the derivative of a function f(x) at a point x by computing the slope of a secant line through two points, (x-h, f(x-h)) and (x+h, f(x+h)). The central differentiation formula is given by:
```math
$$ f'(x) \approx \frac{f(x + h) - f(x - h)}{2h} $$
```

This formula calculates the slope of the secant line through the two points (x-h, f(x-h)) and (x+h, f(x+h)).

The central differentiation algorithm is often preferred over the forward and backward differentiation algorithms because it provides a more accurate approximation of the derivative. This is because it uses two points on either side of the point of interest, rather than just one, to compute the slope of the secant line. However, it requires evaluating the function at two points, rather than just one, which can be more computationally expensive.
 
 # Taylor Series for function approximation
 The Taylor series for the sine and cosine functions are:

Sine Function:

$$\sin(x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!}x^{2n+1} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots $$

Cosine Function:

$$\cos(x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n)!}x^{2n} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$

Here, the $n$th term in the series is given by $(-1)^n x^{2n+1}/(2n+1)!$ for the sine function, and $(-1)^n x^{2n}/(2n)!$ for the cosine function. The Taylor series represents an infinite sum of terms, where each term depends on the value of $n$ and the value of $x$. The terms get smaller and smaller as $n$ increases, and the series converges to the function for any finite value of $x$.

Using more terms in the Taylor series for approximating the sine and cosine functions leads to a more accurate approximation of these functions.

The Taylor series for the sine and cosine functions are infinite series, so using more terms in the series means including higher-order terms with increasingly smaller coefficients. As we add more and more terms to the series, the approximation becomes more accurate, especially for values of $x$ that are closer to zero.

However, it's important to note that adding more terms to the Taylor series does not necessarily mean that the approximation becomes more accurate for all values of $x$. In fact, for large values of $x$, the approximation may actually become less accurate, as the series terms grow larger and the series becomes less convergent.

In practice, it's often more efficient to use a finite number of terms in the Taylor series that is appropriate for the range of values of $x$ being considered. This can lead to a good balance between accuracy and computational efficiency.


