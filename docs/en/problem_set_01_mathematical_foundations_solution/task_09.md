# Task 09 – Harmonic Oscillator

## Problem Statement

Given the differential equation for a harmonic oscillator:

$$
\frac{d^2 x}{dt^2} + \omega^2 x = 0
$$

1. Find the general solution.
2. Solve for the given initial conditions (let us assume general initial conditions $x(0) = x_0$ and $x'(0) = v_0$).
3. Visualize in an HTML/JS application: $x(t)$, $x'(t)$, $x''(t)$ for selected parameters and initial conditions.

## Theory

The given equation is a second-order, linear, homogeneous ordinary differential equation with constant coefficients. It is the fundamental equation of motion for a simple harmonic oscillator, such as a mass on a spring (where $\omega^2 = k/m$) or an ideal pendulum for small angles.

To solve such equations, we use the characteristic equation method. Assuming a solution of the form $x(t) = e^{rt}$, we substitute it into the differential equation to find the allowed values of $r$. When the roots of the characteristic equation are purely imaginary, the solution takes the form of oscillating sine and cosine functions.

The position $x(t)$, velocity $v(t) = x'(t)$, and acceleration $a(t) = x''(t)$ of a harmonic oscillator are continuous, periodic functions.

## Step-by-Step Solution

### 1. General solution

Assume a solution of the form:

$$
x(t) = e^{rt}
$$

Substitute this into the differential equation:

$$
r^2 e^{rt} + \omega^2 e^{rt} = 0
$$

Divide by $e^{rt}$ (which is never zero) to get the characteristic equation:

$$
r^2 + \omega^2 = 0
$$

Solving for $r$ yields purely imaginary roots:

$$
r = \pm i\omega
$$

The general solution is a linear combination of the complex exponentials $e^{i\omega t}$ and $e^{-i\omega t}$. Using Euler's formula, this can be written entirely in terms of real-valued sine and cosine functions:

$$
x(t) = A \cos(\omega t) + B \sin(\omega t)
$$

where $A$ and $B$ are arbitrary real constants determined by the initial conditions.

### 2. Solving for initial conditions

Let the initial position be $x(0) = x_0$ and the initial velocity be $x'(0) = v_0$.

First, substitute $t = 0$ into the general solution to find $A$:

$$
\begin{align}
x(0) &= A \cos(0) + B \sin(0) \\
x_0 &= A(1) + B(0) \\
A &= x_0
\end{align}
$$

Next, differentiate the general solution to find the velocity $x'(t)$:

$$
x'(t) = -A\omega \sin(\omega t) + B\omega \cos(\omega t)
$$

Substitute $t = 0$ into the velocity equation to find $B$:

$$
\begin{align}
x'(0) &= -A\omega \sin(0) + B\omega \cos(0) \\
v_0 &= -A\omega(0) + B\omega(1) \\
v_0 &= B\omega \\
B &= \frac{v_0}{\omega}
\end{align}
$$

Substitute $A$ and $B$ back into the general solution to get the particular solution:

$$
x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)
$$

### 3. Deriving velocity and acceleration

For the visualization, we need explicit formulas for $x'(t)$ and $x''(t)$:

Velocity $x'(t)$:

$$
x'(t) = -x_0\omega \sin(\omega t) + v_0 \cos(\omega t)
$$

Acceleration $x''(t)$:

$$
\begin{align}
x''(t) &= \frac{d}{dt} \left( -x_0\omega \sin(\omega t) + v_0 \cos(\omega t) \right) \\
       &= -x_0\omega^2 \cos(\omega t) - v_0\omega \sin(\omega t) \\
       &= -\omega^2 \left( x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t) \right) \\
       &= -\omega^2 x(t)
\end{align}
$$

This verifies that our solution satisfies the original differential equation.

## Final Result

- **General solution:** $x(t) = A \cos(\omega t) + B \sin(\omega t)$
- **Solution for initial conditions $x(0)=x_0$, $x'(0)=v_0$:**
  $$
  x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)
  $$
- **Velocity:** $x'(t) = -x_0\omega \sin(\omega t) + v_0 \cos(\omega t)$
- **Acceleration:** $x''(t) = -\omega^2 x(t)$

## Interpretation

The parameter $\omega$ represents the angular frequency of the oscillator, dictating how fast the system oscillates. Higher $\omega$ means faster oscillations and a shorter period $T = \frac{2\pi}{\omega}$.

The functions for position, velocity, and acceleration are inherently out of phase. When the position $x(t)$ is at a maximum or minimum, the velocity $x'(t)$ is zero, and the acceleration $x''(t)$ is at its maximum magnitude but points in the opposite direction of the displacement. This "restoring force" behavior is exactly what causes the sustained harmonic motion.