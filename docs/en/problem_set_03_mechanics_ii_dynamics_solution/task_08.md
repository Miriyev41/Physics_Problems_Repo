# Task 08 – Harmonic Oscillator (Formal Dynamics)

## Problem Statement

The equation of motion for a simple harmonic oscillator is given by:

$$
m\ddot{x} + kx = 0
$$

* Solve the differential equation.
* Determine the natural frequency $\omega_0$.
* Write down the total energy as a function of time.
* Show that the total energy is conserved.
* Interpret the motion in phase space.

## Theory

A simple harmonic oscillator represents a system where a restoring force is directly proportional to the displacement from equilibrium. This is the dynamical basis for springs, pendulums (at small angles), and molecular vibrations.

The dynamics are governed by a linear second-order homogeneous differential equation. Because the force is conservative, the sum of kinetic and potential energy remains constant throughout the motion.



## Step-by-Step Solution

### 1. Solving the Equation of Motion

Dividing the original equation by $m$:

$$
\ddot{x} + \frac{k}{m}x = 0
$$

We define the natural frequency squared as $\omega_0^2 = \frac{k}{m}$. The equation becomes:

$$
\ddot{x} + \omega_0^2 x = 0
$$

The general solution for this differential equation is:

$$
x(t) = A \cos(\omega_0 t + \phi)
$$

Where $A$ is the amplitude and $\phi$ is the initial phase constant.

### 2. Velocity and Natural Frequency

The velocity $v(t)$ is the first derivative of position:

$$
v(t) = \dot{x}(t) = -A\omega_0 \sin(\omega_0 t + \phi)
$$

The natural frequency is:

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

### 3. Energy as a Function of Time

The total energy $E$ is the sum of kinetic energy ($K$) and potential energy ($U$).

**Kinetic Energy:**

$$
K(t) = \frac{1}{2}m v(t)^2 = \frac{1}{2}m (A^2 \omega_0^2 \sin^2(\omega_0 t + \phi))
$$

Since $\omega_0^2 = k/m$, then $m\omega_0^2 = k$:

$$
K(t) = \frac{1}{2} k A^2 \sin^2(\omega_0 t + \phi)
$$

**Potential Energy:**

$$
U(t) = \frac{1}{2} k x(t)^2 = \frac{1}{2} k A^2 \cos^2(\omega_0 t + \phi)
$$

### 4. Proof of Energy Conservation

Total Energy $E(t) = K(t) + U(t)$:

$$
E(t) = \frac{1}{2} k A^2 \sin^2(\omega_0 t + \phi) + \frac{1}{2} k A^2 \cos^2(\omega_0 t + \phi)
$$

$$
E(t) = \frac{1}{2} k A^2 \left[ \sin^2(\omega_0 t + \phi) + \cos^2(\omega_0 t + \phi) \right]
$$

Using the trigonometric identity $\sin^2\theta + \cos^2\theta = 1$:

$$
E = \frac{1}{2} k A^2
$$

Since $E$ is independent of time $t$, the energy is conserved.

## Final Result

* **Solution**: $x(t) = A \cos(\omega_0 t + \phi)$
* **Natural Frequency**: $\omega_0 = \sqrt{k/m}$
* **Total Energy**: $E = \frac{1}{2} k A^2$ (Constant)

## Interpretation

In phase space (a plot of velocity $v$ vs position $x$), the motion of a harmonic oscillator traces an ellipse. This closed loop signifies periodic motion where energy is continuously traded between kinetic and potential forms without loss. The area of the ellipse is proportional to the total energy of the system.