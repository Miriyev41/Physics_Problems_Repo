# Task 01 – Uniform and uniformly accelerated motion

## Problem Statement

The equation of motion for a particle is given by:

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

The required operations are:

1. Determine the velocity $v(t)$ and acceleration $a(t)$ by differentiation.
2. Given the parameters $x_0 = 0$, $v_0 = 5\ \text{m/s}$, and $a = -2\ \text{m/s}^2$, calculate:
    - The stopping time $t_s$.
    - The maximum displacement $x_{max}$.
    - The behavior of velocity depending on the time and the sign of the acceleration.
3. Visualize the kinematic variables $x(t)$, $v(t)$, and $a(t)$.

## Theory

In kinematics, the state of a particle is described by its position $x(t)$. The velocity $v(t)$ is defined as the first derivative of the position with respect to time:

$$
v(t) = \frac{dx}{dt}
$$

The acceleration $a(t)$ is the first derivative of the velocity, or the second derivative of the position, with respect to time:

$$
a(t) = \frac{dv}{dt} = \frac{d^2x}{dt^2}
$$

For uniformly accelerated motion, the acceleration is constant. A "stopping time" refers to the instant $t_s$ when the instantaneous velocity reaches zero ($v(t_s) = 0$). This point often corresponds to a local extremum in the position function, such as the maximum displacement before the particle reverses direction.

## Step-by-Step Solution

### 1. Derive velocity and acceleration

Start with the position equation:

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

Differentiate with respect to $t$ to find velocity:

$$
\begin{align}
v(t) &= \frac{d}{dt} \left( x_0 + v_0 t + \frac{1}{2} a t^2 \right) \\
     &= 0 + v_0 + \frac{1}{2} a (2t) \\
     &= v_0 + at
\end{align}
$$

Differentiate velocity with respect to $t$ to find acceleration:

$$
\begin{align}
a(t) &= \frac{d}{dt} (v_0 + at) \\
     &= 0 + a \\
     &= a
\end{align}
$$

This confirms that the motion is uniformly accelerated, as the acceleration is independent of time.

### 2. Calculations with given parameters

Given: $x_0 = 0$, $v_0 = 5\ \text{m/s}$, $a = -2\ \text{m/s}^2$.

**Step 1: Calculate the stopping time $t_s$**

The particle stops when $v(t) = 0$:

$$
0 = v_0 + at_s
$$

Substitute the parameters:

$$
\begin{align}
0 &= 5 + (-2)t_s \\
2t_s &= 5 \\
t_s &= 2.5\ \text{s}
\end{align}
$$

**Step 2: Calculate the maximum displacement $x_{max}$**

The maximum displacement occurs at the stopping time $t_s = 2.5\ \text{s}$. Substitute this into the position equation:

$$
\begin{align}
x_{max} &= x(2.5) \\
        &= 0 + 5(2.5) + \frac{1}{2}(-2)(2.5)^2 \\
        &= 12.5 - (6.25) \\
        &= 6.25\ \text{m}
\end{align}
$$

**Step 3: Analyze velocity behavior**

The velocity equation is $v(t) = 5 - 2t$. 

- At $t=0$, the velocity is positive ($5\ \text{m/s}$).
- Because the acceleration is negative ($a = -2\ \text{m/s}^2$), the velocity decreases linearly over time.
- After the stopping time ($t > 2.5\ \text{s}$), the velocity becomes negative, meaning the particle has reversed its direction of motion.

## Final Result

- Velocity: $v(t) = v_0 + at$
- Acceleration: $a(t) = a$
- Stopping time: $t_s = 2.5\ \text{s}$
- Maximum displacement: $x_{max} = 6.25\ \text{m}$

## Interpretation


In this scenario, the particle acts as if it is thrown upward or sliding against friction. The negative acceleration acts as a "deceleration" relative to the initial positive velocity. The position graph is a downward-opening parabola, where the vertex represents the point of maximum displacement and zero velocity. The linear decrease of velocity reflects the constant "drain" on the particle's speed by the uniform acceleration field. Once $v(t)$ crosses the horizontal axis, the particle moves back toward its starting position, eventually crossing $x=0$ again at $t = 5\ \text{s}$.