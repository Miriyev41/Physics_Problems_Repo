# Task 09 – Potential and Conservative Field

## Problem Statement

Given a two-dimensional potential energy function:

$$
U(x,y) = \frac{k}{2}(x^2 + y^2)
$$

* Determine the force $\vec{F}$ as the negative gradient of the potential.
* Write down the equations of motion.
* Determine the type of motion.
* Determine the total energy.
* Interpret the trajectory geometrically.

## Theory

A force field is conservative if it can be derived from a scalar potential energy function $U$. The force is defined as the negative gradient of this potential:

$$
\vec{F} = -\nabla U = -\left( \frac{\partial U}{\partial x} \hat{i} + \frac{\partial U}{\partial y} \hat{j} \right)
$$

In such a field, the total mechanical energy $E = T + U$ is a constant of motion. The equations of motion are obtained by substituting the force components into Newton's Second Law:

$$
m\ddot{x} = F_x, \qquad m\ddot{y} = F_y
$$

## Step-by-Step Solution

### 1. Determining the Force Vector

We calculate the partial derivatives of $U(x,y) = \frac{k}{2}x^2 + \frac{k}{2}y^2$:

$$
F_x = -\frac{\partial U}{\partial x} = -\frac{\partial}{\partial x} \left[ \frac{k}{2}x^2 + \frac{k}{2}y^2 \right] = -kx
$$

$$
F_y = -\frac{\partial U}{\partial y} = -\frac{\partial}{\partial y} \left[ \frac{k}{2}x^2 + \frac{k}{2}y^2 \right] = -ky
$$

The force vector is:

$$
\vec{F} = \begin{pmatrix} -kx \\ -ky \end{pmatrix} = -k\vec{r}
$$

### 2. Equations of Motion

Substituting the force components into $m\vec{a} = \vec{F}$:

$$
m\ddot{x} = -kx \implies \ddot{x} + \frac{k}{m}x = 0
$$

$$
m\ddot{y} = -ky \implies \ddot{y} + \frac{k}{m}y = 0
$$

### 3. Type of Motion

Both equations describe a simple harmonic oscillator with the same natural frequency $\omega_0 = \sqrt{k/m}$. 

The general solutions are:

$$
x(t) = A_x \cos(\omega_0 t + \phi_x)
$$

$$
y(t) = A_y \cos(\omega_0 t + \phi_y)
$$

This is a **two-dimensional isotropic harmonic oscillator**.

### 4. Total Energy

The total energy is the sum of kinetic and potential energy:

$$
E = \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{1}{2}k(x^2 + y^2)
$$

Substituting the oscillatory solutions (as shown in Task 08 for a single dimension):

$$
E = \frac{1}{2}k A_x^2 + \frac{1}{2}k A_y^2 = \frac{1}{2}k(A_x^2 + A_y^2)
$$

Since $k$, $A_x$, and $A_y$ are constants, the total energy is conserved.

## Final Result

* **Force**: $\vec{F} = -k\vec{r}$ (Central restoring force)
* **Equations**: $\ddot{x} + \omega_0^2 x = 0$ and $\ddot{y} + \omega_0^2 y = 0$
* **Energy**: $E = \frac{1}{2}k(A_x^2 + A_y^2)$

## Interpretation

Geometrically, the potential $U(x,y)$ represents a **paraboloid** centered at the origin. The resulting trajectories are **Lissajous figures**. Because the frequencies in $x$ and $y$ are identical, the path is generally an **ellipse** centered at the origin. If the phases are equal ($\phi_x = \phi_y$), the motion is linear; if the amplitudes are equal and the phase difference is $90^\circ$, the motion is circular.