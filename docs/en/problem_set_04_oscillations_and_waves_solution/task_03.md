# Task 03 – Harmonic Wave

## Problem Statement

The wave equation is given:

$$
y(x,t) = A \sin(kx - \omega t)
$$

1. Determine the wavelength.
2. Determine the phase velocity.
3. Calculate $v$ for $k = 4\pi$, $\omega = 20\pi$.
4. Does the point $x = \lambda$ oscillate in phase with the point $x = 0$?

## Theory

A harmonic wave is a disturbance that travels through a medium, transferring energy without transferring matter. The mathematical description $y(x,t)$ represents the displacement of a point at position $x$ at time $t$.

The parameters of the wave are:
* **Wave number ($k$):** Related to the spatial periodicity (wavelength).
* **Angular frequency ($\omega$):** Related to the temporal periodicity (period).
* **Phase velocity ($v$):** The speed at which a specific phase of the wave (e.g., a crest) propagates through the medium.



## Step-by-Step Solution

### 1. Determining the Wavelength

The wavelength $\lambda$ is the distance over which the wave's shape repeats. In the sine function, the phase $kx$ must increase by $2\pi$ when $x$ increases by $\lambda$.

$$
k\lambda = 2\pi
$$

Solving for $\lambda$:

$$
\lambda = \frac{2\pi}{k}
$$

### 2. Determining the Phase Velocity

The phase velocity $v$ is the speed at which a point of constant phase moves. For a constant phase:

$$
kx - \omega t = \text{constant}
$$

Differentiating this expression with respect to time $t$:

$$
k \frac{dx}{dt} - \omega = 0
$$

Since $v = \frac{dx}{dt}$:

$$
kv - \omega = 0 \implies v = \frac{\omega}{k}
$$

### 3. Numerical Calculation

Given: $k = 4\pi$ and $\omega = 20\pi$.

Using the derived formula for phase velocity:

$$
v = \frac{20\pi}{4\pi} = 5\ \text{m/s}
$$

### 4. Phase Comparison

Two points oscillate in phase if the difference in their phases is an integer multiple of $2\pi$. We compare the phase at $x = \lambda$ and $x = 0$ at the same time $t$.

**Phase at $x = 0$:**
$\phi_0 = -\omega t$

**Phase at $x = \lambda$:**
$\phi_\lambda = k\lambda - \omega t$

The phase difference $\Delta\phi$ is:

$$
\Delta\phi = \phi_\lambda - \phi_0 = k\lambda
$$

Substituting $k = \frac{2\pi}{\lambda}$:

$$
\Delta\phi = \left( \frac{2\pi}{\lambda} \right) \lambda = 2\pi
$$

Since the phase difference is exactly $2\pi$, the oscillations are identical in state at any given moment.

## Final Result

* **Wavelength**: $\lambda = \frac{2\pi}{k}$
* **Phase Velocity**: $v = \frac{\omega}{k}$
* **Calculated Velocity**: $v = 5\ \text{m/s}$
* **Phase Relation**: Yes, the points oscillate in phase because the displacement is separated by exactly one wavelength.

## Interpretation

The wavelength represents the "spatial period" of the wave. The result in part 4 confirms the definition of wavelength: it is the smallest distance between two points that are in the same state of vibration. Any two points separated by an integer multiple of $\lambda$ will always oscillate in phase.