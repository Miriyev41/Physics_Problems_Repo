# Task 10 – Numerical Model of a Dynamical System

## Problem Statement

Consider motion in a one-dimensional potential:

$$
U(x) = \frac{k}{2}x^2 + \lambda x^4
$$

* Determine the force $F(x)$.
* Write down the equation of motion.
* Describe the motion for small and large amplitudes.
* Discuss the numerical approach (Euler method) to solve such an equation.
* Perform a numerical simulation for chosen parameters $k, \lambda$.

## Theory

This potential represents an **anharmonic oscillator**. The first term corresponds to a linear restoring force (Hooke's Law), while the second term ($\lambda x^4$) introduces a non-linearity. 

In dynamics, the force is the negative derivative of the potential energy:

$$
F(x) = -\frac{dU}{dx}
$$

Since the force is non-linear, the equation of motion does not have a simple analytical solution in terms of basic trigonometric functions. Therefore, numerical methods like the **Euler method** or **Runge-Kutta** are used to approximate the trajectory by discretizing time into small steps $\Delta t$.



## Step-by-Step Solution

### 1. Determining the Force

Differentiating the potential $U(x)$:

$$
F(x) = -\frac{d}{dx} \left( \frac{k}{2}x^2 + \lambda x^4 \right)
$$

$$
F(x) = -(kx + 4\lambda x^3)
$$

### 2. Equation of Motion

Using Newton's Second Law ($m\ddot{x} = F$):

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

$$
\ddot{x} + \frac{k}{m}x + \frac{4\lambda}{m}x^3 = 0
$$

This is known as the **Duffing equation** (without damping or driving force).

### 3. Motion Analysis

* **Small Amplitudes ($x \ll 1$):** The $x^3$ term becomes negligible compared to the $x$ term. The system behaves like a simple harmonic oscillator with frequency $\omega_0 = \sqrt{k/m}$.
* **Large Amplitudes:** The $4\lambda x^3$ term dominates. If $\lambda > 0$ (hard spring), the restoring force increases faster than linearly, leading to a higher frequency of oscillation as amplitude increases.

### 4. Numerical Approach (Euler Method)

To solve $\ddot{x} = f(x, v)$, we break it into two first-order equations:
1. $\frac{dv}{dt} = -\frac{k}{m}x - \frac{4\lambda}{m}x^3$
2. $\frac{dx}{dt} = v$

For each time step $n$:

$$
v_{n+1} = v_n + a_n \Delta t
$$

$$
x_{n+1} = x_n + v_n \Delta t
$$

### 5. Numerical Simulation (Conceptual)

For parameters $m=1, k=1, \lambda=0.5$ and initial conditions $x(0)=1, v(0)=0$:
* At $t=0$: $a = -(1(1) + 4(0.5)(1^3)) = -3$.
* After $\Delta t = 0.01$:
    * $v(0.01) = 0 + (-3)(0.01) = -0.03$
    * $x(0.01) = 1 + (0)(0.01) = 1.00$
* The simulation repeats these steps to trace the non-sinusoidal periodic path.

## Final Result

* **Force**: $F(x) = -kx - 4\lambda x^3$
* **Equation of Motion**: $\ddot{x} + \frac{k}{m}x + \frac{4\lambda}{m}x^3 = 0$
* **Method**: Euler integration $x(t+\Delta t) \approx x(t) + v(t)\Delta t$.

## Interpretation

The $x^4$ term in the potential breaks the simple harmony of the system. In a physical sense, $\lambda$ represents the "stiffness" adjustment of a spring. Numerical models allow us to explore these complex systems where pen-and-paper math becomes insufficient, revealing how period depends on amplitude—a phenomenon not seen in simple linear oscillators.