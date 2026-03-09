# Task 10 – Analysis of motion from numerical data

## Problem Statement

For the measurement data $x(t) = t + \frac{1}{20}t^2$ on the interval $t \in [0, 10]$.

The required operations are:
1. Determine the exact velocity $v(t)$ and acceleration $a(t)$ using differentiation.
2. Calculate the average velocity $\bar{v}$ over the entire interval $[0, 10]$.
3. Use a numerical approach to estimate velocity at $t = 5$ using the symmetric difference quotient:
   $$
   v_{num}(t) = \frac{x(t + \Delta t) - x(t - \Delta t)}{2\Delta t}
   $$
   for $\Delta t = 1$ and $\Delta t = 0.1$.
4. Compare the numerical results with the exact value $v(5)$.

## Theory

The instantaneous velocity $v(t)$ is the derivative of the position function $x(t)$ with respect to time:

$$
v(t) = \frac{dx}{dt} = \lim_{\Delta t \to 0} \frac{x(t + \Delta t) - x(t)}{\Delta t}
$$

The average velocity $\bar{v}$ over an interval $[t_1, t_2]$ is the total displacement divided by the total time:

$$
\bar{v} = \frac{x(t_2) - x(t_1)}{t_2 - t_1}
$$

In experimental physics, we often lack a continuous function and must estimate derivatives from discrete data points. The **Symmetric Difference Quotient** (or central difference) is a common numerical method that provides a more accurate approximation of the derivative at a point than the forward or backward difference:

$$
v_{num}(t) \approx \frac{x(t + \Delta t) - x(t - \Delta t)}{2\Delta t}
$$

The error in this approximation generally decreases as the time step $\Delta t$ becomes smaller.

## Step-by-Step Solution

### 1. Determine exact velocity and acceleration

**Step 1: Differentiate $x(t)$ to find $v(t)$**

Given:
$$
x(t) = t + \frac{1}{20}t^2
$$

Differentiate with respect to $t$:

$$
\begin{align}
v(t) &= \frac{d}{dt} \left( t + \frac{1}{20}t^2 \right) \\
     &= 1 + \frac{1}{20}(2t) \\
     &= 1 + \frac{t}{10}
\end{align}
$$

**Step 2: Differentiate $v(t)$ to find $a(t)$**

$$
\begin{align}
a(t) &= \frac{d}{dt} \left( 1 + \frac{t}{10} \right) \\
     &= 0 + \frac{1}{10} \\
     &= 0.1
\end{align}
$$

### 2. Calculate average velocity $\bar{v}$ on $[0, 10]$

**Step 1: Calculate positions at the boundaries**

At $t_1 = 0$:
$$
x(0) = 0 + \frac{1}{20}(0)^2 = 0
$$

At $t_2 = 10$:
$$
x(10) = 10 + \frac{1}{20}(10)^2 = 10 + \frac{100}{20} = 10 + 5 = 15
$$

**Step 2: Calculate the average**

$$
\begin{align}
\bar{v} &= \frac{x(10) - x(0)}{10 - 0} \\
        &= \frac{15 - 0}{10} \\
        &= 1.5
\end{align}
$$

### 3. Numerical estimation of velocity at $t = 5$

The exact value at $t=5$ is:
$$
v(5) = 1 + \frac{5}{10} = 1.5
$$

**Case A: $\Delta t = 1$**

We need $x(5+1)$ and $x(5-1)$:

$$
x(6) = 6 + \frac{36}{20} = 6 + 1.8 = 7.8
$$

$$
x(4) = 4 + \frac{16}{20} = 4 + 0.8 = 4.8
$$

Apply the formula:

$$
\begin{align}
v_{num} &= \frac{x(6) - x(4)}{2(1)} \\
        &= \frac{7.8 - 4.8}{2} \\
        &= \frac{3}{2} \\
        &= 1.5
\end{align}
$$

**Case B: $\Delta t = 0.1$**

We need $x(5.1)$ and $x(4.9)$:

$$
x(5.1) = 5.1 + \frac{(5.1)^2}{20} = 5.1 + \frac{26.01}{20} = 5.1 + 1.3005 = 6.4005
$$

$$
x(4.9) = 4.9 + \frac{(4.9)^2}{20} = 4.9 + \frac{24.01}{20} = 4.9 + 1.2005 = 6.1005
$$

Apply the formula:

$$
\begin{align}
v_{num} &= \frac{6.4005 - 6.1005}{2(0.1)} \\
        &= \frac{0.3}{0.2} \\
        &= 1.5
\end{align}
$$

### 4. Comparison of results

| Method | $\Delta t$ | Velocity at $t=5$ |
| :--- | :--- | :--- |
| **Exact** | - | $1.5$ |
| **Numerical** | $1.0$ | $1.5$ |
| **Numerical** | $0.1$ | $1.5$ |

In this specific case, the numerical approximation matches the exact value perfectly for both steps.

## Final Result

* Exact velocity: $v(t) = 1 + 0.1t$
* Exact acceleration: $a(t) = 0.1$
* Average velocity on $[0, 10]$: $\bar{v} = 1.5$
* Numerical velocity at $t=5$ ($\Delta t = 1$): $v_{num} = 1.5$
* Numerical velocity at $t=5$ ($\Delta t = 0.1$): $v_{num} = 1.5$

## Interpretation



The reason the symmetric difference quotient provided an exact result even with a large $\Delta t = 1$ is that the position function $x(t)$ is a quadratic polynomial. For any quadratic function $f(t) = At^2 + Bt + C$, the central difference approximation of the first derivative is mathematically exact. This is because the "secant line" passing through $(t-\Delta t)$ and $(t+\Delta t)$ on a parabola is always perfectly parallel to the "tangent line" at the midpoint $t$. In real-world data containing noise or higher-order terms (like $t^3$), smaller $\Delta t$ values would be required to minimize the approximation error.