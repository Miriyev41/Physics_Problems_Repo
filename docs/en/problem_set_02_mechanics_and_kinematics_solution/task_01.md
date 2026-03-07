# Task 01 – Uniform and Uniformly Accelerated Motion

## Problem Statement

The equation of motion is given by:

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

1. Determine the velocity $v(t)$ and acceleration $a(t)$.
2. For the parameters $x_0 = 0$, $v_0 = 5\ \text{m/s}$, and $a = -2\ \text{m/s}^2$:
    * Calculate the stopping time.
    * Determine the maximum velocity depending on the time and the sign of the acceleration.
    * Calculate the maximum displacement.
3. Visualize $x(t)$, $v(t)$, and $a(t)$.

## Theory

In classical mechanics, the state of a particle is defined by its position, velocity, and acceleration. These quantities are related through differentiation with respect to time $t$.

The velocity is the first derivative of the position:

$$
v(t) = \frac{dx}{dt}
$$

The acceleration is the first derivative of the velocity (and the second derivative of the position):

$$
a(t) = \frac{dv}{dt} = \frac{d^2x}{dt^2}
$$

For uniformly accelerated motion, the acceleration remains constant over time.

## Step-by-Step Solution

### 1. Deriving Velocity and Acceleration

Starting with the position equation:

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

Differentiating with respect to $t$ to find velocity:

$$
v(t) = \frac{d}{dt} \left( x_0 + v_0 t + \frac{1}{2} a t^2 \right)
$$

$$
v(t) = v_0 + at
$$

Differentiating velocity with respect to $t$ to find acceleration:

$$
a(t) = \frac{d}{dt} (v_0 + at)
$$

$$
a(t) = a
$$

### 2. Numerical Calculations

Given: $x_0 = 0$, $v_0 = 5\ \text{m/s}$, $a = -2\ \text{m/s}^2$.

**Stopping Time ($t_s$):**
The body stops when its instantaneous velocity is zero.

$$
0 = v_0 + at_s
$$

$$
t_s = -\frac{v_0}{a} = -\frac{5}{-2} = 2.5\ \text{s}
$$

**Maximum Velocity:**
Since the acceleration $a = -2\ \text{m/s}^2$ is constant and negative, the velocity decreases linearly over time. The "maximum" velocity in the direction of initial motion occurs at $t = 0$.

$$
v_{max} = v(0) = 5\ \text{m/s}
$$

**Maximum Displacement ($x_{max}$):**
Maximum displacement occurs at the stopping time $t_s = 2.5\ \text{s}$.

$$
x_{max} = x(2.5) = 0 + 5(2.5) + \frac{1}{2}(-2)(2.5)^2
$$

$$
x_{max} = 12.5 - 6.25 = 6.25\ \text{m}
$$

### 3. Visualization Description

* **Position $x(t)$**: A parabola opening downwards, starting at the origin, peaking at $(2.5, 6.25)$.
* **Velocity $v(t)$**: A straight line with a negative slope, crossing the t-axis at $t = 2.5$.
* **Acceleration $a(t)$**: A horizontal line at the constant value of $-2$.

## Final Result

* **Velocity**: $v(t) = v_0 + at$
* **Acceleration**: $a(t) = a$
* **Stopping Time**: $2.5\ \text{s}$
* **Maximum Displacement**: $6.25\ \text{m}$

## Interpretation

The negative acceleration acts as a deceleration relative to the initial velocity. The body moves forward while slowing down, momentarily stops at $t = 2.5\ \text{s}$, and would subsequently begin moving in the negative $x$ direction if the acceleration remained applied.