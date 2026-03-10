# Task 07 – Forced oscillator and resonance

## Problem Statement

The equation for a forced harmonic oscillator is given by:

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = F_0 \cos(\Omega t)
$$

1. Solve the equation analytically, determining the amplitude of oscillations as a function of $\Omega$.
2. Solve the equation numerically.
3. Investigate the steady-state amplitude as a function of $\Omega$.
4. Generate the resonance curve.
5. Investigate the phase shift.
6. Interpret the phenomenon of resonance.

## Theory

[Image of resonance curve for a driven harmonic oscillator showing amplitude vs driving frequency]

A driven (or forced) harmonic oscillator is subjected to a periodic external force $F(t) = F_0 \cos(\Omega t)$ in addition to the restoring force and damping force. The general solution to this non-homogeneous differential equation is the sum of two parts:
1. **Transient solution ($x_h$):** The solution to the homogeneous equation (unforced damped oscillator), which decays to zero over time due to damping.
2. **Steady-state solution ($x_p$):** The particular solution that persists indefinitely, oscillating at exactly the driving frequency $\Omega$, but with a specific amplitude and phase shift relative to the driving force.

When the driving frequency $\Omega$ approaches the natural frequency of the system, the amplitude of the steady-state oscillations can become dramatically large. This phenomenon is known as **resonance**.

## Step-by-Step Solution

### 1. Solve the equation analytically

Divide the entire equation by the mass $m$:

$$
\frac{d^2 x}{dt^2} + \frac{b}{m} \frac{dx}{dt} + \frac{k}{m} x = \frac{F_0}{m} \cos(\Omega t)
$$

Define the standard parameters:
* $\omega_0 = \sqrt{\frac{k}{m}}$ (undamped natural frequency)
* $\gamma = \frac{b}{2m}$ (damping ratio)
* $f_0 = \frac{F_0}{m}$ (mass-normalized force amplitude)

The equation becomes:

$$
\ddot{x} + 2\gamma \dot{x} + \omega_0^2 x = f_0 \cos(\Omega t)
$$

To find the steady-state solution, we assume a solution of the form:

$$
x_p(t) = A \cos(\Omega t - \phi)
$$

where $A$ is the steady-state amplitude and $\phi$ is the phase shift. 

Substituting $x_p(t)$ and its derivatives into the differential equation and equating the sine and cosine coefficients yields the following expressions for $A$ and $\phi$:

**Amplitude:**
$$
A(\Omega) = \frac{f_0}{\sqrt{(\omega_0^2 - \Omega^2)^2 + (2\gamma\Omega)^2}} = \frac{F_0}{\sqrt{m^2(\omega_0^2 - \Omega^2)^2 + b^2\Omega^2}}
$$

**Phase Shift:**
$$
\tan \phi = \frac{2\gamma\Omega}{\omega_0^2 - \Omega^2} = \frac{b\Omega}{m(\omega_0^2 - \Omega^2)}
$$

### 2. Solve the equation numerically

To solve this numerically (e.g., using RK4), we convert the second-order ODE into a system of two first-order ODEs. Let $v = \dot{x}$:

$$
\begin{align}
\frac{dx}{dt} &= v \\
\frac{dv}{dt} &= \frac{F_0}{m}\cos(\Omega t) - \frac{b}{m}v - \frac{k}{m}x
\end{align}
$$

Starting from initial conditions $x(0)$ and $v(0)$, numerical integration will capture both the initial transient behavior (the "beat-like" interference between the natural frequency and driving frequency) and the eventual settling into the steady-state harmonic motion.

### 3 & 4. Steady-state amplitude and the resonance curve

The steady-state amplitude $A(\Omega)$ heavily depends on the driving frequency $\Omega$. 
* For $\Omega \to 0$ (very slow driving), $A \approx \frac{F_0}{m\omega_0^2} = \frac{F_0}{k}$. The system acts like a static spring.
* For $\Omega \to \infty$ (very fast driving), $A \to 0$. The mass's inertia prevents it from responding to rapid force fluctuations.
* **Resonance:** The amplitude reaches a maximum when the denominator is minimized. Setting the derivative of the term inside the square root to zero yields the amplitude resonance frequency:
  $$\Omega_{res} = \sqrt{\omega_0^2 - 2\gamma^2}$$
  For light damping ($\gamma \ll \omega_0$), $\Omega_{res} \approx \omega_0$, and the peak amplitude is very large, approximately $A_{max} \approx \frac{F_0}{b\omega_0}$.

The graph of $A$ vs $\Omega$ is called the **resonance curve**. It features a prominent peak near $\omega_0$, the sharpness of which is defined by the quality factor $Q = \frac{\omega_0}{2\gamma}$.

### 5. Investigate the phase shift $\phi$

The phase shift $\phi$ describes how much the displacement lags behind the driving force.
* When $\Omega \ll \omega_0$, $\tan \phi \to 0^+ \implies \phi \approx 0$. The displacement is perfectly in phase with the force.
* When $\Omega = \omega_0$, the denominator of $\tan \phi$ is zero, meaning $\phi = \frac{\pi}{2}$ (90 degrees). The force is exactly in phase with the *velocity*, meaning it constantly does positive work on the system, leading to resonance.
* When $\Omega \gg \omega_0$, $\tan \phi \to 0^- \implies \phi \approx \pi$ (180 degrees). The displacement is completely out of phase with the force; the mass moves opposite to the direction it is being pushed due to inertia.

### 6. Interpret the phenomenon of resonance

Resonance is the tendency of a system to absorb maximum energy from an oscillating driving force when the frequency of the force matches the system's natural frequency. At this specific frequency ($\Omega \approx \omega_0$), the external force pushes the mass precisely when it is already moving in the direction of the force, continuously adding energy to the system. Without damping ($b=0$), the amplitude would theoretically grow to infinity. With damping, the amplitude stabilizes when the energy added by the driving force per cycle exactly equals the energy dissipated by friction.