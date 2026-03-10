# Task 07 – Work of a Force Along a Trajectory

## Problem Statement

A force field and a trajectory are given by:

$$
\vec F(x,y) = (y, 2x)
$$

$$
x(t) = t, \qquad y(t) = t^2, \qquad t \in [0,1]
$$

1. Determine the velocity vector $\vec v(t)$.
2. Calculate the work done by the force $\vec{F}$ along the trajectory, given by the line integral:

$$
W = \int_{C} \vec{F} \cdot d\vec{r}
$$
3. Write the integral as the limit of a Riemann sum and calculate its value numerically in an HTML/JS application, comparing it with the analytical result.

## Theory

The work $W$ done by a force field $\vec F$ on a particle moving along a curve $C$ is calculated using a line integral. If the curve is parameterized by a position vector $\vec r(t)$ from $t=a$ to $t=b$, the differential displacement is $d\vec r = \vec v(t) dt$, where $\vec v(t)$ is the velocity vector. 

The line integral then transforms into a standard definite integral over the parameter $t$:

$$
W = \int_a^b \vec F(\vec r(t)) \cdot \vec v(t) \, dt
$$

Numerically, a definite integral can be approximated by a Riemann sum. By dividing the interval $[a, b]$ into $N$ subintervals of width $\Delta t$, the continuous integral is approximated by a discrete sum of the function values multiplied by $\Delta t$:

$$
\int_a^b f(t) \, dt \approx \sum_{i=0}^{N-1} f(t_i) \Delta t
$$

In the limit as $N \to \infty$ (and $\Delta t \to 0$), the Riemann sum converges to the exact value of the integral.

## Step-by-Step Solution

### 1. Velocity vector

The position vector is $\vec r(t) = (t, t^2)$. Differentiating with respect to time $t$:

$$
\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right) = (1, 2t)
$$

### 2. Work calculated analytically

First, express the force vector $\vec F(x,y) = (y, 2x)$ in terms of the parameter $t$ by substituting $x(t) = t$ and $y(t) = t^2$:

$$
\vec F(\vec r(t)) = (t^2, 2t)
$$

Next, compute the dot product of the force and velocity vectors:

$$
\begin{align}
\vec F(\vec r(t)) \cdot \vec v(t) &= (t^2, 2t) \cdot (1, 2t) \\
                                  &= (t^2)(1) + (2t)(2t) \\
                                  &= t^2 + 4t^2 \\
                                  &= 5t^2
\end{align}
$$

Now, integrate this dot product over the interval $t \in [0,1]$:

$$
\begin{align}
W &= \int_0^1 5t^2 \, dt \\
  &= 5 \left[ \frac{t^3}{3} \right]_0^1 \\
  &= 5 \left( \frac{1}{3} - 0 \right) \\
  &= \frac{5}{3}
\end{align}
$$

### 3. Integral as the limit of a Riemann sum

Let the interval $[0,1]$ be partitioned into $N$ equal subintervals of width $\Delta t = \frac{1}{N}$. Let $t_i = i \Delta t$ for $i = 0, 1, \dots, N-1$. 

The work integral can be written as the limit of a Riemann sum:

$$
W = \lim_{N \to \infty} \sum_{i=0}^{N-1} \vec F(\vec r(t_i)) \cdot \vec v(t_i) \Delta t
$$

Substituting the dot product derived above:

$$
W = \lim_{N \to \infty} \sum_{i=0}^{N-1} 5t_i^2 \Delta t
$$

This sum will be implemented in the numerical calculation.

## Final Result

- **Velocity vector:** $\vec v(t) = (1, 2t)$
- **Analytical work:** $W = \frac{5}{3} \approx 1.6667$
- **Riemann sum formulation:** $W = \lim_{N \to \infty} \sum_{i=0}^{N-1} 5t_i^2 \Delta t$

## Interpretation

The force field $\vec F(x,y) = (y, 2x)$ performs positive work on the particle moving along the parabola $y = t^2$. Because both components of the force vector $(t^2, 2t)$ and both components of the displacement vector $d\vec r = (1, 2t) dt$ are positive in the first quadrant, their dot product is strictly positive, meaning the force continuously acts to add energy to the particle. The exact calculated energy added is exactly $5/3$ units.