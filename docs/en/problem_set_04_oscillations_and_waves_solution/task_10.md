# Task 10 – Double pendulum and deterministic chaos

## Problem Statement

Consider a double pendulum (two massive points $m_1, m_2$ on massless rods $l_1, l_2$) in a uniform gravitational field $g$. Assume the equations of motion from the standard form for a double pendulum.

1. Write the coordinates $(x_1,y_1)$ and $(x_2,y_2)$ as functions of the angles $(\theta_1,\theta_2)$.
2. Implement a numerical integration of the equations (e.g., RK4) and check numerical stability.
3. Investigate the sensitivity to initial conditions: simulate simultaneously 50 copies of the system with minimally different initial conditions (e.g., a perturbation only in $\theta_2(0)$ on the order of $10^{-4}$–$10^{-2}$ rad).
4. Experiment with different scales of perturbation and observe the divergence of the trajectories.

Starting parameters: $m_1=m_2=1$, $l_1=l_2=1$, $g=9.81$, integration step $\Delta t \le 0.01\ \mathrm{s}$.

## Theory

[Image of a double pendulum schematic with angles theta_1 and theta_2]

The double pendulum is a classic example of a simple physical system that exhibits **deterministic chaos**. While the equations governing its motion are strictly deterministic (meaning future states are perfectly defined by initial states without any randomness), the system is extremely sensitive to initial conditions. 

This sensitivity, often popularly called the "butterfly effect," means that two starting states differing by an infinitesimally small amount will quickly diverge into completely different trajectories. The rate of this exponential divergence is quantified by the Lyapunov exponent.

Because the equations of motion for a double pendulum are highly nonlinear and cannot be solved analytically for arbitrary amplitudes, we must rely on numerical integration methods, such as the 4th-order Runge-Kutta (RK4) method, to simulate its behavior.

## Step-by-Step Solution

### 1. Coordinates as functions of angles

Let the origin $(0,0)$ be the pivot point of the first pendulum. Let the $y$-axis point downwards. 
The angle $\theta_1$ is the angle the first rod makes with the vertical, and $\theta_2$ is the angle the second rod makes with the vertical.

The coordinates of the first mass $m_1$ are:
$$
x_1 = l_1 \sin\theta_1 \\
y_1 = l_1 \cos\theta_1
$$

The coordinates of the second mass $m_2$ are located at the end of the second rod, which is attached to the first mass:
$$
x_2 = x_1 + l_2 \sin\theta_2 = l_1 \sin\theta_1 + l_2 \sin\theta_2 \\
y_2 = y_1 + l_2 \cos\theta_2 = l_1 \cos\theta_1 + l_2 \cos\theta_2
$$

### 2. Equations of Motion and Numerical Integration

Using Lagrangian mechanics, the standard equations of motion for the angular accelerations $\ddot{\theta}_1$ and $\ddot{\theta}_2$ are:

$$
\ddot{\theta}_1 = \frac{-g(2m_1+m_2)\sin\theta_1 - m_2 g \sin(\theta_1-2\theta_2) - 2\sin(\theta_1-\theta_2)m_2(\dot{\theta}_2^2 l_2 + \dot{\theta}_1^2 l_1 \cos(\theta_1-\theta_2))}{l_1 (2m_1 + m_2 - m_2\cos(2\theta_1 - 2\theta_2))}
$$

$$
\ddot{\theta}_2 = \frac{2\sin(\theta_1-\theta_2)(\dot{\theta}_1^2 l_1(m_1+m_2) + g(m_1+m_2)\cos\theta_1 + \dot{\theta}_2^2 l_2 m_2 \cos(\theta_1-\theta_2))}{l_2 (2m_1 + m_2 - m_2\cos(2\theta_1 - 2\theta_2))}
$$

To integrate this numerically, we convert this into a system of four first-order differential equations:
$$\dot{\theta}_1 = \omega_1$$
$$\dot{\omega}_1 = f_1(\theta_1, \theta_2, \omega_1, \omega_2)$$
$$\dot{\theta}_2 = \omega_2$$
$$\dot{\omega}_2 = f_2(\theta_1, \theta_2, \omega_1, \omega_2)$$

Where $f_1$ and $f_2$ are the right-hand sides of the equations above. The RK4 method uses these derivatives to update the state $(\theta_1, \omega_1, \theta_2, \omega_2)$ by calculating four intermediate slopes and taking a weighted average for the final step. 

[Image of deterministic chaos in double pendulum phase space]

**Numerical Stability (Energy Drift):**
Since the system is conservative (no friction), the total energy $E = T + V$ must remain strictly constant:
$$V = -m_1 g l_1 \cos\theta_1 - m_2 g (l_1 \cos\theta_1 + l_2 \cos\theta_2)$$
$$T = \frac{1}{2}m_1(l_1\dot{\theta}_1)^2 + \frac{1}{2}m_2[l_1^2\dot{\theta}_1^2 + l_2^2\dot{\theta}_2^2 + 2l_1l_2\dot{\theta}_1\dot{\theta}_2\cos(\theta_1-\theta_2)]$$
Numerical integration methods inevitably introduce small rounding and truncation errors at each step. By keeping $\Delta t$ sufficiently small ($\le 0.01\ \mathrm{s}$ with RK4), the energy drift remains negligible for long periods, validating the simulation.

### 3 & 4. Sensitivity to initial conditions (Ensemble Simulation)

We initialize $N=50$ copies of the double pendulum. They all share the same $\theta_1$, but their $\theta_2$ values are distributed uniformly across a tiny range $\Delta \theta$ (e.g., $10^{-3}$ radians). 

Initially, the 50 pendulums swing as a single coherent block. Their trajectories appear identical. However, because the system is chaotic, the microscopic differences in their initial states grow exponentially. After a few swings, the "block" begins to fray. Shortly after, the pendulums scatter entirely, exhibiting completely independent and chaotic motions, visualizing the stark reality of the butterfly effect.

## Final Result

- **Coordinates:** $x_1 = l_1\sin\theta_1$, $y_1 = l_1\cos\theta_1$; $x_2 = l_1\sin\theta_1 + l_2\sin\theta_2$, $y_2 = l_1\cos\theta_1 + l_2\cos\theta_2$.
- **Simulation setup:** Implemented using 4th-order Runge Kutta (RK4) with $dt = 0.01\ \mathrm{s}$.
- **Observations:** An ensemble of 50 pendulums differing by $10^{-4}$ rad will stay bound together for a few periods before diverging exponentially into entirely uncorrelated chaotic orbits.

## Interpretation

The double pendulum simulation beautifully destroys the classical intuition that "similar causes produce similar effects." While true for a simple harmonic oscillator, in nonlinear chaotic systems, "almost the same" initial state does not result in "almost the same" final state. This fundamentally limits our ability to predict the long-term future of chaotic systems (like weather patterns) because it is physically impossible to measure the initial conditions with infinite precision.