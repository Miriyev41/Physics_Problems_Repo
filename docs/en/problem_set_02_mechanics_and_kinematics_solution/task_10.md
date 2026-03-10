# Task 10 – Analysis of motion from numerical data

## Problem Statement

For the measurement data $x(t) = t + \frac{1}{20}t^2$ on the interval $t \in [0, 10]$ with a time step of $\Delta t = 0.1$:

1. Approximate the velocity using the finite difference method.
2. Approximate the acceleration using the finite difference method.
3. Compare with the analytical solution (if known).
4. Investigate the effect of the time step on accuracy.

## Theory

When the position of an object is known only at discrete time steps $t_i$ separated by a constant interval $\Delta t$, we use numerical approximations called finite differences.



**Velocity (First Derivative):**

1. **Forward Difference:**
$$
v_{\text{forward}}(t_i) \approx \frac{x(t_{i+1}) - x(t_i)}{\Delta t}
$$

2. **Central Difference:**
$$
v_{\text{central}}(t_i) \approx \frac{x(t_{i+1}) - x(t_{i-1})}{2\Delta t}
$$

**Acceleration (Second Derivative):**

$$
a(t_i) \approx \frac{x(t_{i+1}) - 2x(t_i) + x(t_{i-1})}{(\Delta t)^2}
$$

## Step-by-Step Solution

### 1. Analytical Solution

Given the position function:
$$
x(t) = t + 0.05t^2
$$

The exact velocity is:
$$
\begin{aligned}
v(t) &= \frac{dx}{dt} \\
&= 1 + 2(0.05)t \\
&= 1 + 0.1t
\end{aligned}
$$

The exact acceleration is:
$$
\begin{aligned}
a(t) &= \frac{dv}{dt} \\
&= 0.1
\end{aligned}
$$

### 2. Numerical Velocity (Forward Difference)

$$
\begin{aligned}
v_{\text{num}}(t) &= \frac{x(t + \Delta t) - x(t)}{\Delta t} \\
&= \frac{(t + \Delta t) + 0.05(t + \Delta t)^2 - (t + 0.05t^2)}{\Delta t} \\
&= \frac{t + \Delta t + 0.05(t^2 + 2t\Delta t + (\Delta t)^2) - t - 0.05t^2}{\Delta t} \\
&= \frac{\Delta t + 0.1t\Delta t + 0.05(\Delta t)^2}{\Delta t} \\
&= 1 + 0.1t + 0.05\Delta t
\end{aligned}
$$

### 3. Numerical Acceleration (Central Difference)

$$
\begin{aligned}
a_{\text{num}}(t) &= \frac{x(t + \Delta t) - 2x(t) + x(t - \Delta t)}{(\Delta t)^2} \\
&= \frac{(t + \Delta t + 0.05(t + \Delta t)^2) - 2(t + 0.05t^2) + (t - \Delta t + 0.05(t - \Delta t)^2)}{(\Delta t)^2}
\end{aligned}
$$

Expanding the squares:
$$
\begin{aligned}
a_{\text{num}}(t) &= \frac{t + \Delta t + 0.05(t^2 + 2t\Delta t + \Delta t^2) - 2t - 0.1t^2 + t - \Delta t + 0.05(t^2 - 2t\Delta t + \Delta t^2)}{(\Delta t)^2} \\
&= \frac{0.1t^2 - 0.1t^2 + 0.1t\Delta t - 0.1t\Delta t + 0.1\Delta t^2}{(\Delta t)^2} \\
&= \frac{0.1(\Delta t)^2}{(\Delta t)^2} \\
&= 0.1
\end{aligned}
$$

### 4. Comparison and Effect of Time Step ($\Delta t$)

**Velocity Comparison:**
* Exact: $v(t) = 1 + 0.1t$
* Numerical (Forward): $v_{\text{num}}(t) = 1 + 0.1t + 0.05\Delta t$
* Error: $\epsilon_v = |v_{\text{num}}(t) - v(t)| = 0.05\Delta t$

For $\Delta t = 0.1$, the error is $0.005$. The error is directly proportional to the size of the time step ($O(\Delta t)$).

**Acceleration Comparison:**
* Exact: $a(t) = 0.1$
* Numerical (Central): $a_{\text{num}}(t) = 0.1$
* Error: $\epsilon_a = 0$

## Final Result

* **Analytical Velocity:** $v(t) = 1 + 0.1t$
* **Analytical Acceleration:** $a(t) = 0.1$
* **Numerical Velocity (Forward):** $v_{\text{num}}(t) = 1 + 0.1t + 0.05\Delta t$
* **Numerical Acceleration (Central):** $a_{\text{num}}(t) = 0.1$

## Interpretation

The forward difference velocity systematically overestimates the true velocity for this increasing function. However, the central difference for the second derivative is perfectly accurate for quadratic functions because the truncation error for this method depends on the third derivative, which is zero for a parabola.