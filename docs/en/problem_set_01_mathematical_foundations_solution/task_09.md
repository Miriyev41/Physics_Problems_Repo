# Task 09 – Harmonic oscillator

## Problem Statement

The differential equation for a simple harmonic oscillator is given by:

$$
\frac{d^2 x}{dt^2} + \omega^2 x = 0
$$

The required operations are:
1. Find the general solution of the differential equation.
2. Solve for specific initial conditions $x(0) = x_0$ and $v(0) = v_0$.
3. Visualize the results for $x(t)$, $v(t)$, and $a(t)$ in an interactive application.

## Theory

A second-order linear homogeneous differential equation with constant coefficients can be solved using the characteristic equation. For an equation of the form:

$$
a \frac{d^2x}{dt^2} + b \frac{dx}{dt} + cx = 0
$$

The characteristic equation is $ar^2 + br + c = 0$. In the case of the harmonic oscillator, we have $r^2 + \omega^2 = 0$, which leads to purely imaginary roots $r = \pm i\omega$.

According to Euler's formula, $e^{i\omega t} = \cos(\omega t) + i\sin(\omega t)$. The general real-valued solution is a linear combination of these trigonometric functions:

$$
x(t) = A\cos(\omega t) + B\sin(\omega t)
$$

The velocity $v(t)$ and acceleration $a(t)$ are the first and second derivatives of position:

$$
v(t) = \frac{dx}{dt}, \qquad a(t) = \frac{d^2x}{dt^2}
$$

## Step-by-Step Solution

### 1. Find the general solution

The characteristic equation is:

$$
r^2 + \omega^2 = 0
$$

Solving for $r$:

$$
r^2 = -\omega^2
$$

$$
r = \pm i\omega
$$

The general solution is:

$$
x(t) = c_1 e^{i\omega t} + c_2 e^{-i\omega t}
$$

Using Euler's identities and regrouping constants, we express this in terms of real sine and cosine functions:

$$
x(t) = A\cos(\omega t) + B\sin(\omega t)
$$

### 2. Solve for initial conditions

We are given $x(0) = x_0$ and $\dot{x}(0) = v_0$.

**Step 1: Use the position at $t=0$**

Substitute $t=0$ into the general solution:

$$
\begin{align}
x(0) &= A\cos(0) + B\sin(0) \\
x_0  &= A(1) + B(0) \\
A    &= x_0
\end{align}
$$

**Step 2: Find the velocity function**

Differentiate $x(t)$ with respect to $t$:

$$
\begin{align}
v(t) &= \frac{d}{dt}(A\cos(\omega t) + B\sin(\omega t)) \\
     &= -A\omega\sin(\omega t) + B\omega\cos(\omega t)
\end{align}
$$

**Step 3: Use the velocity at $t=0$**

Substitute $t=0$ into the velocity function:

$$
\begin{align}
v(0) &= -A\omega\sin(0) + B\omega\cos(0) \\
v_0  &= 0 + B\omega(1) \\
B    &= \frac{v_0}{\omega}
\end{align}
$$

**Step 4: Combine the constants**

Substitute $A$ and $B$ back into the general solution:

$$
x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)
$$

### 3. Determine acceleration

Differentiate $v(t)$ to find $a(t)$:

$$
\begin{align}
a(t) &= \frac{d}{dt}(-x_0\omega\sin(\omega t) + v_0\cos(\omega t)) \\
     &= -x_0\omega^2\cos(\omega t) - v_0\omega\sin(\omega t)
\end{align}
$$

Factoring out $-\omega^2$:

$$
a(t) = -\omega^2 \left( x_0\cos(\omega t) + \frac{v_0}{\omega}\sin(\omega t) \right)
$$

$$
a(t) = -\omega^2 x(t)
$$

## Final Result

* General solution: $x(t) = A\cos(\omega t) + B\sin(\omega t)$
* Particular solution: $x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)$
* Velocity: $v(t) = -x_0\omega\sin(\omega t) + v_0\cos(\omega t)$
* Acceleration: $a(t) = -\omega^2 x(t)$

## Interpretation

[Image of simple harmonic motion graphs for position, velocity and acceleration]

The motion is periodic with a period $T = \frac{2\pi}{\omega}$. The acceleration is always proportional to the displacement but in the opposite direction; this is the defining characteristic of a restoring force (Hooke's Law). 

Phase Relationships:
- When displacement $x(t)$ is at its maximum, velocity $v(t)$ is zero, and acceleration $a(t)$ is at its negative maximum.
- Velocity leads displacement by a phase of $\pi/2$ (90 degrees).
- Acceleration and displacement are exactly $\pi$ (180 degrees) out of phase.