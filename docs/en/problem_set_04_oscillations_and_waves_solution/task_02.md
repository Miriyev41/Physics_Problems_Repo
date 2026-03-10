# Task 02 – Energy of a harmonic oscillator

## Problem Statement

A system with the following initial parameters is given:

* $m = 1\ \mathrm{kg}$
* $k = 100\ \mathrm{N/m}$
* $x(0) = 2\ \mathrm{m}$
* $v(0) = 1\ \mathrm{m/s}$

1. Determine the natural frequency.
2. Calculate the total energy of the system.
3. For what displacement does the kinetic energy account for 50% of the total energy?

## Theory


In a simple harmonic oscillator, such as a mass on an ideal spring, the total mechanical energy $E$ is conserved. This total energy is the sum of the system's kinetic energy $T$ and potential energy $U$ at any given instant:

$$
E = T + U
$$

The kinetic energy depends on the instantaneous velocity $v$:

$$
T = \frac{1}{2} m v^2
$$

The potential energy is stored in the restoring force mechanism (the spring) and depends on the instantaneous displacement $x$:

$$
U = \frac{1}{2} k x^2
$$

Because the total energy is conserved, we can calculate it using the initial conditions at $t=0$ and rely on that value for the rest of the object's motion.

The natural angular frequency of a mass-spring system is determined solely by its mass and the spring constant:

$$
\omega = \sqrt{\frac{k}{m}}
$$

## Step-by-Step Solution

### 1. Determine the natural frequency

Using the given mass $m = 1\ \mathrm{kg}$ and spring constant $k = 100\ \mathrm{N/m}$, the angular natural frequency is:

$$
\begin{align}
\omega &= \sqrt{\frac{k}{m}} \\
       &= \sqrt{\frac{100}{1}} \\
       &= 10\ \mathrm{rad/s}
\end{align}
$$

The standard frequency $f$ in Hertz is:

$$
\begin{align}
f &= \frac{\omega}{2\pi} \\
  &= \frac{10}{2\pi} \approx 1.59\ \mathrm{Hz}
\end{align}
$$

### 2. Calculate the total energy of the system

The total energy $E$ is conserved and can be found by evaluating the kinetic and potential energies at time $t=0$, using $x(0) = 2\ \mathrm{m}$ and $v(0) = 1\ \mathrm{m/s}$:

$$
\begin{align}
E &= T(0) + U(0) \\
  &= \frac{1}{2} m v(0)^2 + \frac{1}{2} k x(0)^2 \\
  &= \frac{1}{2} (1)(1)^2 + \frac{1}{2} (100)(2)^2 \\
  &= 0.5 + 50(4) \\
  &= 0.5 + 200 \\
  &= 200.5\ \mathrm{J}
\end{align}
$$

The total mechanical energy of the system is $200.5\ \mathrm{J}$.

### 3. Displacement where kinetic energy is 50% of total energy

We need to find the displacement $x$ at which the kinetic energy $T$ is exactly half of the total energy $E$:

$$
T = 0.5 E
$$

Since $E = T + U$, if the kinetic energy makes up 50% of the total energy, the potential energy must make up the remaining 50%:

$$
U = 0.5 E
$$

Substitute the expression for potential energy and the known value of total energy ($E = 200.5\ \mathrm{J}$):

$$
\frac{1}{2} k x^2 = 0.5 E
$$

Multiply both sides by 2:

$$
k x^2 = E
$$

Now, solve for the displacement $x$:

$$
\begin{align}
x^2 &= \frac{E}{k} \\
    &= \frac{200.5}{100} \\
    &= 2.005\ \mathrm{m^2}
\end{align}
$$

Take the square root to find $x$:

$$
x = \pm \sqrt{2.005} \approx \pm 1.416\ \mathrm{m}
$$

## Final Result

- **Natural frequency:** $\omega = 10\ \mathrm{rad/s}$ (or $f \approx 1.59\ \mathrm{Hz}$)
- **Total energy:** $E = 200.5\ \mathrm{J}$
- **Displacement for 50% kinetic energy:** $x = \pm\sqrt{2.005}\ \mathrm{m} \approx \pm 1.416\ \mathrm{m}$

## Interpretation

The total energy of $200.5\ \mathrm{J}$ dictates the maximum possible boundaries of the motion. The amplitude (maximum displacement, where $T=0$) would be $x_{\max} = \sqrt{\frac{2E}{k}} \approx 2.0025\ \mathrm{m}$, which is very close to the initial position. The points where energy is split equally between kinetic and potential ($x \approx \pm 1.416\ \mathrm{m}$) occur at $1/\sqrt{2} \approx 70.7\%$ of the maximum amplitude. Because energy depends on the *square* of displacement, the halfway point for energy is not the physical halfway point of the spatial trajectory.