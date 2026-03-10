# Task 01 – Uniform and uniformly accelerated motion

## Problem Statement

The equation of motion is given:

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

1. Determine the velocity $v(t)$ and acceleration $a(t)$.
2. For the given parameters $x_0=0$, $v_0=5\ \text{m/s}$, $a=-2\ \text{m/s}^2$:
   * calculate the stopping time,
   * calculate the maximum velocity depending on the time and the sign of the acceleration,
   * calculate the maximum displacement.
3. Visualize $x(t)$, $v(t)$, $a(t)$.

## Theory

Kinematics describes motion through the fundamental relationships between position, velocity, and acceleration. Velocity is defined as the first time derivative of position, representing the rate of change of displacement. Acceleration is defined as the first time derivative of velocity, or the second time derivative of position, representing the rate of change of velocity.

A fundamental property of calculus is that a continuous, differentiable function reaches a local extremum (maximum or minimum) when its first derivative is equal to zero. Therefore, a particle reaches its maximum displacement precisely at the moment when its velocity is zero (the turning point).

## Step-by-Step Solution

### 1. General expressions for velocity and acceleration

To determine the velocity $v(t)$, compute the first derivative of the position function $x(t)$ with respect to time $t$:

$$
\begin{align}
v(t) &= \frac{dx}{dt} \\
     &= \frac{d}{dt} \left( x_0 + v_0 t + \frac{1}{2} a t^2 \right) \\
     &= 0 + v_0 + \frac{1}{2} a (2t) \\
     &= v_0 + a t
\end{align}
$$

To determine the acceleration $a(t)$, compute the derivative of the velocity function $v(t)$ with respect to time $t$:

$$
\begin{align}
a(t) &= \frac{dv}{dt} \\
     &= \frac{d}{dt} (v_0 + a t) \\
     &= a
\end{align}
$$

This confirms that the constant $a$ in the polynomial represents the constant acceleration of the object.

### 2. Analysis with specific parameters

Substitute the given values $x_0 = 0$, $v_0 = 5$, and $a = -2$ into the kinematic equations:

$$
x(t) = 5t - t^2
$$

$$
v(t) = 5 - 2t
$$

$$
a(t) = -2
$$

**Stopping time:**
The object stops when its velocity reaches zero. Set $v(t) = 0$ and solve for $t$:

$$
\begin{align}
5 - 2t &= 0 \\
2t &= 5 \\
t &= 2.5\ \text{s}
\end{align}
$$

The stopping time is $t = 2.5\ \text{s}$.

**Maximum velocity:**
Assuming the analysis begins at $t = 0\ \text{s}$, the acceleration is negative ($a = -2\ \text{m/s}^2$). Because the acceleration is constant and strictly negative, the velocity decreases linearly over time. Therefore, the maximum velocity occurs exactly at the initial moment $t = 0$:

$$
v_{max} = v(0) = 5\ \text{m/s}
$$

**Maximum displacement:**
The maximum displacement in the positive direction occurs at the turning point, which corresponds to the stopping time $t = 2.5\ \text{s}$ derived earlier. Substitute this time back into the position equation $x(t)$:

$$
\begin{align}
x_{max} &= x(2.5) \\
        &= 5(2.5) - (2.5)^2 \\
        &= 12.5 - 6.25 \\
        &= 6.25\ \text{m}
\end{align}
$$

## Final Result

- **Velocity equation:** $v(t) = v_0 + at$
- **Acceleration equation:** $a(t) = a$
- **Stopping time:** $2.5\ \text{s}$
- **Maximum velocity:** $5\ \text{m/s}$ (at $t=0$)
- **Maximum displacement:** $6.25\ \text{m}$

## Interpretation

The negative acceleration indicates that the force acting on the body opposes its initial velocity, characteristic of a braking process or motion under a uniform opposing force (such as an object sliding to a halt under kinetic friction). The object travels forward, decelerating linearly until it comes to a complete, instantaneous stop at $2.5\ \text{s}$, having covered a total distance of $6.25\ \text{m}$. If the equations are allowed to continue past this point without assuming a physical barrier, the negative velocity implies the object will reverse direction and accelerate back towards the origin.