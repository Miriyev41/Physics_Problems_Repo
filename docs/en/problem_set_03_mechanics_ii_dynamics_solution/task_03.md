# Task 03 – Work of a Variable Force

## Problem Statement

Given a one-dimensional force:

$$
F(x) = -kx
$$

* Write down the equation of motion and solve it.
* Calculate the work done during the displacement from $0$ to $x_0$.
* Interpret the result as potential energy.
* Verify the relationship $F = -\frac{dU}{dx}$.
* Draw the graph of $F(x)$ and $U(x)$.

## Theory

When a force depends on the position of an object, it is a variable force. The work done by such a force is calculated using integration over the path of motion:

$$
W = \int_{x_1}^{x_2} F(x) \, dx
$$

According to Newton's Second Law, the equation of motion is $m\ddot{x} = F(x)$. For a conservative force, the work done by the force is equal to the negative change in potential energy $U$:

$$
W = -\Delta U = -(U(x_2) - U(x_1))
$$

This leads to the fundamental differential relationship between force and potential:

$$
F(x) = -\frac{dU}{dx}
$$

## Step-by-Step Solution

### 1. Equation of Motion

Substituting the force law $F(x) = -kx$ into Newton's Second Law:

$$
m \frac{d^2x}{dt^2} = -kx
$$

Rearranging into the standard form of a linear homogeneous differential equation:

$$
\frac{d^2x}{dt^2} + \frac{k}{m}x = 0
$$

Defining the natural frequency $\omega^2 = \frac{k}{m}$, the general solution is harmonic:

$$
x(t) = A \cos(\omega t + \phi)
$$

### 2. Calculation of Work

The work done by the force as the body moves from $x = 0$ to $x = x_0$ is:

$$
W = \int_{0}^{x_0} (-kx) \, dx
$$

$$
W = -k \left[ \frac{1}{2}x^2 \right]_{0}^{x_0}
$$

$$
W = -\frac{1}{2}kx_0^2
$$

### 3. Potential Energy Interpretation

Since $W = -\Delta U$ and defining $U(0) = 0$:

$$
-\frac{1}{2}kx_0^2 = -(U(x_0) - U(0))
$$

The potential energy of the system at position $x$ is:

$$
U(x) = \frac{1}{2}kx^2
$$

### 4. Verification of the Force-Potential Relationship

To verify the relationship, we take the negative derivative of the potential energy function:

$$
-\frac{dU}{dx} = -\frac{d}{dt} \left( \frac{1}{2}kx^2 \right)
$$

$$
-\frac{dU}{dx} = - \left( \frac{1}{2}k \cdot 2x \right) = -kx
$$

This matches the original expression for $F(x)$, confirming the force is conservative.

## Final Result

* **Equation of Motion**: $\ddot{x} + \frac{k}{m}x = 0$
* **Work Done**: $W = -\frac{1}{2}kx_0^2$
* **Potential Energy**: $U(x) = \frac{1}{2}kx^2$
* **Derivative Check**: $-\frac{dU}{dx} = -kx = F$

## Interpretation

The negative sign in the work calculation indicates that the force acts in the opposite direction of the displacement (a restoring force). The energy is not "lost" but is stored as elastic potential energy in the system. The quadratic nature of the potential energy $U(x)$ creates a "potential well," which explains why the resulting motion is oscillatory around the equilibrium point $x=0$.