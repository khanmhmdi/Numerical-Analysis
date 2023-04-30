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

# Fourier series
The Fourier formula expresses a periodic function $f(t)$ as a sum of sine and cosine waves with different frequencies, amplitudes, and phases. The formula is given by:

$$f(t) = \frac{a_0}{2} + \sum_{n=1}^{\infty} \left(a_n \cos\left(\frac{2\pi n t}{T}\right) + b_n \sin\left(\frac{2\pi n t}{T}\right)\right)$$

where $T$ is the period of the function, $a_0$, $a_n$, and $b_n$ are the Fourier coefficients given by the formulas:

$$a_0 = \frac{1}{T}\int_{-T/2}^{T/2}f(t)dt$$

$$a_n = \frac{2}{T}\int_{-T/2}^{T/2}f(t)\cos\left(\frac{2\pi n t}{T}\right)dt$$

$$b_n = \frac{2}{T}\int_{-T/2}^{T/2}f(t)\sin\left(\frac{2\pi n t}{T}\right)dt$$

The terms $\cos\left(\frac{2\pi n t}{T}\right)$ and $\sin\left(\frac{2\pi n t}{T}\right)$ represent harmonic waves with frequencies $\frac{n}{T},, n \in \mathbb{Z}$, and the coefficients $a_n$ and $b_n$ represent the amplitudes and phases of these waves. The term $\frac{a_0}{2}$ represents the average value of the function over one period.

The Fourier formula is a powerful tool for analyzing and manipulating periodic functions. It allows us to break down complex functions into simpler components, and to reconstruct functions from their Fourier coefficients. It is widely used in many areas of science and engineering, including signal processing, audio and image compression, and quantum mechanics.

## How to approximate the functions with Fourier series?
* Identify the period of the function:
   Let $T$ be the period of the function.
* Determine the coefficients of the Fourier series:
   * The Fourier series coefficients $a_0$, $a_n$, and $b_n$ can be calculated using the following formulas:
     $$a_0 = \frac{1}{T}\int_{-T/2}^{T/2}f(t)dt$$
     $$a_n = \frac{2}{T}\int_{-T/2}^{T/2}f(t)\cos\left(\frac{2\pi n t}{T}\right)dt$$
     $$b_n = \frac{2}{T}\int_{-T/2}^{T/2}f(t)\sin\left(\frac{2\pi n t}{T}\right)dt$$
   * Here, $f(t)$ is the periodic function we want to approximate, and $n$ is a non-negative integer.
* Construct the Fourier series:

 * The Fourier series for $f(t)$ is given by:
   $$f(t) \approx \frac{a_0}{2} + \sum_{n=1}^{\infty} \left(a_n \cos\left(\frac{2\pi n t}{T}\right) + b_n \sin\left(\frac{2\pi n t}{T}\right)\right)$$

* Choose the number of terms:
  Let $N$ be the number of terms we include in the Fourier series.
* Evaluate the approximation:
  The accuracy of the Fourier series approximation can be evaluated by comparing it with the original function $f(t)$. We can use various measures such as the mean squared error or the maximum error to assess the accuracy of the approximation.


# Hermit Interpolation

Hermit interpolation is a method for constructing a polynomial function that passes through a given set of data points, while also taking into account the first and possibly higher derivatives at those points. The resulting polynomial is typically smoother and more accurate than a polynomial constructed using only the data points themselves.

The resulting Hermit polynomial is guaranteed to pass through all of the data points and to have the specified derivatives at those points. Moreover, it tends to be smoother and more accurate than a polynomial constructed using only the data points themselves, especially when the data points are noisy or irregularly spaced.
Hermit interpolation has a wide range of applications in numerical analysis, including computer graphics, computer-aided design, and physics simulations. It is also commonly used in data analysis and visualization to interpolate between discrete data points and to smooth out noisy data.

