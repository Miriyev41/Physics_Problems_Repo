# Task 10 – Analysis of motion from numerical data

## Problem Statement

For the measurement data $x(t)=t+\frac{1}{20}t^2$ on the interval $t\in[0,10]$ with a time step of $\Delta t=0.1$:

1. Approximate the velocity using the finite difference method.
2. Approximate the acceleration using the finite difference method.
3. Compare with the analytical solution (if known).
4. Investigate the effect of the time step on accuracy.

## Theory

When the position of an object is known only at discrete time steps $t_i$ separated by a constant interval $\Delta t$, derivatives such as velocity and acceleration cannot be calculated using continuous calculus. Instead, we use numerical approximations called finite differences.

**Velocity (First Derivative):**
1. **Forward Difference:** Approximates the velocity at time $t_i$ by looking ahead to the next point.
   $$
   v_{\text{forward}}(t_i) \approx \frac{x(t_{i+1}) - x(t_i)}{\Delta t}
   $$
2. **Central Difference:** Approximates the velocity by looking at the points directly before and after, providing a more symmetric and generally more accurate result.
   $$
   v_{\text{central}}(t_i) \approx \frac{x(t_{i+1}) - x(t_{i-1})}{2\Delta t}
   $$

**Acceleration (Second Derivative):**
Using the central difference applied twice, the second derivative at time $t_i$ can be approximated directly from position data:
$$
a(t_i) \approx \frac{x(t_{i+1}) - 2x(t_i) + x(t_{i-1})}{(\Delta t)^2}
$$

## Step-by-Step Solution

### 1. Analytical Solution

Before performing the numerical approximation, we establish the exact analytical solution to serve as a baseline for comparison.

Given the position function:
$$
x(t) = t + 0.05t^2
$$

The exact velocity is the first time-derivative:
$$
\begin{align}
v(t) &= \frac{dx}{dt} \\
     &= 1 + 2(0.05)t \\
     &= 1 + 0.1t
\end{align}
$$

The exact acceleration is the second time-derivative:
$$
\begin{align}
a(t) &= \frac{dv}{dt} \\
     &= 0.1
\end{align}
$$

### 2. Numerical Velocity (Forward Difference)

Let's evaluate the forward difference approximation for velocity analytically to see its dependence on $\Delta t$:

$$
\begin{align}
v_{\text{num}}(t) &= \frac{x(t + \Delta t) - x(t)}{\Delta t} \\
                  &= \frac{(t + \Delta t) + 0.05(t + \Delta t)^2 - (t + 0.05t^2)}{\Delta t} \\
                  &= \frac{t + \Delta t + 0.05(t^2 + 2t\Delta t + (\Delta t)^2) - t - 0.05t^2}{\Delta t} \\
                  &= \frac{\Delta t + 0.1t\Delta t + 0.05(\Delta t)^2}{\Delta t} \\
                  &= 1 + 0.1t + 0.05\Delta t
\end{align}
$$

### 3. Numerical Acceleration (Central Difference)

Now, let's evaluate the central difference approximation for the second derivative (acceleration):

$$
\begin{align}
a_{\text{num}}(t) &= \frac{x(t + \Delta t) - 2x(t) + x(t - \Delta t)}{(\Delta t)^2} \\
                  &= \frac{(t + \Delta t + 0.05(t + \Delta t)^2) - 2(t + 0.05t^2) + (t - \Delta t + 0.05(t - \Delta t)^2)}{(\Delta t)^2}
\end{align}
$$

Expanding the squares:
$$
\begin{align}
a_{\text{num}}(t) &= \frac{t + \Delta t + 0.05(t^2 + 2t\Delta t + \Delta t^2) - 2t - 0.1t^2 + t - \Delta t + 0.05(t^2 - 2t\Delta t + \Delta t^2)}{(\Delta t)^2} \\
                  &= \frac{0.1t^2 - 0.1t^2 + 0.1t\Delta t - 0.1t\Delta t + 0.1\Delta t^2}{(\Delta t)^2} \\
                  &= \frac{0.1(\Delta t)^2}{(\Delta t)^2} \\
                  &= 0.1
\end{align}
$$

### 4. Comparison and Effect of Time Step ($\Delta t$)

**Velocity Comparison:**
* Exact: $v(t) = 1 + 0.1t$
* Numerical (Forward): $v_{\text{num}}(t) = 1 + 0.1t + 0.05\Delta t$
* Error: $\epsilon_v = |v_{\text{num}}(t) - v(t)| = 0.05\Delta t$

For the given $\Delta t = 0.1$, the error in velocity is exactly $0.05(0.1) = 0.005\ \text{m/s}$. The error is directly proportional to the size of the time step. A smaller $\Delta t$ yields a smaller error, confirming linear convergence $O(\Delta t)$.

**Acceleration Comparison:**
* Exact: $a(t) = 0.1$
* Numerical (Central): $a_{\text{num}}(t) = 0.1$
* Error: $\epsilon_a = 0$

The central difference method for the second derivative produces zero error, regardless of the size of $\Delta t$. This is a known property of the central difference approximation: it perfectly computes the second derivative for any polynomial of degree 2 or less.

## Final Result

- **Analytical Velocity:** $v(t) = 1 + 0.1t$
- **Analytical Acceleration:** $a(t) = 0.1$
- **Numerical Velocity (Forward):** $v_{\text{num}}(t) = 1 + 0.1t + 0.05\Delta t$
- **Numerical Acceleration (Central):** $a_{\text{num}}(t) = 0.1$
- **Error in Velocity:** Scales linearly with $\Delta t$ ($0.05\Delta t$).
- **Error in Acceleration:** Exactly $0$ for this specific quadratic function.

## Interpretation

The finite difference method relies on discrete samples to approximate the local slope of the function. For the forward difference velocity, the slope is measured between $t$ and $t+\Delta t$. Because the true velocity is continuously increasing (due to positive acceleration), the forward secant line always has a slightly steeper slope than the true tangent line at $t$. This leads to a systematic overestimation of the velocity, heavily dependent on how wide the gap ($\Delta t$) is. 

Conversely, the second derivative of a parabola is a constant. Because a parabola curves uniformly, the symmetric nature of the standard central difference formula perfectly captures the constant curvature without any truncation error, completely independent of the sampling rate.