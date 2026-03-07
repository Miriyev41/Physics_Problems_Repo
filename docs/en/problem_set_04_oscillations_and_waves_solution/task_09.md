# Task 09 – Chain of N Springs (Discrete Wave Model)

## Problem Statement

System: $N$ masses connected by springs in a linear chain.

1. Write down the equations of motion.
2. Discuss the numerical solution for large $N$ ($N = 20, 50, 100$).
3. Analyze the propagation of a local initial disturbance.
4. Investigate the effect of $k$ and $m$ on the propagation speed.

## Theory

A chain of $N$ coupled oscillators serves as a discrete model for a continuous medium, such as a string or a solid lattice. When the number of masses $N$ becomes very large and the spacing between them becomes very small, the discrete equations of motion transition into the continuous wave equation.

In this model, each mass $i$ is connected to its neighbors $i-1$ and $i+1$. The restoring force on mass $i$ depends on its relative displacement compared to its neighbors.



## Step-by-Step Solution

### 1. Equations of Motion

Consider $N$ identical masses $m$ connected by identical springs with constant $k$. Let $x_i$ be the displacement of the $i$-th mass from its equilibrium position.

For an interior mass $i$ (where $1 < i < N$), the net force is:
$F_i = -k(x_i - x_{i-1}) + k(x_{i+1} - x_i)$.

Applying Newton's Second Law:

$$m \ddot{x}_i = k(x_{i+1} - 2x_i + x_{i-1})$$.

For boundary masses (1 and $N$), the equations depend on the boundary conditions (e.g., fixed ends where $x_0 = 0$ and $x_{N+1} = 0$).

### 2. Numerical Solution for Large N

As $N$ increases ($20 \to 50 \to 100$), the system becomes a large set of coupled second-order ODEs. Solving this analytically (finding $N$ normal modes) becomes computationally expensive. Numerical integration (like RK4) is used to track the displacement of every mass simultaneously.
* **Stability**: A smaller time step $\Delta t$ is required as $N$ increases to maintain numerical precision.
* **Visualization**: With high $N$, the discrete masses appear to form a continuous string.

### 3. Propagation of a Pulse

If we introduce a local disturbance (e.g., displacing only mass $i=1$ and then releasing it), the energy is transferred to mass $i=2$, then $i=3$, and so on.
* The disturbance travels through the chain as a **wave pulse**.
* When the pulse reaches a fixed boundary, it reflects (often with a phase inversion).

### 4. Effect of Parameters on Speed

The speed $v$ at which the disturbance propagates through the discrete chain is determined by the "stiffness" and "inertia" of the components:
* **Spring Constant ($k$):** Increasing $k$ increases the restoring force, causing the signal to transfer faster between masses ($v \propto \sqrt{k}$).
* **Mass ($m$):** Increasing $m$ increases the inertia of each link, slowing down the response to the neighboring mass ($v \propto 1/\sqrt{m}$).

In the continuous limit, the speed is $v = a\sqrt{k/m}$, where $a$ is the equilibrium spacing.

## Final Result

* **Dynamical Equation**: $\ddot{x}_i = \frac{k}{m}(x_{i+1} - 2x_i + x_{i-1})$.
* **Propagation**: A local pulse travels at a speed determined by $\sqrt{k/m}$.
* **Model**: This discrete system effectively approximates the wave equation $\frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2}$.

## Interpretation

The $N$-spring chain provides a bridge between particle mechanics and continuum mechanics. It illustrates that "waves" are not a separate entity but a collective phenomenon emerging from the local interactions of many individual particles. This model is fundamental in solid-state physics for describing phonons (lattice vibrations).