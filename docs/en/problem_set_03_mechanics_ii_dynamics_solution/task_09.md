# Task 09 – Potential and conservative field

## Problem Statement

A particle moves in a two-dimensional potential energy field given by:

$$
U(x, y) = \frac{k}{2}(x^2 + y^2)
$$

The required operations are:
1. Determine the force $\vec F(x, y)$ as the negative gradient of the potential.
2. Write down the equations of motion for $x(t)$ and $y(t)$.
3. Identify the type of motion described by these equations.
4. Determine the total mechanical energy $E$.
5. Interpret the trajectory geometrically and present it in an HTML/JS application.

## Theory

A force field is **conservative** if the work done by the force on a particle moving between two points is independent of the path taken. For such fields, a scalar potential energy function $U(\vec r)$ exists such that the force is the negative gradient of the potential:

$$
\vec F = -\nabla U = -\left( \frac{\partial U}{\partial x}, \frac{\partial U}{\partial y}, \frac{\partial U}{\partial z} \right)
$$

In 2D Cartesian coordinates, the equations of motion are derived from Newton's Second Law:

$$
m\ddot x = F_x, \qquad m\ddot y = F_y
$$

The total energy $E = K + U$ is a constant of motion. Geometrically, the potential $U(x, y) = \frac{k}{2}(x^2 + y^2)$ represents a **2D isotropic harmonic potential**, which looks like a paraboloid centered at the origin.

## Step-by-Step Solution

### 1. Determine the force $\vec F(x, y)$

The force is the negative gradient of $U(x, y) = \frac{k}{2}x^2 + \frac{k}{2}y^2$:

**x-component:**
$$
F_x = -\frac{\partial U}{\partial x} = -\frac{\partial}{\partial x} \left( \frac{k}{2}x^2 + \frac{k}{2}y^2 \right) = -kx
$$

**y-component:**
$$
F_y = -\frac{\partial U}{\partial y} = -\frac{\partial}{\partial y} \left( \frac{k}{2}x^2 + \frac{k}{2}y^2 \right) = -ky
$$

Thus, the force vector is:
$$
\vec F = (-kx, -ky) = -k\vec r
$$
This is a **central restoring force** directed toward the origin.

### 2. Write the equations of motion

Using $m\vec a = \vec F$:

$$
m\ddot x = -kx \implies \ddot x + \frac{k}{m}x = 0
$$
$$
m\ddot y = -ky \implies \ddot y + \frac{k}{m}y = 0
$$

### 3. Identify the type of motion

These are two independent simple harmonic oscillator equations with the same natural frequency $\omega_0 = \sqrt{k/m}$. 

The general solutions are:
$$
x(t) = A_x \cos(\omega_0 t + \phi_x)
$$
$$
y(t) = A_y \cos(\omega_0 t + \phi_y)
$$

This is a **2D Isotropic Harmonic Oscillator**. Depending on the phase difference $\Delta \phi = \phi_y - \phi_x$, the trajectory will be a line, a circle, or an ellipse.

### 4. Determine total energy $E$

The total energy is the sum of kinetic and potential energies:

$$
E = \frac{1}{2}m(\dot x^2 + \dot y^2) + \frac{1}{2}k(x^2 + y^2)
$$

Since each dimension is an independent oscillator, the total energy is the sum of the energies of the $x$ and $y$ motions:
$$
E = E_x + E_y = \frac{1}{2}k A_x^2 + \frac{1}{2}k A_y^2
$$

### 5. Geometric Interpretation

[Image of 3D paraboloid potential energy surface with an elliptical orbit at the bottom]

The potential $U(x, y)$ forms a "bowl" (paraboloid). A particle placed in this bowl will oscillate back and forth. Because the restoring constant $k$ is the same in all directions (isotropic), the orbits are closed ellipses centered at the origin.

## Final Result

* Force: $\vec F = -k(x, y)$
* Equations of Motion: $\ddot x + \omega_0^2 x = 0$ and $\ddot y + \omega_0^2 y = 0$
* Motion Type: 2D Isotropic Harmonic Motion (Elliptical orbits)
* Total Energy: $E = \frac{1}{2}k(A_x^2 + A_y^2)$