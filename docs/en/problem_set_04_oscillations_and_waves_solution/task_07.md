# Task 07 – Forced Oscillations and Resonance

## Problem Statement

The equation of motion for a forced oscillator is:

$$
m\ddot{x} + b\dot{x} + kx = F_0 \cos(\Omega t)
$$

1. Determine the steady-state solution $x(t) = A(\Omega) \cos(\Omega t + \delta)$.
2. Determine the amplitude $A(\Omega)$ as a function of the driving frequency.
3. Determine the resonance frequency $\Omega_r$.
4. Draw the resonance curve for different values of the damping coefficient $b$ (qualitative description).

## Theory

Forced oscillation occurs when an external periodic force is applied to a damped harmonic oscillator. While the initial motion (transient solution) depends on the initial conditions and damping, it eventually dies out, leaving the **steady-state solution**. In this state, the system oscillates at the frequency of the driving force $\Omega$, not its own natural frequency $\omega_0$.

Resonance is the phenomenon where the amplitude of oscillation reaches a maximum when the driving frequency $\Omega$ is close to the natural frequency of the system.



## Step-by-Step Solution

### 1. Steady-State Amplitude and Phase

We rewrite the equation using $\gamma = b/2m$ and $\omega_0^2 = k/m$:

$$
\ddot{x} + 2\gamma\dot{x} + \omega_0^2 x = f_0 \cos(\Omega t)
$$

where $f_0 = F_0/m$. We assume a solution of the form $x(t) = A \cos(\Omega t + \delta)$. Substituting this into the differential equation and using trigonometric identities (or complex exponentials), we solve for $A$:

$$
A(\Omega) = \frac{f_0}{\sqrt{(\omega_0^2 - \Omega^2)^2 + (2\gamma\Omega)^2}}
$$

The phase angle $\delta$ is given by:

$$
\tan \delta = \frac{-2\gamma\Omega}{\omega_0^2 - \Omega^2}
$$

### 2. Amplitude Analysis

The amplitude $A(\Omega)$ depends heavily on the denominator. 
* If $\Omega \to 0$ (static limit), $A \to f_0/\omega_0^2 = F_0/k$.
* If $\Omega \to \infty$, $A \to 0$.
* If $\Omega \approx \omega_0$, the first term in the square root vanishes, and the amplitude is limited only by the damping term $2\gamma\Omega$.

### 3. Resonance Frequency

To find the frequency $\Omega_r$ that maximizes $A(\Omega)$, we minimize the expression inside the square root:
$g(\Omega) = (\omega_0^2 - \Omega^2)^2 + 4\gamma^2\Omega^2$.

Taking the derivative with respect to $\Omega$ and setting it to zero:

$$
\frac{dg}{d\Omega} = 2(\omega_0^2 - \Omega^2)(-2\Omega) + 8\gamma^2\Omega = 0
$$

Dividing by $-4\Omega$:

$$
\omega_0^2 - \Omega^2 - 2\gamma^2 = 0
$$

$$
\Omega_r = \sqrt{\omega_0^2 - 2\gamma^2}
$$

### 4. Resonance Curves

The resonance curve (Amplitude vs. $\Omega$) exhibits the following features:
* **Low Damping**: A very sharp, high peak located very close to $\omega_0$.
* **High Damping**: A broader, lower peak shifted further to the left (lower frequencies).
* **Critical Case**: If $2\gamma^2 \ge \omega_0^2$, the peak disappears entirely, and the maximum amplitude occurs at $\Omega = 0$.

## Final Result

* **Amplitude Function**: $A(\Omega) = \frac{F_0/m}{\sqrt{(\omega_0^2 - \Omega^2)^2 + (2\gamma\Omega)^2}}$
* **Resonance Frequency**: $\Omega_r = \sqrt{\omega_0^2 - 2\gamma^2}$
* **Phase**: $\delta$ shifts from $0$ to $-\pi$ as $\Omega$ passes through resonance.

## Interpretation

Resonance demonstrates the efficient transfer of energy from an external source to an oscillator. At $\Omega_r$, the driving force is timed perfectly with the velocity of the system, maximizing the work done on the oscillator. In engineering, resonance must often be avoided (e.g., in bridges or buildings) to prevent structural failure due to excessive amplitudes.