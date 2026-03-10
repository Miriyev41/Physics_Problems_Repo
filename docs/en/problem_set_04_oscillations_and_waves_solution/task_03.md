# Task 03 – Harmonic wave

## Problem Statement

The wave equation is given by:

$$
y(x,t) = A \sin(kx - \omega t)
$$

1. Determine the wavelength.
2. Determine the phase velocity.
3. Calculate $v$ for $k = 4\pi$, $\omega = 20\pi$.
4. Does the point $x = \lambda$ oscillate in phase with the point $x = 0$?

## Theory

[Image of a harmonic wave indicating wavelength, amplitude, and propagation direction]

A harmonic wave represents a disturbance propagating through space and time, where the displacement of any point in the medium undergoes simple harmonic motion. The general equation $y(x,t) = A \sin(kx - \omega t)$ describes a wave traveling in the positive $x$-direction.

- **Wave number ($k$)**: Represents the spatial frequency of the wave, measured in radians per unit length.
- **Angular frequency ($\omega$)**: Represents the temporal frequency, measured in radians per unit time.
- **Wavelength ($\lambda$)**: The spatial period of the wave—the distance over which the wave's shape repeats.
- **Phase velocity ($v$)**: The speed at which the phase of the wave (e.g., a specific crest or trough) propagates through space.

Two points are said to oscillate "in phase" if their phase difference is an integer multiple of $2\pi$.

## Step-by-Step Solution

### 1. Determine the wavelength $\lambda$

The spatial dependence of the wave is governed by the term $kx$. A full cycle of the sine function corresponds to a change in the argument by $2\pi$. The distance over which this full cycle occurs is, by definition, the wavelength $\lambda$.

Therefore, increasing the coordinate $x$ by $\lambda$ must increase the phase by exactly $2\pi$:

$$
k(x + \lambda) - kx = 2\pi
$$

$$
k\lambda = 2\pi
$$

Solving for $\lambda$ yields:

$$
\lambda = \frac{2\pi}{k}
$$

### 2. Determine the phase velocity $v$

The phase velocity is the speed at which a point of constant phase travels. Let us set the entire phase argument to a constant value $C$:

$$
kx - \omega t = C
$$

To find the velocity $v = \frac{dx}{dt}$, we differentiate both sides with respect to time $t$:

$$
\begin{align}
\frac{d}{dt} (kx - \omega t) &= \frac{d}{dt} (C) \\
k \frac{dx}{dt} - \omega &= 0 \\
k v - \omega &= 0
\end{align}
$$

Solving for $v$:

$$
v = \frac{\omega}{k}
$$

### 3. Calculate $v$ for $k = 4\pi$ and $\omega = 20\pi$

Substitute the given values into the phase velocity formula:

$$
\begin{align}
v &= \frac{\omega}{k} \\
  &= \frac{20\pi}{4\pi} \\
  &= 5\ \mathrm{m/s}
\end{align}
$$
*(Assuming standard SI units of $\mathrm{rad/m}$ for $k$ and $\mathrm{rad/s}$ for $\omega$.)*

### 4. Phase comparison for $x = 0$ and $x = \lambda$

Let us evaluate the phase angle of the wave at the two specific points at an arbitrary time $t$. 

For $x = 0$, the phase is:

$$
\phi_1(t) = k(0) - \omega t = -\omega t
$$

For $x = \lambda$, we first substitute $\lambda = \frac{2\pi}{k}$:

$$
\begin{align}
\phi_2(t) &= k\lambda - \omega t \\
          &= k\left(\frac{2\pi}{k}\right) - \omega t \\
          &= 2\pi - \omega t
\end{align}
$$

Now, we calculate the phase difference between the two points:

$$
\begin{align}
\Delta \phi &= \phi_2(t) - \phi_1(t) \\
            &= (2\pi - \omega t) - (-\omega t) \\
            &= 2\pi
\end{align}
$$

Because the phase difference is exactly $2\pi$, the sine function yields the exact same value and derivative at both points. Therefore, **yes**, the point $x = \lambda$ oscillates perfectly in phase with the point $x = 0$.

## Final Result

- **Wavelength:** $\lambda = \frac{2\pi}{k}$
- **Phase velocity:** $v = \frac{\omega}{k}$
- **Calculated velocity:** $v = 5$ (for $k=4\pi$, $\omega=20\pi$)
- **Phase comparison:** Yes, the points at $x = 0$ and $x = \lambda$ oscillate exactly in phase.

## Interpretation

The wave number $k$ and angular frequency $\omega$ are the spatial and temporal analogs of each other. While $\omega$ tells us how many radians of phase pass per second, $k$ tells us how many radians of phase exist per meter. The ratio $\omega/k$ cleanly extracts the speed at which the wave pattern translates. The fact that points separated by exactly one wavelength ($\lambda$) oscillate in phase is a fundamental property of wave periodicity—the spatial landscape of the wave essentially "resets" every $\lambda$ distance.