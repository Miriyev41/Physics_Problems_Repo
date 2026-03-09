# Task 03 – Work of a variable force

## Problem Statement

Given a one-dimensional force:

$$
F(x) = -kx
$$

The required operations are:
1. Write down the equation of motion and solve it.
2. Calculate the work done during the displacement from $0$ to $x_0$.
3. Interpret the result as potential energy.
4. Verify the relationship $F = -\frac{dU}{dx}$.
5. Draw the graph of $F(x)$ and $U(x)$.

## Theory

Newton's Second Law for a one-dimensional system is $F = m\ddot{x}$. When the force depends on the position $x$, the equation of motion becomes a differential equation. Specifically, $F(x) = -kx$ describes a linear restoring force, characteristic of a **Hookean spring**.

Work $W$ done by a variable force over a path from $x_1$ to $x_2$ is defined by the integral:

$$
W = \int_{x_1}^{x_2} F(x) \, dx
$$

In a conservative force field, the work done by an external agent against the field is stored as potential energy $U$. The change in potential energy is defined as the negative of the work done by the conservative force:

$$
\Delta U = -W_{field} = -\int_{x_1}^{x_2} F(x) \, dx
$$

This leads to the fundamental relationship between force and potential:

$$
F(x) = -\frac{dU}{dx}
$$

## Step-by-Step Solution

### 1. Write and solve the equation of motion

**Step 1: Set up the differential equation**

Substitute $F = -kx$ into Newton's Second Law $m\frac{d^2x}{dt^2} = F$:

$$
m\frac{d^2x}{dt^2} = -kx
$$

Rearrange into the standard form of a second-order linear homogeneous ODE:

$$
\frac{d^2x}{dt^2} + \frac{k}{m}x = 0
$$

**Step 2: Define the natural frequency**

Let $\omega^2 = \frac{k}{m}$. The equation becomes:

$$
\ddot{x} + \omega^2 x = 0
$$

**Step 3: Provide the general solution**

This is the equation for Simple Harmonic Motion (SHM). The general solution is:

$$
x(t) = A\cos(\omega t + \phi)
$$

where $A$ is the amplitude and $\phi$ is the phase constant.

### 2. Calculate the work done from $0$ to $x_0$

Calculate the integral of the force $F(x) = -kx$ over the interval $[0, x_0]$:

$$
\begin{align}
W &= \int_{0}^{x_0} (-kx) \, dx \\
  &= -k \int_{0}^{x_0} x \, dx \\
  &= -k \left[ \frac{1}{2}x^2 \right]_0^{x_0} \\
  &= -k \left( \frac{1}{2}x_0^2 - 0 \right)
\end{align}
$$

$$
W = -\frac{1}{2}kx_0^2
$$

### 3. Interpret the result as potential energy

The work done *by the force* is negative because the force (pointing toward the origin) opposes the displacement (pointing away from the origin). The potential energy $U(x)$ is defined as the work required by an *external agent* to move the body, which is $-W$:

$$
U(x_0) = -W = \frac{1}{2}kx_0^2
$$

Assuming $U(0) = 0$, the potential energy function is:

$$
U(x) = \frac{1}{2}kx^2
$$

### 4. Verify the relationship $F = -dU/dx$

Take the negative derivative of the potential energy function $U(x) = \frac{1}{2}kx^2$ with respect to $x$:

$$
\begin{align}
-\frac{dU}{dx} &= -\frac{d}{dx} \left( \frac{1}{2}kx^2 \right) \\
               &= -\frac{1}{2}k (2x) \\
               &= -kx
\end{align}
$$

Since $-kx$ is exactly the original force $F(x)$, the relationship is verified.

## Final Result

* Equation of motion: $m\ddot{x} + kx = 0$
* General solution: $x(t) = A\cos(\sqrt{\frac{k}{m}}t + \phi)$
* Work done by the force: $W = -\frac{1}{2}kx_0^2$
* Potential energy: $U(x) = \frac{1}{2}kx^2$
* Verification: $-\frac{dU}{dx} = -kx = F(x)$

## Interpretation



The linear restoring force $F(x) = -kx$ leads to a quadratic potential energy $U(x) = \frac{1}{2}kx^2$, often called a **potential well**. In this well, the origin $x=0$ is a point of stable equilibrium because it represents the minimum of the potential energy. If the particle is displaced, the force always acts to push it back toward this minimum. The negative work calculated indicates that as the particle moves away from equilibrium, kinetic energy is being converted into stored potential energy.