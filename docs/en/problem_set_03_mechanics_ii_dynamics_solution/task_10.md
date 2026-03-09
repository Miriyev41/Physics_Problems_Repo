# Task 10 – Numerical model of a dynamical system (Anharmonic Oscillator)

## Problem Statement

Consider motion in a one-dimensional potential given by:

$$
U(x) = \frac{k}{2}x^2 + \lambda x^4
$$

The required operations are:
1. Determine the force $F(x)$.
2. Write down the equation of motion.
3. Explain why the equation is non-linear and cannot be solved with basic trigonometric functions.
4. Implement a numerical solution using the Velocity Verlet algorithm.
5. Analyze the effect of the anharmonic term $\lambda$ on the period of oscillation.

## Theory

The potential $U(x) = \frac{k}{2}x^2 + \lambda x^4$ describes an **anharmonic oscillator**. The first term ($\frac{k}{2}x^2$) represents the standard harmonic potential (Hooke's Law), while the second term ($\lambda x^4$) introduces a non-linear correction. If $\lambda > 0$, the potential "wall" is steeper than a parabola, making the restoring force stronger at large displacements.

The force is derived from the potential:
$$
F(x) = -\frac{dU}{dx}
$$

The **Velocity Verlet algorithm** is a second-order numerical method used to integrate Newton's equations of motion. It is preferred over the simple Euler method because it is time-reversible and preserves the energy of the system much more accurately (it is a symplectic integrator).

The update steps for a time step $\Delta t$ are:
1. Calculate next position: $x(t+\Delta t) = x(t) + v(t)\Delta t + \frac{1}{2}a(t)\Delta t^2$
2. Calculate intermediate velocity: $v(t+\frac{\Delta t}{2}) = v(t) + \frac{1}{2}a(t)\Delta t$
3. Calculate new acceleration: $a(t+\Delta t) = F(x(t+\Delta t))/m$
4. Calculate final velocity: $v(t+\Delta t) = v(t+\frac{\Delta t}{2}) + \frac{1}{2}a(t+\Delta t)\Delta t$

## Step-by-Step Solution

### 1. Determine the force $F(x)$

Differentiate the potential with respect to $x$:

$$
\begin{align}
F(x) &= -\frac{d}{dx} \left( \frac{k}{2}x^2 + \lambda x^4 \right) \\
     &= -\left( \frac{k}{2} \cdot 2x + \lambda \cdot 4x^3 \right) \\
     &= -kx - 4\lambda x^3
\end{align}
$$

### 2. Write down the equation of motion

Using Newton's Second Law $m\ddot{x} = F$:

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

Standard form:
$$
\ddot{x} + \frac{k}{m}x + \frac{4\lambda}{m}x^3 = 0
$$

### 3. Non-linearity and Analytical Limitations

This equation is a **non-linear second-order differential equation** due to the $x^3$ term. 
- In a linear harmonic oscillator ($\lambda = 0$), the restoring force is proportional to displacement ($F \propto x$), leading to solutions like $\sin(\omega t)$ where the period is independent of amplitude.
- In the anharmonic case, the restoring force grows faster than displacement ($F \propto x^3$). This means the "stiffness" of the system effectively increases as the particle moves further from the origin. 
- Consequently, the period of oscillation $T$ becomes dependent on the amplitude $A$. Such equations generally require Jacobi elliptic functions for analytical solutions, which are significantly more complex than basic trigonometry.

### 4. Numerical Implementation (Velocity Verlet)

We solve the system by iterating the Velocity Verlet steps. For each step, we calculate the total energy $E = \frac{1}{2}mv^2 + U(x)$ to monitor numerical stability.

## Final Result

* Force: $F(x) = -kx - 4\lambda x^3$
* Equation of Motion: $m\ddot{x} + kx + 4\lambda x^3 = 0$
* If $\lambda > 0$, the oscillator is "stiffer," leading to a shorter period as amplitude increases.
* If $\lambda < 0$, the oscillator is "softer," leading to a longer period as amplitude increases.

## Interpretation



The anharmonic term $\lambda x^4$ fundamentally changes the dynamics of the system. While the motion remains periodic, the simple relationship between mass, spring constant, and frequency is broken. In a real physical system, such as a vibrating molecule, this anharmonicity is responsible for phenomena like thermal expansion—as the energy increases, the asymmetry or change in the potential shape causes the average position of the particles to shift.