Let $\{x_i, y_i, y'_i, y''_i, \ldots, y^{(k)}_i\}$ for $i=0,1,\ldots,n$ be a set of $n+1$ distinct data points and their derivatives up to order $k$. The Hermit polynomial of degree at most $2n+1$ that passes through these points is given by:

$$
p(x) = \sum_{i=0}^n y_i h_i(x) + \sum_{i=0}^n y'_i \hat{h}_i(x)
$$

where $h_i(x)$ and $\hat{h}_i(x)$ are the blending functions defined as:

$$
h_i(x) = (1-2L_i(x) L'_i(x))L_i(x)^2
$$

$$
\hat{h}_i(x) = (x-x_i)L_i(x)^2
$$

and $L_i(x)$ is the Lagrange basis polynomial that satisfies $L_i(x_j) = \delta_{ij}$, where $\delta_{ij}$ is the Kronecker delta.

The blending functions $h_i(x)$ and $\hat{h}_i(x)$ are constructed so that they are equal to one at $x=x_i$ and zero at all other data points, and also satisfy the condition that the Hermit polynomial $p(x)$ has the desired derivatives at each data point. Specifically, the coefficients of $p(x)$ are chosen so that $p^{(m)}(x_i) = y^{(m)}_i$ for $m=0,1,\ldots,k$.

By construction, the resulting Hermit polynomial $p(x)$ passes through all of the given data points and has the specified derivatives at each point. Moreover, it tends to be smoother and more accurate than a polynomial constructed using only the data points themselves.

# Lagrange Interpolation
Lagrange interpolation is a method of approximating a function using a polynomial that passes through a set of given data points. The goal of interpolation is to estimate the value of a function at a point within a given interval, based on a limited number of data points. In other words, interpolation allows us to estimate values of a function at points where we do not have direct measurements. The Lagrange interpolation method is particularly useful because it is simple and straightforward to implement, and can be used to approximate a wide range of functions.

Given $n+1$ distinct data points $\{(x_0, y_0), (x_1, y_1), \ldots, (x_n, y_n)\}$, where $x_i \neq x_j$ for $i \neq j$, the Lagrange interpolation polynomial $P(x)$ of degree at most $n$ that passes through these points is given by:

$$
P(x) = \sum_{i=0}^n y_i L_i(x),
$$

where $L_i(x)$ are the Lagrange basis polynomials defined as:

$$
L_i(x) = \prod_{j=0, j \neq i}^n \frac{x - x_j}{x_i - x_j}.
$$

The Lagrange basis polynomials are constructed so that $L_i(x_j) = \delta_{ij}$, where $\delta_{ij}$ is the Kronecker delta. That is, $L_i(x)$ is equal to $1$ when $x = x_i$, and is equal to $0$ when $x = x_j$ for all $j \neq i$. Therefore, the Lagrange interpolation polynomial $P(x)$ constructed using these basis polynomials passes through all of the given data points.

One important property of the Lagrange interpolation polynomial is that it is unique, meaning that there is only one polynomial of degree at most $n$ that passes through a given set of $n+1$ distinct data points. This property makes Lagrange interpolation a useful tool for approximating functions and for numerical integration.

However, one potential drawback of Lagrange interpolation is that the complexity of the polynomial increases rapidly as the number of data points increases. This can lead to numerical instability and inaccurate results, particularly when the data is noisy or when the degree of the polynomial is very high. Other methods, such as spline interpolation, may be more appropriate in these cases.

# Refrences 
[1] Weisstein, Eric W. "Hermite Polynomial." From MathWorld--A Wolfram Web Resource. https://mathworld.wolfram.com/HermitePolynomial.html

[2] Press, W. H., et al. "Numerical Recipes in C: The Art of Scientific Computing." 2nd ed., Cambridge University Press, 1992.

[3] Atkinson, K. E. (1989). An Introduction to Numerical Analysis (2nd ed.). John Wiley & Sons. ISBN 0-471-50023-2.

[4] Burden, R. L., & Faires, J. D. (2000). Numerical Analysis (7th ed.). Brooks/Cole. ISBN 0-534-38216-9.

[5] Conte, S. D., & de Boor, C. (1980). Elementary Numerical Analysis: An Algorithmic Approach (3rd ed.). McGraw-Hill. ISBN 0-07-012447-7.

[6] Davis, P. J. (1963). Interpolation and Approximation. Dover Publications. ISBN 0-486-60172-5.

[7] Stoer, J., & Bulirsch, R. (2002). Introduction to Numerical Analysis (3rd ed.). Springer-Verlag. ISBN 0-387-95452-X.

