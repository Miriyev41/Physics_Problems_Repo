# Task 08 – Harmonic oscillator (formal dynamics)

## Problem Statement

The differential equation of motion for a harmonic oscillator is given by:

$$
m\ddot x + kx = 0
$$

The required operations are:
1. Solve the differential equation.
2. Determine the natural frequency $\omega_0$.
3. Write down the total energy $E$ as a function of time.
4. Show that the total energy is conserved ($dE/dt = 0$).
5. Interpret the motion in phase space $(x, v)$.

## Theory

A harmonic oscillator is a system where a particle is subject to a linear restoring force $F = -kx$. According to Newton's Second Law:

$$
m\vec a = \vec F \implies m\ddot x = -kx
$$

This is a second-order, linear, homogeneous ordinary differential equation. The solution is periodic, representing an oscillation around the equilibrium point $x=0$.

The total mechanical energy $E$ is the sum of kinetic energy $K$ and potential energy $U$:

$$
E = \frac{1}{2}m\dot x^2 + \frac{1}{2}kx^2
$$

Phase space is a multidimensional space in which all possible states of a system are represented, with each possible state corresponding to one unique point. For a 1D oscillator, the phase space is a 2D plane with axes representing position $x$ and velocity $v$ (or momentum $p$).

## Step-by-Step Solution

### 1. Solve the differential equation

**Step 1: Standard form**

Divide the equation $m\ddot x + kx = 0$ by $m$:

$$
\ddot x + \frac{k}{m}x = 0
$$

**Step 2: Identify the natural frequency**

We define the square of the natural angular frequency as:

$$
\omega_0^2 = \frac{k}{m} \implies \omega_0 = \sqrt{\frac{k}{m}}
$$

**Step 3: General solution**

The characteristic equation is $r^2 + \omega_0^2 = 0$, giving $r = \pm i\omega_0$. The general real solution is:

$$
x(t) = A\cos(\omega_0 t + \phi)
$$

where $A$ is the amplitude and $\phi$ is the initial phase.

### 2. Determine velocity and energy as functions of time

**Step 1: Velocity $v(t)$**

Differentiate position with respect to time:

$$
v(t) = \dot x(t) = -A\omega_0 \sin(\omega_0 t + \phi)
$$

**Step 2: Total Energy $E(t)$**

Substitute $x(t)$ and $v(t)$ into the energy equation:

$$
E(t) = \frac{1}{2}m \bigl[ -A\omega_0 \sin(\omega_0 t + \phi) \bigr]^2 + \frac{1}{2}k \bigl[ A\cos(\omega_0 t + \phi) \bigr]^2
$$

$$
E(t) = \frac{1}{2}m A^2 \omega_0^2 \sin^2(\omega_0 t + \phi) + \frac{1}{2}k A^2 \cos^2(\omega_0 t + \phi)
$$

Since $m\omega_0^2 = k$:

$$
E(t) = \frac{1}{2}k A^2 \sin^2(\omega_0 t + \phi) + \frac{1}{2}k A^2 \cos^2(\omega_0 t + \phi)
$$

**Step 3: Simplify**

$$
E(t) = \frac{1}{2}k A^2 \bigl[ \sin^2(\omega_0 t + \phi) + \cos^2(\omega_0 t + \phi) \bigr]
$$

Using the identity $\sin^2\theta + \cos^2\theta = 1$:

$$
E = \frac{1}{2}k A^2
$$

### 3. Show that energy is conserved

To prove conservation, we show the time derivative of $E$ is zero:

$$
\frac{dE}{dt} = \frac{d}{dt} \left( \frac{1}{2}m\dot x^2 + \frac{1}{2}kx^2 \right)
$$

Using the chain rule:

$$
\frac{dE}{dt} = m\dot x \ddot x + kx \dot x
$$

Factor out $\dot x$:

$$
\frac{dE}{dt} = \dot x (m\ddot x + kx)
$$

From the original equation of motion, $m\ddot x + kx = 0$. Therefore:

$$
\frac{dE}{dt} = \dot x (0) = 0
$$

The total energy is constant over time.

### 4. Interpret motion in phase space

The state of the system is defined by $(x, v)$. From our energy conservation:

$$
\frac{1}{2}mv^2 + \frac{1}{2}kx^2 = E
$$

Divide by $E$:

$$
\frac{mv^2}{2E} + \frac{kx^2}{2E} = 1
$$

Rearrange into the standard form of an ellipse:

$$
\frac{x^2}{(2E/k)} + \frac{v^2}{(2E/m)} = 1
$$

## Final Result

* Natural frequency: $\omega_0 = \sqrt{k/m}$
* Position: $x(t) = A\cos(\omega_0 t + \phi)$
* Total Energy: $E = \frac{1}{2}kA^2$ (Constant)
* Conservation: $dE/dt = 0$ because work is done by a conservative force.
* Phase space: The trajectory is an **ellipse**.

## Interpretation



The elliptical trajectory in phase space represents the continuous exchange between potential and kinetic energy. When the displacement $x$ is maximum (at the vertices of the ellipse on the x-axis), the velocity $v$ is zero; all energy is potential. When the particle passes through equilibrium $x=0$, the velocity is maximum; all energy is kinetic. Because there is no friction to dissipate energy, the particle stays on the same elliptical path forever, encircling the stable equilibrium point at the origin.