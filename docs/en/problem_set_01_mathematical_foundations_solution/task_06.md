# Task 06 – Curve length and numerical integration

## Problem Statement

A parametric trajectory in 2D is given:

$$
x(t) = t, \qquad y(t)=t^2, \qquad t\in[0,1]
$$

The required analytical operations are:
1. Determine the velocity vector $\vec v(t) = \frac{d\vec r}{dt}$.
2. Determine the magnitude of the velocity $|\vec v(t)|$.
3. Write the arc length of the trajectory as an integral $s = \int_0^1 |\vec v(t)|\,dt$.
4. Calculate this integral analytically (if possible) or reduce it to a form that requires a numerical method.

The required computational operations (implemented separately) are:
5. Implement the trapezoidal rule in HTML/JS to calculate $s$, check convergence with increasing divisions $N$, and plot the error.

## Theory

The length of a parametric curve (arc length) from $t=a$ to $t=b$ is the integral of the particle's speed over that time interval:

$$
s = \int_a^b |\vec v(t)| \, dt
$$

Where the speed $|\vec v(t)|$ is the magnitude of the velocity vector:

$$
|\vec v(t)| = \sqrt{v_x(t)^2 + v_y(t)^2} = \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}
$$

To integrate expressions of the form $\sqrt{1 + u^2}$, trigonometric substitution is highly effective. By substituting $u = \tan \theta$, we can utilize the trigonometric identity:

$$
1 + \tan^2 \theta = \sec^2 \theta
$$

Additionally, numerical integration methods, such as the trapezoidal rule, approximate the definite integral of a function $f(t)$ by dividing the interval $[a,b]$ into $N$ subintervals of width $\Delta t = \frac{b-a}{N}$. The approximation is given by:

$$
\int_a^b f(t) \, dt \approx \Delta t \left( \frac{f(a) + f(b)}{2} + \sum_{k=1}^{N-1} f(a + k\Delta t) \right)
$$

## Step-by-Step Solution

### 1. Determine the velocity vector $\vec v(t)$

Given the position vector $\vec r(t) = (t, t^2)$. We take the derivative with respect to $t$.

First component:

$$
v_x(t) = \frac{d}{dt}(t) = 1
$$

Second component:

$$
v_y(t) = \frac{d}{dt}(t^2) = 2t
$$

The velocity vector is:

$$
\vec v(t) = \bigl(1, 2t\bigr)
$$

### 2. Determine the magnitude of the velocity $|\vec v(t)|$

Using the Euclidean norm on the velocity vector:

$$
\begin{align}
|\vec v(t)| &= \sqrt{(1)^2 + (2t)^2} \\
            &= \sqrt{1 + 4t^2}
\end{align}
$$

### 3. Write the arc length as an integral

Substitute the velocity magnitude into the arc length formula with the limits $t=0$ to $t=1$:

$$
s = \int_0^1 \sqrt{1 + 4t^2} \, dt
$$

### 4. Calculate the integral analytically

We solve the integral using trigonometric substitution. Let:

$$
2t = \tan \theta \implies t = \frac{1}{2} \tan \theta
$$

The differential $dt$ becomes:

$$
dt = \frac{1}{2} \sec^2 \theta \, d\theta
$$

Substitute these into the square root expression:

$$
\begin{align}
\sqrt{1 + 4t^2} &= \sqrt{1 + \tan^2 \theta} \\
                &= \sqrt{\sec^2 \theta} \\
                &= \sec \theta
\end{align}
$$

Now, substitute back into the indefinite integral $\int \sqrt{1+4t^2} \, dt$:

$$
\begin{align}
\int \sqrt{1 + 4t^2} \, dt &= \int (\sec \theta) \left( \frac{1}{2} \sec^2 \theta \, d\theta \right) \\
                           &= \frac{1}{2} \int \sec^3 \theta \, d\theta
\end{align}
$$

The integral of $\sec^3 \theta$ is a standard result (obtained via integration by parts):

$$
\int \sec^3 \theta \, d\theta = \frac{1}{2} \sec \theta \tan \theta + \frac{1}{2} \ln|\sec \theta + \tan \theta|
$$

Therefore, our integral becomes:

$$
\begin{align}
\frac{1}{2} \int \sec^3 \theta \, d\theta &= \frac{1}{2} \left( \frac{1}{2} \sec \theta \tan \theta + \frac{1}{2} \ln|\sec \theta + \tan \theta| \right) \\
                                          &= \frac{1}{4} \sec \theta \tan \theta + \frac{1}{4} \ln|\sec \theta + \tan \theta|
\end{align}
$$

Now, transform back to the variable $t$. We know $\tan \theta = 2t$ and $\sec \theta = \sqrt{1 + 4t^2}$:

$$
\int \sqrt{1 + 4t^2} \, dt = \frac{1}{4} \left(\sqrt{1 + 4t^2}\right)(2t) + \frac{1}{4} \ln \left| \sqrt{1 + 4t^2} + 2t \right|
$$

Simplify the expression:

$$
\int \sqrt{1 + 4t^2} \, dt = \frac{1}{2} t \sqrt{1 + 4t^2} + \frac{1}{4} \ln \left( 2t + \sqrt{1 + 4t^2} \right)
$$

Finally, evaluate this definite integral from $t = 0$ to $t = 1$.

Upper limit ($t=1$):

$$
\begin{align}
\text{Upper} &= \frac{1}{2}(1)\sqrt{1 + 4(1)^2} + \frac{1}{4} \ln\left(2(1) + \sqrt{1 + 4(1)^2}\right) \\
             &= \frac{\sqrt{5}}{2} + \frac{1}{4} \ln(2 + \sqrt{5})
\end{align}
$$

Lower limit ($t=0$):

$$
\begin{align}
\text{Lower} &= \frac{1}{2}(0)\sqrt{1 + 0} + \frac{1}{4} \ln(0 + \sqrt{1 + 0}) \\
             &= 0 + \frac{1}{4} \ln(1) \\
             &= 0
\end{align}
$$

Subtract the lower limit from the upper limit:

$$
s = \frac{\sqrt{5}}{2} + \frac{1}{4} \ln(2 + \sqrt{5})
$$

## Final Result

* Velocity vector: $\vec v(t) = (1, 2t)$
* Velocity magnitude: $|\vec v(t)| = \sqrt{1 + 4t^2}$
* Integral formulation: $s = \int_0^1 \sqrt{1 + 4t^2} \, dt$
* Analytical length: $s = \frac{\sqrt{5}}{2} + \frac{1}{4} \ln(2 + \sqrt{5}) \approx 1.4789$

## Interpretation

[Image of parabolic trajectory with tangent velocity vectors]

The arc length of a simple parabola ($y = x^2$) results in a non-trivial integral involving a square root of a quadratic. This leads to an analytical solution containing both an algebraic component (representing the linear distance approximation) and a logarithmic component (representing the stretching curvature of the space). Due to the complexity of integrating such radicals analytically, computing arc lengths for more complex curves typically relies entirely on numerical integration, which is why algorithms like the trapezoidal rule are highly valuable in computational physics.