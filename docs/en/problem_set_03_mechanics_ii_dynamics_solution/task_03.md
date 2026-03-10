# Task 03 – Work of a variable force

## Problem Statement

Given a one-dimensional force:

$$
F(x)=-kx
$$

1. Write down the equation of motion and solve it.
2. Calculate the work done during the displacement from $0$ to $x_0$.
3. Interpret the result as potential energy.
4. Verify the relationship $F = -\frac{dU}{dx}$.
5. Draw the graph of $F(x)$ and $U(x)$.

## Theory

A restoring force proportional to displacement (Hooke's Law) describes a simple harmonic oscillator. The equation of motion results in a second-order linear differential equation, giving solutions involving sine and cosine functions.

The work done by a variable force in one dimension is found by integrating the force over the displacement:

$$
W = \int_{x_i}^{x_f} F(x) \, dx
$$

If the force is conservative, the work done by it is exactly equal to the negative change in potential energy $U$:

$$
\Delta U = -W
$$

This leads to the fundamental relation defining a conservative force from its potential energy field:

$$
F(x) = -\frac{dU}{dx}
$$

## Step-by-Step Solution

### 1. Equation of motion and solution

Using Newton's Second Law:

$$
m \ddot{x} = F(x)
$$

Substituting the given force:

$$
m \ddot{x} = -kx
$$

Dividing by mass $m$:

$$
\ddot{x} + \frac{k}{m} x = 0
$$

Let $\omega^2 = \frac{k}{m}$. This gives the standard simple harmonic oscillator equation:

$$
\ddot{x} + \omega^2 x = 0
$$

The general solution is a linear combination of trigonometric functions:

$$
x(t) = A \cos(\omega t) + B \sin(\omega t)
$$

where $A$ and $B$ are constants determined by initial conditions.

### 2. Work done from $0$ to $x_0$

The work done by the force is calculated using the definite integral:

$$
W = \int_0^{x_0} F(x) \, dx
$$

Substitute $F(x) = -kx$:

$$
\begin{align}
W &= \int_0^{x_0} (-kx) \, dx \\
  &= \left[ -\frac{1}{2} k x^2 \right]_0^{x_0} \\
  &= -\frac{1}{2} k x_0^2 - (-0) \\
  &= -\frac{1}{2} k x_0^2
\end{align}
$$

### 3. Interpretation as potential energy

Because the force is conservative, the change in potential energy is the negative of the work done by the force:

$$
\begin{align}
\Delta U &= -W \\
U(x_0) - U(0) &= -\left( -\frac{1}{2} k x_0^2 \right) \\
U(x_0) - U(0) &= \frac{1}{2} k x_0^2
\end{align}
$$

By standard convention, we set the potential energy at the equilibrium position to zero ($U(0) = 0$). Therefore, the potential energy function at any general position $x$ is:

$$
U(x) = \frac{1}{2} k x^2
$$

### 4. Verify the relationship $F = -\frac{dU}{dx}$

Given our derived expression $U(x) = \frac{1}{2} k x^2$, calculate the negative derivative with respect to $x$:

$$
\begin{align}
-\frac{dU}{dx} &= -\frac{d}{dx} \left( \frac{1}{2} k x^2 \right) \\
               &= -\frac{1}{2} k (2x) \\
               &= -kx
\end{align}
$$

This perfectly matches the original force equation $F(x) = -kx$, verifying the mathematical consistency of the potential energy definition.

## Final Result

- **Equation of motion:** $m \ddot{x} + kx = 0$
- **General solution:** $x(t) = A \cos\left(\sqrt{\frac{k}{m}} t\right) + B \sin\left(\sqrt{\frac{k}{m}} t\right)$
- **Work ($0 \to x_0$):** $W = -\frac{1}{2} k x_0^2$
- **Potential Energy:** $U(x) = \frac{1}{2} k x^2$
- **Verification:** $-\frac{dU}{dx} = -kx = F(x)$

## Interpretation

The negative sign of the work done indicates that the restoring force acts in the opposite direction to the displacement, extracting kinetic energy from the particle and storing it. This stored energy exactly defines the potential energy field $U(x)$, which takes the shape of an upward-opening parabola. Because the potential energy is quadratic, the force (its negative derivative) must be linear.