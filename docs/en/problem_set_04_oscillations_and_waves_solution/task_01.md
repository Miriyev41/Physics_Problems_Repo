# Task 01 – Harmonic Motion: Motion Parameters

## Problem Statement

A function describing harmonic motion is given:

$$
x(t) = A \cos(\omega t + \varphi)
$$

1. Determine the period $T$ and the frequency $f$.
2. Determine the maximum velocity and the maximum acceleration.
3. For $A = 0.2\ \text{m}$, $f = 2\ \text{Hz}$:
   * calculate $\omega$,
   * calculate $v_{\max}$,
   * calculate $a_{\max}$.

## Theory

Harmonic motion is a periodic motion where the position $x(t)$ varies sinusoidally with time. The parameters of this motion are defined as:
* **Amplitude ($A$):** The maximum displacement from the equilibrium position.
* **Angular Frequency ($\omega$):** The rate of change of the phase of the sinusoidal waveform.
* **Phase Constant ($\varphi$):** The initial state of the oscillation at $t=0$.

The velocity $v(t)$ and acceleration $a(t)$ are the first and second derivatives of the position with respect to time, respectively.

## Step-by-Step Solution

### 1. Determining Period and Frequency

The argument of the cosine function, $(\omega t + \varphi)$, completes one full cycle of $2\pi$ radians in one period $T$.

$$
\omega T = 2\pi \implies T = \frac{2\pi}{\omega}
$$

The frequency $f$ is the reciprocal of the period, representing the number of oscillations per unit time:

$$
f = \frac{1}{T} = \frac{\omega}{2\pi}
$$

### 2. Maximum Velocity and Acceleration

To find velocity, we differentiate the position function:

$$
v(t) = \frac{dx}{dt} = \frac{d}{dt} [A \cos(\omega t + \varphi)] = -A\omega \sin(\omega t + \varphi)
$$

The maximum velocity $v_{\max}$ occurs when the sine term is $\pm 1$:

$$
v_{\max} = A\omega
$$

To find acceleration, we differentiate the velocity function:

$$
a(t) = \frac{dv}{dt} = \frac{d}{dt} [-A\omega \sin(\omega t + \varphi)] = -A\omega^2 \cos(\omega t + \varphi)
$$

The maximum acceleration $a_{\max}$ occurs when the cosine term is $\pm 1$:

$$
a_{\max} = A\omega^2
$$

### 3. Numerical Calculations

Given: $A = 0.2\ \text{m}$, $f = 2\ \text{Hz}$.

**Calculating $\omega$:**

$$
\omega = 2\pi f = 2\pi (2) = 4\pi\ \text{rad/s} \approx 12.57\ \text{rad/s}
$$

**Calculating $v_{\max}$:**

$$
v_{\max} = A\omega = 0.2 \times 4\pi = 0.8\pi\ \text{m/s} \approx 2.51\ \text{m/s}
$$

**Calculating $a_{\max}$:**

$$
a_{\max} = A\omega^2 = 0.2 \times (4\pi)^2 = 0.2 \times 16\pi^2 = 3.2\pi^2\ \text{m/s}^2 \approx 31.58\ \text{m/s}^2
$$

## Final Result

* **Period and Frequency**: $T = \frac{2\pi}{\omega}$, $f = \frac{\omega}{2\pi}$.
* **Kinematic Limits**: $v_{\max} = A\omega$, $a_{\max} = A\omega^2$.
* **Numerical Values**: $\omega = 4\pi\ \text{rad/s}$, $v_{\max} = 0.8\pi\ \text{m/s}$, $a_{\max} = 3.2\pi^2\ \text{m/s}^2$.

## Interpretation

The maximum velocity occurs as the object passes through the equilibrium position ($x=0$), where all energy is kinetic. Conversely, maximum acceleration occurs at the points of maximum displacement ($x = \pm A$), where the restoring force is strongest. Note that as the frequency of oscillation increases, the maximum acceleration grows quadratically ($\omega^2$), placing significantly higher mechanical stress on the system than a simple increase in amplitude would.