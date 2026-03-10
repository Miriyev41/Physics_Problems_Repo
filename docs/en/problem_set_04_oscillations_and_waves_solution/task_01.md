# Task 01 – Harmonic motion: motion parameters

## Problem Statement

A function describing harmonic motion is given:

$$
x(t) = A \cos(\omega t + \varphi)
$$

1. Determine the period $T$ and the frequency $f$.
2. Determine the maximum velocity and the maximum acceleration.
3. For $A = 0.2\ \mathrm{m}$, $f = 2\ \mathrm{Hz}$:
   * calculate $\omega$,
   * calculate $v_{\max}$,
   * calculate $a_{\max}$.

## Theory


Simple Harmonic Motion (SHM) is a periodic motion where the restoring force is directly proportional to the displacement and acts in the direction opposite to that of displacement. The motion is described by sinusoidal functions of time.

- **Amplitude ($A$)**: The maximum displacement from the equilibrium position.
- **Angular frequency ($\omega$)**: The rate of change of the phase of the oscillation, measured in radians per second.
- **Phase constant ($\varphi$)**: Determines the initial state of the system at $t=0$.
- **Period ($T$)**: The time required to complete one full cycle of oscillation.
- **Frequency ($f$)**: The number of cycles completed per unit of time (usually seconds, giving Hertz).

Velocity and acceleration are found by taking the first and second time derivatives of the position function, respectively.

## Step-by-Step Solution

### 1. Determine the period $T$ and the frequency $f$

The argument of the cosine function is the phase $\theta(t) = \omega t + \varphi$. The cosine function repeats every $2\pi$ radians. Therefore, the time it takes for one full cycle (the period $T$) corresponds to a phase change of $2\pi$:

$$
\omega (t + T) + \varphi = (\omega t + \varphi) + 2\pi
$$

$$
\omega T = 2\pi
$$

Solving for the period $T$:

$$
T = \frac{2\pi}{\omega}
$$

The frequency $f$ is the reciprocal of the period:

$$
f = \frac{1}{T} = \frac{\omega}{2\pi}
$$

### 2. Determine the maximum velocity and maximum acceleration

The velocity $v(t)$ is the first derivative of position with respect to time:

$$
\begin{align}
v(t) &= \frac{dx}{dt} \\
     &= \frac{d}{dt} [A \cos(\omega t + \varphi)] \\
     &= -A\omega \sin(\omega t + \varphi)
\end{align}
$$

The sine function oscillates between $-1$ and $1$. Therefore, the maximum magnitude of the velocity is the amplitude of this function:

$$
v_{\max} = A\omega
$$

The acceleration $a(t)$ is the derivative of velocity with respect to time (or the second derivative of position):

$$
\begin{align}
a(t) &= \frac{dv}{dt} \\
     &= \frac{d}{dt} [-A\omega \sin(\omega t + \varphi)] \\
     &= -A\omega^2 \cos(\omega t + \varphi)
\end{align}
$$

The cosine function also oscillates between $-1$ and $1$. Thus, the maximum magnitude of the acceleration is:

$$
a_{\max} = A\omega^2
$$

### 3. Calculations for $A = 0.2\ \mathrm{m}$ and $f = 2\ \mathrm{Hz}$

First, calculate the angular frequency $\omega$ using the relation $f = \frac{\omega}{2\pi}$:

$$
\begin{align}
\omega &= 2\pi f \\
       &= 2\pi (2) \\
       &= 4\pi\ \mathrm{rad/s} \approx 12.57\ \mathrm{rad/s}
\end{align}
$$

Next, calculate the maximum velocity $v_{\max}$:

$$
\begin{align}
v_{\max} &= A\omega \\
         &= (0.2)(4\pi) \\
         &= 0.8\pi\ \mathrm{m/s} \approx 2.51\ \mathrm{m/s}
\end{align}
$$

Finally, calculate the maximum acceleration $a_{\max}$:

$$
\begin{align}
a_{\max} &= A\omega^2 \\
         &= (0.2)(4\pi)^2 \\
         &= (0.2)(16\pi^2) \\
         &= 3.2\pi^2\ \mathrm{m/s^2} \approx 31.58\ \mathrm{m/s^2}
\end{align}
$$

## Final Result

- **Period:** $T = \frac{2\pi}{\omega}$
- **Frequency:** $f = \frac{\omega}{2\pi}$
- **Maximum velocity:** $v_{\max} = A\omega$
- **Maximum acceleration:** $a_{\max} = A\omega^2$
- **For $A = 0.2\ \mathrm{m}, f = 2\ \mathrm{Hz}$:**
  - $\omega = 4\pi \approx 12.57\ \mathrm{rad/s}$
  - $v_{\max} = 0.8\pi \approx 2.51\ \mathrm{m/s}$
  - $a_{\max} = 3.2\pi^2 \approx 31.58\ \mathrm{m/s^2}$

## Interpretation

The derivations show that in harmonic motion, the limits of speed and acceleration depend strictly on the amplitude and the angular frequency. Higher frequencies lead to proportionally higher maximum speeds but result in a quadratic increase in maximum acceleration. This means that oscillating an object back and forth very rapidly (high $f$) requires dramatically stronger restoring forces (which provide the acceleration) than oscillating it slowly.