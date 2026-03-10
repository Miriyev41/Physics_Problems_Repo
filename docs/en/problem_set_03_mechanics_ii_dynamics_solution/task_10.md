# Task 10 – Numerical model of a dynamical system

## Problem Statement

Consider motion in a one-dimensional potential:

$$
U(x)=\frac{k}{2}x^2 + \lambda x^4
$$

1. Determine the force.
2. Write down the equation of motion.
3. Solve the system numerically using an HTML/JS application and explore the phase space for different values of $\lambda$.

## Theory

[Image of anharmonic oscillator potential well]
[Image of phase space for Duffing oscillator]

The given potential represents an **anharmonic oscillator**. The quadratic term $\frac{k}{2}x^2$ corresponds to the standard harmonic oscillator (a linear spring). The quartic term $\lambda x^4$ introduces a non-linear perturbation. 

- If $\lambda > 0$, the potential grows steeper than a parabola, modeling a "hard" spring that becomes increasingly difficult to stretch. 
- If $\lambda < 0$, the potential grows less steeply and eventually turns downwards, modeling a "soft" spring that can break or allow the particle to escape to infinity if the energy is high enough.

For conservative systems, the force is the negative derivative of the potential energy. Because the resulting force depends non-linearly on position ($x^3$), the equation of motion cannot be solved using simple sines and cosines (it requires Jacobi elliptic functions). Therefore, numerical integration is the standard approach to analyze its dynamics.

## Step-by-Step Solution

### 1. Determine the force

The force is the negative spatial derivative of the potential energy:

$$
\begin{align}
F(x) &= -\frac{dU}{dx} \\
     &= -\frac{d}{dx} \left( \frac{k}{2}x^2 + \lambda x^4 \right) \\
     &= -kx - 4\lambda x^3
\end{align}
$$

### 2. Equation of motion

Apply Newton's Second Law ($m\ddot{x} = F(x)$):

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

Dividing by mass $m$, the acceleration is:

$$
\ddot{x} = -\frac{k}{m}x - \frac{4\lambda}{m}x^3
$$

This is a specific form of the Duffing equation (without damping or external driving).

### 3. Numerical Integration (Semi-Implicit Euler)

To solve this numerically in an application, we break the second-order differential equation into two coupled first-order equations:

$$
\frac{dv}{dt} = -\frac{k}{m}x - \frac{4\lambda}{m}x^3
$$

$$
\frac{dx}{dt} = v
$$

A simple and highly stable numerical method for conservative oscillatory systems is the **Euler-Cromer** (or semi-implicit Euler) method. For a small time step $\Delta t$, the updates are:

$$
v_{i+1} = v_i + a(x_i) \Delta t
$$

$$
x_{i+1} = x_i + v_{i+1} \Delta t
$$

Notice that the new velocity $v_{i+1}$ is used to calculate the new position $x_{i+1}$. This slight modification from the standard Euler method ensures that the numerical simulation perfectly conserves the average energy over time, keeping the orbits in phase space closed.

## Final Result

- **Force:** $F(x) = -kx - 4\lambda x^3$
- **Equation of Motion:** $m\ddot{x} + kx + 4\lambda x^3 = 0$
- **Numerical Update Rules:** $v_{new} = v_{old} + \left(-\frac{k}{m}x_{old} - \frac{4\lambda}{m}x_{old}^3\right) \Delta t$
  $x_{new} = x_{old} + v_{new} \Delta t$

## Interpretation

In phase space, when $\lambda = 0$, the orbits are perfect ellipses. 

When $\lambda > 0$, the extra restoring force causes the velocity to change more abruptly at large displacements, squashing the elliptical phase-space orbits into more rectangular, "stadium-like" shapes. The period of oscillation decreases as the amplitude increases (unlike a harmonic oscillator, whose period is independent of amplitude).

When $\lambda < 0$, the restoring force weakens at large $x$. If the total energy is lower than the local maximum of the potential barrier, the particle remains trapped in closed, egg-shaped orbits. If the initial energy exceeds the barrier height, the particle escapes to infinity, and its phase space trajectory veers off openly, never to return.