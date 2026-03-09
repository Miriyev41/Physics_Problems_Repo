# Task 07 – Work of a force along a trajectory

## Problem Statement

A force field and a trajectory are given by:

$$
\vec F(x,y) = (y, 2x)
$$

$$
x = t, \qquad y = t^2, \qquad t \in [0,1]
$$

The required analytical operations are:
1. Determine the velocity vector $\vec v(t)$.
2. Calculate the work done by the force $\vec F$ along the trajectory, i.e., the line integral $W = \int_C \vec F \cdot d\vec r$.
3. Write the integral as the limit of a Riemann sum.

The required computational operation is to calculate the Riemann sum numerically in HTML/JS and compare it with the analytical result.

## Theory

The velocity vector $\vec v(t)$ is the first derivative of the position vector $\vec r(t)$ with respect to time:

$$
\vec v(t) = \frac{d\vec r}{dt} = \left(\frac{dx}{dt}, \frac{dy}{dt}\right)
$$

The work done by a force field $\vec F(x,y)$ on a particle moving along a curve $C$ parameterized by $\vec r(t)$ from $t=a$ to $t=b$ is given by the line integral:

$$
W = \int_C \vec F \cdot d\vec r = \int_a^b \vec F(\vec r(t)) \cdot \vec v(t) \, dt
$$

To evaluate this integral, the force field must be expressed in terms of the parameter $t$ by substituting the trajectory equations $x(t)$ and $y(t)$ into $\vec F(x,y)$.

A definite integral can be formally defined as the limit of a Riemann sum. By dividing the interval $[a, b]$ into $N$ subintervals of equal width $\Delta t = \frac{b-a}{N}$, and choosing the right endpoint of each subinterval $t_i = a + i\Delta t$, the integral is:

$$
\int_a^b f(t) \, dt = \lim_{N \to \infty} \sum_{i=1}^N f(t_i) \Delta t
$$

## Step-by-Step Solution

### 1. Determine the velocity vector $\vec v(t)$

Given the parametric equations for the trajectory $x(t) = t$ and $y(t) = t^2$, compute their derivatives:

$$
v_x(t) = \frac{d}{dt}(t) = 1
$$

$$
v_y(t) = \frac{d}{dt}(t^2) = 2t
$$

The velocity vector is:

$$
\vec v(t) = (1, 2t)
$$

### 2. Calculate the work done by the force analytically

Express the force $\vec F(x,y) = (y, 2x)$ in terms of the parameter $t$. Substitute $x = t$ and $y = t^2$:

$$
\vec F(t) = (t^2, 2t)
$$

Compute the dot product of the force vector and the velocity vector:

$$
\begin{align}
\vec F(\vec r(t)) \cdot \vec v(t) &= (t^2, 2t) \cdot (1, 2t) \\
                                  &= (t^2)(1) + (2t)(2t) \\
                                  &= t^2 + 4t^2 \\
                                  &= 5t^2
\end{align}
$$

Set up and evaluate the definite integral for work $W$ from $t=0$ to $t=1$:

$$
\begin{align}
W &= \int_0^1 5t^2 \, dt \\
  &= 5 \left[ \frac{t^3}{3} \right]_0^1 \\
  &= 5 \left( \frac{1^3}{3} - \frac{0^3}{3} \right) \\
  &= \frac{5}{3}
\end{align}
$$

### 3. Write the integral as the limit of a Riemann sum

We are integrating the function $f(t) = 5t^2$ over the interval $[0, 1]$.

Define the width of each subinterval:

$$
\Delta t = \frac{1 - 0}{N} = \frac{1}{N}
$$

Define the sample points (using right endpoints):

$$
t_i = 0 + i\Delta t = \frac{i}{N}
$$

Construct the Riemann sum:

$$
\begin{align}
S_N &= \sum_{i=1}^N f(t_i) \Delta t \\
    &= \sum_{i=1}^N 5\left(\frac{i}{N}\right)^2 \left(\frac{1}{N}\right) \\
    &= \sum_{i=1}^N 5\left(\frac{i^2}{N^2}\right) \left(\frac{1}{N}\right) \\
    &= \frac{5}{N^3} \sum_{i=1}^N i^2
\end{align}
$$

The integral is the limit of this sum as $N \to \infty$:

$$
W = \lim_{N \to \infty} \frac{5}{N^3} \sum_{i=1}^N i^2
$$

*Note: Using the formula for the sum of squares $\sum i^2 = \frac{N(N+1)(2N+1)}{6}$, the limit evaluates exactly to $\frac{5}{6} \cdot 2 = \frac{5}{3}$, matching the analytical result.*

## Final Result

* Velocity vector: $\vec v(t) = (1, 2t)$
* Analytical work: $W = \frac{5}{3} \approx 1.6667$
* Riemann sum limit: $W = \lim_{N \to \infty} \frac{5}{N^3} \sum_{i=1}^N i^2$

## Interpretation

The work evaluated is positive ($W = 5/3$), which signifies that the vector field $\vec F$ generally points in the same direction as the displacement along the defined trajectory, thus adding energy to the system. Since $\vec F$ is not a conservative field (its curl $\nabla \times \vec F = \frac{\partial (2x)}{\partial x} - \frac{\partial (y)}{\partial y} = 2 - 1 = 1 \neq 0$), the work done depends strictly on the path taken between the origin and the point $(1,1)$.