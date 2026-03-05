# Task 06 – Curve length and numerical integration

## Problem Statement

A parametric trajectory is given by $x(t) = t, y(t) = t^2$ for $t \in [0,1]$.
Determine the velocity vector, its magnitude, and write the arc length as an integral. Reduce the integral to a form suitable for numerical evaluation and outline the implementation of the trapezoidal rule in a web application to study the convergence.

## Theory

The total distance traveled along a continuous parametric curve from time $t_1$ to $t_2$ is the integral of the speed (the magnitude of the velocity vector) with respect to time.

$$
s = \int_{t_1}^{t_2} |\vec v(t)|\,dt
$$

Because integrating combinations of polynomials under square roots often yields complex inverse hyperbolic functions or lacks closed-form elementary solutions entirely, numerical methods like the trapezoidal rule approximate the definite integral by dividing the area under the curve into $N$ small trapezoids.

## Step-by-Step Solution

Compute the velocity vector.

$$
\vec v(t) = \left( \frac{d}{dt}(t), \frac{d}{dt}(t^2) \right)
$$

$$
\vec v(t) = (1, 2t)
$$

Determine the magnitude of the velocity vector.

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2}
$$

$$
|\vec v(t)| = \sqrt{1 + 4t^2}
$$

Write the formula for the arc length $s$.

$$
s = \int_0^1 \sqrt{1 + 4t^2} \,dt
$$

Analytically, this integral evaluates to $\frac{1}{4}\left(2\sqrt{5} + \text{arcsinh}(2)\right) \approx 1.4789$. For a numerical HTML/JS implementation, the domain $[0,1]$ is divided into $N$ intervals of width $\Delta t = \frac{1}{N}$. The trapezoidal sum approximation is:

$$
s \approx \frac{\Delta t}{2} \sum_{k=1}^{N} \left( |\vec v(t_{k-1})| + |\vec v(t_k)| \right)
$$

Where $t_k = k \Delta t$.

### Application Architecture

To fulfill the application requirements using standard web technologies:

1.  **HTML Structure:** Construct input fields to accept the value of $N$, a button to trigger the calculation, and a canvas element for trajectory visualization.
2.  **JavaScript Logic:** * Define a function `speed(t)` returning $\sqrt{1 + 4t^2}$.
    * Implement a `calculateArcLength(N)` function that iterates through the $N$ intervals, summing the trapezoid areas using the formula derived above.
    * Calculate the error by taking the absolute difference between the numerical result and the precise analytical value.
3.  **Visualization:** Use the HTML5 `<canvas>` API or a lightweight charting library to draw the $(x, y)$ coordinate pairs mapping the parabola, and plot the computed error against different $N$ values to confirm quadratic convergence.

## Final Result

* Velocity: $\vec v(t) = (1, 2t)$
* Speed: $|\vec v(t)| = \sqrt{1 + 4t^2}$
* Arc length integral: $s = \int_0^1 \sqrt{1 + 4t^2} \,dt$

## Interpretation

Evaluating the arc length integral exposes the fundamental difficulty of computing trajectory distances analytically, even for simple curves like a parabola. Implementing the numerical integration requires discretizing continuous time into fixed steps. As the number of divisions $N$ approaches infinity, the trapezoidal approximation geometrically converges to the exact geometric arc length.