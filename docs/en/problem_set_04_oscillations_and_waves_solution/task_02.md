# Task 02 – Energy of a Harmonic Oscillator

## Problem Statement

A system with the following initial parameters is given:

* $m = 1\ \text{kg}$
* $k = 100\ \text{N/m}$
* $x(0) = 2\ \text{m}$
* $v(0) = 1\ \text{m/s}$

1. Determine the natural frequency.
2. Calculate the total energy of the system.
3. For what displacement does the kinetic energy account for 50% of the total energy?

## Theory

The total mechanical energy $E$ of a harmonic oscillator is the sum of its kinetic energy $T$ and potential energy $U$. In an ideal system without damping, this total energy remains constant over time.

The formulas for these energies are:
* **Kinetic Energy:** $T = \frac{1}{2}mv^2$
* **Potential Energy:** $U = \frac{1}{2}kx^2$
* **Total Energy:** $E = T + U = \frac{1}{2}kA^2$, where $A$ is the amplitude.

The natural angular frequency $\omega_0$ represents the rate of oscillation determined by the physical properties of the system (mass and stiffness).



## Step-by-Step Solution

### 1. Determining the Natural Frequency

The natural angular frequency $\omega_0$ is calculated using the mass $m$ and the spring constant $k$:

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

Substituting the given values ($k = 100\ \text{N/m}$, $m = 1\ \text{kg}$):

$$
\omega_0 = \sqrt{\frac{100}{1}} = 10\ \text{rad/s}
$$

### 2. Calculating Total Energy

Since energy is conserved, we can calculate the total energy $E$ using the initial state of the system ($x_0, v_0$):

$$
E = T(0) + U(0)
$$

$$
E = \frac{1}{2}mv(0)^2 + \frac{1}{2}kx(0)^2
$$

Substituting the values:

$$
E = \frac{1}{2}(1)(1)^2 + \frac{1}{2}(100)(2)^2
$$

$$
E = 0.5 + 200 = 200.5\ \text{J}
$$

### 3. Finding Displacement for 50% Kinetic Energy

We are looking for the displacement $x$ where $T = 0.5E$. Because $E = T + U$, if $T = 0.5E$, then $U$ must also equal $0.5E$:

$$
U = 0.5 E
$$

$$
\frac{1}{2}kx^2 = 0.5 E
$$

Solving for $x$:

$$
x^2 = \frac{E}{k}
$$

$$
x = \pm \sqrt{\frac{E}{k}}
$$

Substituting the calculated total energy $E = 200.5\ \text{J}$ and $k = 100\ \text{N/m}$:

$$
x = \pm \sqrt{\frac{200.5}{100}} = \pm \sqrt{2.005} \approx \pm 1.416\ \text{m}
$$

## Final Result

* **Natural Frequency**: $\omega_0 = 10\ \text{rad/s}$
* **Total Energy**: $E = 200.5\ \text{J}$
* **Specific Displacement**: $x \approx \pm 1.416\ \text{m}$

## Interpretation

The total energy of the system is dominated by the initial potential energy ($200\ \text{J}$) compared to the relatively small initial kinetic energy ($0.5\ \text{J}$). As the system oscillates, the energy shifts between these two forms. The point where the energy is split equally ($50/50$) occurs at a displacement $x = A/\sqrt{2}$. Since the total energy $E = \frac{1}{2}kA^2$, the amplitude $A$ for this system is $\sqrt{2E/k} \approx 2.0025\ \text{m}$, and the calculated displacement $1.416\ \text{m}$ correctly corresponds to $A/\sqrt{2}$.