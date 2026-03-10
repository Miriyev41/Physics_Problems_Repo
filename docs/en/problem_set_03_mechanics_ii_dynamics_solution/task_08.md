# Task 08 – Harmonic oscillator (formal dynamics)

## Problem Statement

The equation of motion for a simple harmonic oscillator is given by:

$$
m\ddot x + kx = 0
$$

1. Solve the equation.
2. Determine the natural frequency.
3. Write down the energy as a function of time.
4. Show that energy is conserved.
5. Interpret the motion in phase space.

## Theory



A simple harmonic oscillator represents a system where the restoring force is directly proportional to the displacement from equilibrium (Hooke's Law). Its dynamics are described by a second-order linear homogeneous differential equation with constant coefficients.

The "phase space" of a 1D dynamical system is a two-dimensional plot where the horizontal axis represents the position $x$ and the vertical axis represents the momentum $p$ (or velocity $v = \dot{x}$). The state of the system at any instant is a single point in this space, and as time progresses, the system traces out a continuous trajectory called a phase portrait.

## Step-by-Step Solution

### 1. Solve the equation

Starting with the given equation of motion:

$$
m\ddot x + kx = 0
$$

Divide the entire equation by the mass $m$:

$$
\ddot x + \frac{k}{m} x = 0
$$

Let us define a constant $\omega_0^2 = \frac{k}{m}$. The equation becomes:

$$
\ddot x + \omega_0^2 x = 0
$$

This is the standard form of the harmonic oscillator equation. Its general solution can be written using trigonometric functions:

$$
x(t) = A \cos(\omega_0 t + \phi)
$$

where $A$ is the amplitude and $\phi$ is the initial phase. The velocity is the first time derivative:

$$
\begin{align}
v(t) &= \dot{x}(t) \\
     &= \frac{d}{dt} \left[ A \cos(\omega_0 t + \phi) \right] \\
     &= -A\omega_0 \sin(\omega_0 t + \phi)
\end{align}
$$

### 2. Determine the natural frequency

The parameter $\omega_0$ represents the angular natural frequency of the oscillator. From our substitution $\omega_0^2 = \frac{k}{m}$, we immediately find:

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

The standard natural frequency $f_0$ (in Hertz) is related to the angular frequency by $\omega_0 = 2\pi f_0$, giving:

$$
f_0 = \frac{1}{2\pi} \sqrt{\frac{k}{m}}
$$

### 3. Write down the energy as a function of time

The total mechanical energy $E(t)$ is the sum of the kinetic energy $T(t)$ and the potential energy $U(t)$.

The potential energy of a spring is:

$$
U(t) = \frac{1}{2} k x(t)^2 = \frac{1}{2} k A^2 \cos^2(\omega_0 t + \phi)
$$

The kinetic energy is:

$$
T(t) = \frac{1}{2} m v(t)^2 = \frac{1}{2} m \left( -A\omega_0 \sin(\omega_0 t + \phi) \right)^2 = \frac{1}{2} m A^2 \omega_0^2 \sin^2(\omega_0 t + \phi)
$$

Since $\omega_0^2 = \frac{k}{m}$, we can substitute $m\omega_0^2 = k$ into the kinetic energy expression:

$$
T(t) = \frac{1}{2} k A^2 \sin^2(\omega_0 t + \phi)
$$

The total energy as a function of time is:

$$
E(t) = T(t) + U(t) = \frac{1}{2} k A^2 \sin^2(\omega_0 t + \phi) + \frac{1}{2} k A^2 \cos^2(\omega_0 t + \phi)
$$

### 4. Show that energy is conserved

Factor out the common term $\frac{1}{2} k A^2$ from the total energy equation:

$$
E(t) = \frac{1}{2} k A^2 \left[ \sin^2(\omega_0 t + \phi) + \cos^2(\omega_0 t + \phi) \right]
$$

Using the fundamental Pythagorean trigonometric identity $\sin^2\theta + \cos^2\theta = 1$:

$$
E(t) = \frac{1}{2} k A^2 (1) = \frac{1}{2} k A^2
$$

Because both the spring constant $k$ and the amplitude $A$ are constants determined by the physical system and initial conditions, the total energy $E(t)$ does not depend on time $t$. Therefore, the total mechanical energy is strictly conserved.

### 5. Interpret the motion in phase space

Consider the equations for position and velocity normalized by their maximum amplitudes:

$$
\frac{x(t)}{A} = \cos(\omega_0 t + \phi)
$$

$$
\frac{v(t)}{A\omega_0} = -\sin(\omega_0 t + \phi)
$$

Square both equations and add them together:

$$
\left( \frac{x}{A} \right)^2 + \left( \frac{v}{A\omega_0} \right)^2 = \cos^2(\omega_0 t + \phi) + \sin^2(\omega_0 t + \phi)
$$

$$
\frac{x^2}{A^2} + \frac{v^2}{(A\omega_0)^2} = 1
$$

This is the standard equation of an **ellipse** in the $(x, v)$ plane. 

## Final Result

- **Solution:** $x(t) = A \cos(\omega_0 t + \phi)$
- **Natural Frequency:** $\omega_0 = \sqrt{\frac{k}{m}}$
- **Kinetic Energy:** $T(t) = \frac{1}{2} k A^2 \sin^2(\omega_0 t + \phi)$
- **Potential Energy:** $U(t) = \frac{1}{2} k A^2 \cos^2(\omega_0 t + \phi)$
- **Total Energy:** $E = \frac{1}{2} k A^2$ (Constant)
- **Phase Space:** The trajectory forms an ellipse governed by $\frac{x^2}{A^2} + \frac{v^2}{(A\omega_0)^2} = 1$.

## Interpretation

In phase space, the motion of a conservative harmonic oscillator traces out closed elliptical orbits. The fact that the orbit is closed strictly indicates that the motion is periodic; the system perfectly returns to its initial state $(x_0, v_0)$ after one full period $T = \frac{2\pi}{\omega_0}$. The size of the ellipse correlates directly with the total energy of the system. Larger ellipses represent higher energy states. Furthermore, because the trajectory never spirals inwards or outwards, it graphically confirms that energy is neither being lost to friction nor being added by an external driving force.