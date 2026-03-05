# Task 09 – Harmonic oscillator

## Problem Statement

A system is governed by the following second-order linear differential equation:

$$
\frac{d^2 x}{dt^2} + \omega^2 x = 0
$$

Find the general solution to this equation. Next, determine the specific solution for arbitrary initial conditions $x(0) = x_0$ and $x'(0) = v_0$. Outline the architecture for an HTML application to visualize the position $x(t)$, velocity $x'(t)$, and acceleration $x''(t)$.

## Theory

The given differential equation describes a simple harmonic oscillator. It models systems where a restoring force is directly proportional to the displacement from equilibrium, such as a mass on a Hookean spring or a simple pendulum under a small-angle approximation.


Because the equation is a second-order linear homogeneous ordinary differential equation with constant coefficients, its solution can be found using an ansatz of the form $x(t) = e^{rt}$, which leads to a characteristic algebraic equation. The roots of this characteristic equation determine the fundamental set of solutions.

## Step-by-Step Solution

Assume a solution of the form $x(t) = e^{rt}$. Substitute this into the differential equation.

$$
r^2 e^{rt} + \omega^2 e^{rt} = 0
$$

Divide by $e^{rt}$, which is never zero, to obtain the characteristic equation.

$$
r^2 + \omega^2 = 0
$$

Solve for $r$.

$$
r^2 = -\omega^2
$$

$$
r = \pm i\omega
$$

The roots are purely imaginary. By Euler's formula, the general solution is a linear combination of sine and cosine functions. Let $A$ and $B$ be arbitrary real constants.

$$
x(t) = A\cos(\omega t) + B\sin(\omega t)
$$

To find the specific solution, apply the initial conditions $x(0) = x_0$ and $x'(0) = v_0$. First, evaluate $x(t)$ at $t=0$.

$$
x(0) = A\cos(0) + B\sin(0)
$$

$$
x_0 = A
$$

Next, compute the first derivative $x'(t)$ to apply the second initial condition.

$$
x'(t) = \frac{d}{dt} \bigl( A\cos(\omega t) + B\sin(\omega t) \bigr)
$$

$$
x'(t) = -A\omega\sin(\omega t) + B\omega\cos(\omega t)
$$

Evaluate $x'(t)$ at $t=0$.

$$
x'(0) = -A\omega\sin(0) + B\omega\cos(0)
$$

$$
v_0 = B\omega
$$

$$
B = \frac{v_0}{\omega}
$$

Substitute the constants $A$ and $B$ back into the general solution to obtain the specific solution.

$$
x(t) = x_0\cos(\omega t) + \frac{v_0}{\omega}\sin(\omega t)
$$

Compute the acceleration $x''(t)$ by differentiating the velocity.

$$
x''(t) = \frac{d}{dt} \left( -x_0\omega\sin(\omega t) + v_0\cos(\omega t) \right)
$$

$$
x''(t) = -x_0\omega^2\cos(\omega t) - v_0\omega\sin(\omega t)
$$

Notice that this satisfies the original differential equation $x''(t) = -\omega^2 x(t)$.

### Application Architecture

To visualize the kinematics of the harmonic oscillator using web technologies:

1.  **Interface (HTML):** Create input fields or sliders for the angular frequency $\omega$, initial position $x_0$, and initial velocity $v_0$. Add a canvas element for rendering the graphs.
2.  **Logic (JavaScript):** Define three functions corresponding to $x(t)$, $x'(t)$, and $x''(t)$ based on the derived specific solutions. 
3.  **Visualization:** Iterate over a time parameter $t$ from $0$ to a maximum value. For each time step, calculate the three kinematic values. Map $t$ to the horizontal canvas pixel coordinate and the physical values to vertical pixel coordinates. Plot the three curves using distinct colors and add a dynamic legend to distinguish position, velocity, and acceleration.

## Final Result

* General solution:

$$
x(t) = A\cos(\omega t) + B\sin(\omega t)
$$

* Specific solution for position:

$$
x(t) = x_0\cos(\omega t) + \frac{v_0}{\omega}\sin(\omega t)
$$

* Velocity:

$$
x'(t) = -x_0\omega\sin(\omega t) + v_0\cos(\omega t)
$$

* Acceleration:

$$
x''(t) = -x_0\omega^2\cos(\omega t) - v_0\omega\sin(\omega t)
$$

## Interpretation

The solution describes perpetual, un-damped oscillations. The parameter $\omega$ determines the angular frequency of the system, setting the period of oscillation $T = \frac{2\pi}{\omega}$. The velocity and acceleration functions are phase-shifted relative to the position; velocity leads position by $\frac{\pi}{2}$ radians, while acceleration is exactly out of phase by $\pi$ radians, reflecting the fact that the restoring force is always directed oppositely to the displacement.