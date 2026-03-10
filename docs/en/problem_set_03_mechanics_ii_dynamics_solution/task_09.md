# Task 09 – Potential and conservative field

## Problem Statement

Given the potential energy:

$$
U(x,y) = \frac{k}{2}(x^2+y^2)
$$

1. Determine the force as the gradient of the potential.
2. Write down the equations of motion.
3. Determine the type of motion.
4. Determine the total energy.
5. Interpret the trajectory geometrically, presenting it in an HTML/JS application.

## Theory

[Image of 2D isotropic harmonic oscillator potential well and elliptical trajectory]

A force field is conservative if it can be expressed as the negative gradient of a scalar potential energy function $U(x,y)$. In two dimensions, the gradient operator is $\nabla = \left( \frac{\partial}{\partial x}, \frac{\partial}{\partial y} \right)$, so the force vector is:

$$
\vec F = -\nabla U = \left( -\frac{\partial U}{\partial x}, -\frac{\partial U}{\partial y} \right)
$$

The equations of motion are found by applying Newton's Second Law ($\vec F = m\vec a$) to each coordinate independently.

For a conservative system, the total mechanical energy $E$, which is the sum of kinetic energy $T$ and potential energy $U$, is constant over time.

## Step-by-Step Solution

### 1. Determine the force as the gradient of the potential

Given $U(x,y) = \frac{k}{2}x^2 + \frac{k}{2}y^2$, we calculate the partial derivatives:

$$
\begin{align}
F_x &= -\frac{\partial U}{\partial x} \\
    &= -\frac{\partial}{\partial x} \left( \frac{k}{2}x^2 + \frac{k}{2}y^2 \right) \\
    &= -kx
\end{align}
$$

$$
\begin{align}
F_y &= -\frac{\partial U}{\partial y} \\
    &= -\frac{\partial}{\partial y} \left( \frac{k}{2}x^2 + \frac{k}{2}y^2 \right) \\
    &= -ky
\end{align}
$$

The force vector is:

$$
\vec F(x,y) = (-kx, -ky) = -k\vec r
$$

This represents a central restoring force that is always directed towards the origin and proportional to the distance from it.

### 2. Write down the equations of motion

Using Newton's Second Law ($m\ddot{\vec r} = \vec F$):

$$
m\ddot{x} = -kx \implies \ddot{x} + \frac{k}{m}x = 0
$$

$$
m\ddot{y} = -ky \implies \ddot{y} + \frac{k}{m}y = 0
$$

### 3. Determine the type of motion

The equations of motion describe two independent simple harmonic oscillators, one in the $x$-direction and one in the $y$-direction. Both oscillators share the exact same natural angular frequency:

$$
\omega = \sqrt{\frac{k}{m}}
$$

The general solutions are:

$$
x(t) = A_x \cos(\omega t + \phi_x)
$$

$$
y(t) = A_y \cos(\omega t + \phi_y)
$$

Because the frequencies in both dimensions are identical, this describes a **2D isotropic harmonic oscillator**. The resulting trajectory in the $xy$-plane is generally an **ellipse** centered at the origin. Depending on the initial conditions (the relative amplitudes and phase difference $\phi_y - \phi_x$), this ellipse can degenerate into a circle or a straight line segment.

### 4. Determine the total energy

The total mechanical energy $E$ is the sum of the kinetic energy $T$ and the potential energy $U$:

$$
T = \frac{1}{2} m v^2 = \frac{1}{2} m (\dot{x}^2 + \dot{y}^2)
$$

$$
U = \frac{k}{2}(x^2 + y^2)
$$

So the total energy is:

$$
E = \frac{1}{2} m (\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2)
$$

Since the force is conservative, $E$ is a constant determined entirely by the initial conditions $x_0, y_0, v_{x0}, v_{y0}$.

## Final Result

- **Force vector:** $\vec F = (-kx, -ky)$
- **Equations of motion:** $m\ddot{x} + kx = 0$ and $m\ddot{y} + ky = 0$
- **Type of motion:** 2D Isotropic Harmonic Oscillator (elliptical trajectories).
- **Total energy:** $E = \frac{1}{2} m (\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2) = \text{const}$

## Interpretation

The potential $U(x,y) = \frac{k}{2}(x^2+y^2)$ geometrically represents a 3D paraboloid, often referred to as a "potential well". A physical analogy is a marble rolling smoothly in a perfectly parabolic bowl. The restoring force is completely symmetric (isotropic), meaning there is no preferred direction. As the marble rolls, it trades kinetic and potential energy continuously, tracing out an elliptical path viewed from above. Because there is no friction or driving force, it will orbit within this well indefinitely, conserving its total energy.