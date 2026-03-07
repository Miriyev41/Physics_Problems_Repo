# Task 10 – Double Pendulum and Deterministic Chaos

## Problem Statement

Consider a double pendulum consisting of two massive points $m_1, m_2$ on massless rods of lengths $l_1, l_2$ in a uniform gravitational field $g$.

1. Write the coordinates $(x_1, y_1)$ and $(x_2, y_2)$ as functions of the angles $(\theta_1, \theta_2)$.
2. Discuss the numerical integration (RK4) and the importance of numerical stability.
3. Investigate sensitivity to initial conditions (Chaos theory).
4. Describe the behavior of a 50-copy ensemble simulation with minimal perturbations.

## Theory

The double pendulum is a classic example of a simple physical system that exhibits **deterministic chaos**. While the equations of motion are fully deterministic (derived from the Lagrangian), the system is extremely sensitive to initial conditions. This sensitivity is often called the "Butterfly Effect."

The motion is non-linear and coupled. Unlike a single pendulum, which is integrable and predictable, the double pendulum's trajectory can become essentially unpredictable over long periods, even though it follows strict physical laws.



## Step-by-Step Solution

### 1. Cartesian Coordinates

The positions of the two masses in terms of the angles $\theta_1$ and $\theta_2$ (measured from the vertical) are:

**For the first mass ($m_1$):**
$$x_1 = l_1 \sin\theta_1$$
$$y_1 = -l_1 \cos\theta_1$$

**For the second mass ($m_2$):**
$$x_2 = x_1 + l_2 \sin\theta_2 = l_1 \sin\theta_1 + l_2 \sin\theta_2$$
$$y_2 = y_1 - l_2 \cos\theta_2 = -l_1 \cos\theta_1 - l_2 \cos\theta_2$$

### 2. Numerical Integration (RK4)

The equations of motion for $\ddot{\theta}_1$ and $\ddot{\theta}_2$ are highly complex. To solve them, we use the **Runge-Kutta 4th Order (RK4)** method.
* **Mechanism**: It approximates the state of the system at $t + \Delta t$ by taking a weighted average of four increments, effectively accounting for the curvature of the trajectory.
* **Stability**: In a chaotic system, energy drift is a major concern. If $\Delta t$ is too large, the system may gain or lose energy artificially, leading to unphysical behavior (e.g., the pendulum spontaneously spinning faster). A step of $\Delta t \le 0.01\ \text{s}$ is usually required.

### 3. Sensitivity to Initial Conditions

In a chaotic regime, two trajectories starting with a separation of $10^{-4}\ \text{rad}$ will initially stay close. However, because the system is chaotic, the distance between them grows **exponentially** over time.

$$
\Delta\theta(t) \approx \Delta\theta(0) e^{\lambda t}
$$

where $\lambda$ is the Lyapunov exponent. Once the divergence reaches the scale of the system itself, the two pendulums will appear to be moving completely independently.

### 4. Ensemble Simulation Analysis

When simulating 50 copies of the pendulum:
* **Initial Phase**: All 50 pendulums appear as a single line or a very thin "fan" of colors.
* **Transition Phase**: The "fan" begins to spread. You begin to see the individual colors as the small perturbations ($10^{-4}$ to $10^{-2}$ rad) are amplified.
* **Chaotic Phase**: The pendulums "smear" across the phase space. One might be looping over the top while another is swinging slowly at the bottom. The visual result is a colorful cloud of trajectories that no longer resemble the initial state.



## Final Result

* **Coordinates**: Derived from trigonometry relative to the pivot.
* **Dynamics**: Solved via RK4 to maintain energy conservation.
* **Chaos**: Demonstrated by the exponential divergence of the 50-pendulum ensemble.

## Interpretation

The double pendulum proves that "simple" does not mean "predictable." It serves as a laboratory for understanding complex systems like weather patterns or stock markets. Even with perfect knowledge of the laws of physics, the practical limit of our ability to measure initial conditions perfectly means we cannot predict the long-term state of the system—this is the heart of deterministic chaos.