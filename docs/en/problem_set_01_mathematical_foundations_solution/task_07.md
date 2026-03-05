# Task 07 – Work of a force along a trajectory

## Problem Statement

A force field is given by $\vec F(x,y) = (y, 2x)$. A particle moves along the trajectory $x = t, y = t^2$ for $t \in [0,1]$.
Determine the velocity vector and calculate the exact work done by the force along the trajectory. Represent the integral as a limit of a Riemann sum suitable for numerical verification.

## Theory

The work $W$ done by a vector force field $\vec F$ on a particle moving along a curve $C$ parameterized by $\vec r(t)$ is defined as the line integral of the force along the path. 

$$
W = \int_C \vec F \cdot d\vec r
$$

This can be transformed into a standard definite time integral by substituting $d\vec r = \vec v(t) dt$:

$$
W = \int_{t_1}^{t_2} \vec F(\vec r(t)) \cdot \vec v(t) \,dt
$$

## Step-by-Step Solution

Determine the velocity vector from the trajectory parameterization.

$$
\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

$$
\vec v(t) = (1, 2t)
$$

Substitute the parametric equations $x = t$ and $y = t^2$ into the force field vector.

$$
\vec F(\vec r(t)) = (y(t), 2x(t))
$$

$$
\vec F(\vec r(t)) = (t^2, 2t)
$$

Calculate the dot product of the force vector and the velocity vector.

$$
\vec F(\vec r(t)) \cdot \vec v(t) = (t^2)(1) + (2t)(2t)
$$

$$
\vec F(\vec r(t)) \cdot \vec v(t) = t^2 + 4t^2
$$

$$
\vec F(\vec r(t)) \cdot \vec v(t) = 5t^2
$$

Integrate this scalar product over the time interval from $t=0$ to $t=1$.

$$
W = \int_0^1 5t^2 \,dt
$$

$$
W = \left[ \frac{5}{3}t^3 \right]_0^1
$$

$$
W = \frac{5}{3}(1)^3 - \frac{5}{3}(0)^3
$$

$$
W = \frac{5}{3}
$$

To formulate this as a Riemann sum for a JavaScript implementation, divide the interval $[0,1]$ into $N$ steps of size $\Delta t = \frac{1}{N}$.

$$
W \approx \sum_{i=1}^{N} \vec F(\vec r(t_i)) \cdot \vec v(t_i) \Delta t
$$

$$
W \approx \sum_{i=1}^{N} 5t_i^2 \Delta t
$$

Where $t_i = i\Delta t$.

## Final Result

* Velocity: $\vec v(t) = (1, 2t)$
* Analytical Work: $W = \frac{5}{3}$
* Riemann sum formulation: $\lim_{N \to \infty} \sum_{i=1}^{N} 5\left(\frac{i}{N}\right)^2 \frac{1}{N}$

## Interpretation

The positive sign of the work indicates that the force field transfers energy to the particle, increasing its kinetic energy as it traverses the parabolic path. Because the integrand simplifies strictly to a polynomial function of $t$, numerical methods iterating the Riemann sum will rapidly converge to $1.666...$, providing a robust test case for verifying custom integration algorithms against exact analytical baselines.