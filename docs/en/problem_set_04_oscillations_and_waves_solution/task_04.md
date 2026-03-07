# Task 04 – Wave Equation

## Problem Statement

The function is given:

$$
y(x,t) = A \cos(kx - \omega t)
$$

1. Verify that it satisfies the wave equation:
$$
\frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2}
$$
2. Determine the relationship between $v$, $k$, and $\omega$.

## Theory

The linear wave equation is a second-order partial differential equation that describes the propagation of waves through a medium. It relates the acceleration of a point in the medium (the second temporal derivative) to the curvature of the wave profile at that point (the second spatial derivative).

For a function to be a solution to the wave equation, its second derivatives must be proportional to each other, with the constant of proportionality being the square of the propagation speed $v^2$.

## Step-by-Step Solution

### 1. Calculating Partial Derivatives

To verify the wave equation, we must calculate the second partial derivatives of $y(x,t) = A \cos(kx - \omega t)$.

**Temporal Derivatives:**
First derivative with respect to $t$:

$$
\frac{\partial y}{\partial t} = -A \sin(kx - \omega t) \cdot (-\omega) = A\omega \sin(kx - \omega t)
$$

Second derivative with respect to $t$:

$$
\frac{\partial^2 y}{\partial t^2} = A\omega \cos(kx - \omega t) \cdot (-\omega) = -A\omega^2 \cos(kx - \omega t)
$$

**Spatial Derivatives:**
First derivative with respect to $x$:

$$
\frac{\partial y}{\partial x} = -A \sin(kx - \omega t) \cdot (k) = -Ak \sin(kx - \omega t)
$$

Second derivative with respect to $x$:

$$
\frac{\partial^2 y}{\partial x^2} = -Ak \cos(kx - \omega t) \cdot (k) = -Ak^2 \cos(kx - \omega t)
$$

### 2. Verification and Algebraic Relationship

We substitute the second derivatives into the wave equation:

$$
-A\omega^2 \cos(kx - \omega t) = v^2 \left[ -Ak^2 \cos(kx - \omega t) \right]
$$

Dividing both sides by $-A \cos(kx - \omega t)$ (assuming $A \neq 0$):

$$
\omega^2 = v^2 k^2
$$

Solving for $v^2$:

$$
v^2 = \frac{\omega^2}{k^2}
$$

Taking the square root:

$$
v = \frac{\omega}{k}
$$

This algebraic relation shows that the given cosine function satisfies the wave equation provided that the velocity $v$ is equal to the ratio of the angular frequency to the wave number.

## Final Result

* **Verification**: The function satisfies the equation because $\frac{\partial^2 y}{\partial t^2}$ and $\frac{\partial^2 y}{\partial x^2}$ are both proportional to the original function $\cos(kx - \omega t)$.
* **Relationship**: The wave speed is given by $v = \frac{\omega}{k}$.

## Interpretation

The wave equation implies that the local "bending" of the medium $(\partial^2 y / \partial x^2)$ provides the restoring force that drives the acceleration $(\partial^2 y / \partial t^2)$. The relationship $v = \omega/k$ connects the temporal frequency of oscillation to the spatial wavelength. It confirms that for a given medium where $v$ is constant, higher frequency waves must have proportionally higher wave numbers, meaning shorter wavelengths.