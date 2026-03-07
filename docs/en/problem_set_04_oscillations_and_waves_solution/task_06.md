# Task 06 – Damped Oscillator

## Problem Statement

The equation of motion for a damped harmonic oscillator is:

$$
m\ddot{x} + b\dot{x} + kx = 0
$$

1. Solve the equation for the underdamped case ($b^2 < 4mk$).
2. Determine the damping constant $\gamma$ and the frequency of damped oscillations $\omega$.
3. Draw the graph of $x(t)$ (qualitative description).
4. Discuss the physical meaning of the relaxation time $\tau = 1/\gamma$.

## Theory

A damped oscillator is a system where a resistive force (damping), proportional to velocity, opposes the motion. This leads to a gradual loss of mechanical energy.

The dynamics are governed by a second-order linear homogeneous differential equation. The behavior of the system depends on the relationship between the damping force and the restoring force, leading to three regimes:
* **Underdamped:** The system oscillates with decreasing amplitude.
* **Critically Damped:** The system returns to equilibrium as quickly as possible without oscillating.
* **Overdamped:** The system returns slowly to equilibrium without oscillating.



## Step-by-Step Solution

### 1. Solving the Equation

We rewrite the equation in standard form by dividing by $m$:

$$
\ddot{x} + \frac{b}{m}\dot{x} + \frac{k}{m}x = 0
$$

We introduce the damping constant $\gamma$ and the undamped natural frequency $\omega_0$:

$$
2\gamma = \frac{b}{m}, \qquad \omega_0^2 = \frac{k}{m}
$$

The equation becomes:

$$
\ddot{x} + 2\gamma\dot{x} + \omega_0^2 x = 0
$$

For the underdamped case ($\gamma < \omega_0$), the general solution is:

$$
x(t) = A e^{-\gamma t} \cos(\omega t + \phi)
$$

### 2. Damping Constant and Damped Frequency

The damping constant (attenuation coefficient) is:

$$
\gamma = \frac{b}{2m}
$$

The frequency of the damped oscillations $\omega$ is lower than the natural frequency $\omega_0$ due to the resistance:

$$
\omega = \sqrt{\omega_0^2 - \gamma^2} = \sqrt{\frac{k}{m} - \left(\frac{b}{2m}\right)^2}
$$

### 3. Trajectory Description

The graph of $x(t)$ consists of a sinusoidal wave whose peaks are bounded by an exponential "envelope" $A e^{-\gamma t}$.
* The motion is periodic but the amplitude decays over time.
* The crossing points with the $t$-axis are spaced at intervals of $T/2 = \pi/\omega$.
* As $t \to \infty$, the displacement $x(t) \to 0$.

### 4. Relaxation Time

The relaxation time $\tau$ is defined as the reciprocal of the damping constant:

$$
\tau = \frac{1}{\gamma} = \frac{2m}{b}
$$

**Physical Meaning:** $\tau$ is the time required for the amplitude of the oscillations to drop to $1/e$ (approximately $36.8\%$) of its initial value. It characterizes how quickly the system dissipates energy. A high $\tau$ implies low damping (the system oscillates for a long time), while a low $\tau$ implies high damping (energy is lost quickly).

## Final Result

* **Solution**: $x(t) = A e^{-\gamma t} \cos(\omega t + \phi)$
* **Damped Frequency**: $\omega = \sqrt{\omega_0^2 - \gamma^2}$
* **Relaxation Time**: $\tau = \frac{2m}{b}$

## Interpretation

In a damped oscillator, energy is no longer conserved; it is transformed into heat in the surroundings (due to friction or viscosity). The underdamped case is the most common in engineering and music, where the system still "rings" or oscillates, but eventually settles to its equilibrium position.