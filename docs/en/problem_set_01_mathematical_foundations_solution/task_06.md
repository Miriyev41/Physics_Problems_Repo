# Task 06 – Curve Length and Numerical Integration

## Problem Statement

A parametric trajectory in 2D is given by:

$$
x(t) = t, \qquad y(t) = t^2, \qquad t \in [0,1]
$$

1. Determine the velocity vector $\vec v(t) = \frac{d\vec r}{dt}$.
2. Determine the magnitude of the velocity $|\vec v(t)|$.
3. Write the arc length of the trajectory as an integral $s = \int_0^1 |\vec v(t)| \, dt$.
4. Calculate this integral analytically.
5. Implement the trapezoidal rule in HTML/JS to calculate the arc length, check convergence, and plot the error as a function of the number of divisions $N$.

## Theory

The arc length of a parametric curve from $t=a$ to $t=b$ is the integral of the particle's speed (the magnitude of the velocity vector) over that time interval. 

The trapezoidal rule is a numerical integration method that approximates the area under a curve by dividing the total area into $N$ trapezoids rather than rectangles. The formula for the trapezoidal approximation of an integral $\int_a^b f(t) dt$ is:

$$
\int_a^b f(t) \, dt \approx \frac{h}{2} \left( f(t_0) + 2 \sum_{i=1}^{N-1} f(t_i) + f(t_N) \right)
$$

where $h = \frac{b - a}{N}$ is the step size, and $t_i = a + i \cdot h$.

## Step-by-Step Solution

### 1. Velocity vector

The position vector is $\vec r(t) = (t, t^2)$. Differentiating each component with respect to $t$ yields the velocity vector:

$$
\vec v(t) = \left( \frac{d}{dt}(t), \frac{d}{dt}(t^2) \right) = (1, 2t)
$$

### 2. Magnitude of the velocity

The magnitude of the velocity vector (the speed) is calculated using the Euclidean norm:

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2} = \sqrt{1 + 4t^2}
$$

### 3. Arc length integral

Substituting the speed into the arc length formula:

$$
s = \int_0^1 \sqrt{1 + 4t^2} \, dt
$$

### 4. Analytical calculation

To solve the integral $\int \sqrt{1 + 4t^2} \, dt$, we use a trigonometric substitution. Let $2t = \tan \theta$. Then the differential is $2 \, dt = \sec^2 \theta \, d\theta$, which gives $dt = \frac{1}{2} \sec^2 \theta \, d\theta$.

Substitute these into the integral:

$$
\begin{align}
\int \sqrt{1 + \tan^2 \theta} \left( \frac{1}{2} \sec^2 \theta \right) d\theta &= \frac{1}{2} \int \sqrt{\sec^2 \theta} \sec^2 \theta \, d\theta \\
&= \frac{1}{2} \int \sec^3 \theta \, d\theta
\end{align}
$$

The integral of $\sec^3 \theta$ is a standard result obtained via integration by parts:

$$
\int \sec^3 \theta \, d\theta = \frac{1}{2} \sec \theta \tan \theta + \frac{1}{2} \ln |\sec \theta + \tan \theta|
$$

Applying this to our expression:

$$
\frac{1}{2} \int \sec^3 \theta \, d\theta = \frac{1}{4} \sec \theta \tan \theta + \frac{1}{4} \ln |\sec \theta + \tan \theta|
$$

Convert back to the variable $t$ using the relations $\tan \theta = 2t$ and $\sec \theta = \sqrt{1 + \tan^2 \theta} = \sqrt{1 + 4t^2}$:

$$
\int \sqrt{1 + 4t^2} \, dt = \frac{1}{4} \left( 2t \sqrt{1 + 4t^2} + \ln \left| \sqrt{1 + 4t^2} + 2t \right| \right)
$$

Now, evaluate the definite integral from $t = 0$ to $t = 1$:

$$
\begin{align}
s &= \left[ \frac{1}{4} \left( 2t \sqrt{1 + 4t^2} + \ln \left| \sqrt{1 + 4t^2} + 2t \right| \right) \right]_0^1 \\
  &= \frac{1}{4} \left( 2(1)\sqrt{1 + 4(1)^2} + \ln \left| \sqrt{1 + 4(1)^2} + 2(1) \right| \right) - \frac{1}{4} \left( 0 + \ln |1 + 0| \right) \\
  &= \frac{1}{4} \left( 2\sqrt{5} + \ln(\sqrt{5} + 2) \right) \\
  &= \frac{\sqrt{5}}{2} + \frac{1}{4} \ln(\sqrt{5} + 2)
\end{align}
$$

Approximating the numerical value:

$$
s \approx 1.11803 + 0.25(1.44363) \approx 1.47894
$$

## Final Result

- **Velocity:** $\vec v(t) = (1, 2t)$
- **Speed:** $|\vec v(t)| = \sqrt{1 + 4t^2}$
- **Arc length integral:** $s = \int_0^1 \sqrt{1 + 4t^2} \, dt$
- **Analytical arc length:** $s = \frac{\sqrt{5}}{2} + \frac{1}{4} \ln(\sqrt{5} + 2) \approx 1.47894$

## Interpretation

The exact analytical calculation of arc length often leads to complex integrals, even for simple polynomials like a parabola ($y = t^2$). This highlights the practical necessity of numerical integration methods in physics and engineering. As implemented in the accompanying HTML/JS application, the trapezoidal rule provides an increasingly accurate approximation of this exact value as the number of divisions $N$ increases, with the error decreasing predictably.