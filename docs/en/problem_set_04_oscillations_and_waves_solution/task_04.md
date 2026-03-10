# Task 04 – Wave equation

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

The linear wave equation is a second-order linear partial differential equation that describes the propagation of waves—such as sound or light—through a medium or space. The equation relates the second spatial derivative of the wave's displacement to its second temporal derivative. 

To verify if a specific function is a valid solution to this wave equation, we must compute its second partial derivative with respect to time ($t$) and its second partial derivative with respect to space ($x$), and then substitute them back into the governing equation.

## Step-by-Step Solution

### 1. Verify that the function satisfies the wave equation

Given the wave function:

$$
y(x,t) = A \cos(kx - \omega t)
$$

First, we calculate the partial derivatives with respect to time $t$. Treating $x$ as a constant, the first derivative is:

$$
\begin{align}
\frac{\partial y}{\partial t} &= \frac{\partial}{\partial t} [A \cos(kx - \omega t)] \\
                              &= -A \sin(kx - \omega t) \cdot \frac{\partial}{\partial t}(kx - \omega t) \\
                              &= -A \sin(kx - \omega t) \cdot (-\omega) \\
                              &= A\omega \sin(kx - \omega t)
\end{align}
$$

Taking the derivative again with respect to time yields the second partial derivative:

$$
\begin{align}
\frac{\partial^2 y}{\partial t^2} &= \frac{\partial}{\partial t} [A\omega \sin(kx - \omega t)] \\
                                  &= A\omega \cos(kx - \omega t) \cdot (-\omega) \\
                                  &= -A\omega^2 \cos(kx - \omega t)
\end{align}
$$

Next, we calculate the partial derivatives with respect to position $x$. Treating $t$ as a constant, the first derivative is:

$$
\begin{align}
\frac{\partial y}{\partial x} &= \frac{\partial}{\partial x} [A \cos(kx - \omega t)] \\
                              &= -A \sin(kx - \omega t) \cdot \frac{\partial}{\partial x}(kx - \omega t) \\
                              &= -A \sin(kx - \omega t) \cdot (k) \\
                              &= -Ak \sin(kx - \omega t)
\end{align}
$$

Taking the derivative again with respect to position yields the second partial derivative:

$$
\begin{align}
\frac{\partial^2 y}{\partial x^2} &= \frac{\partial}{\partial x} [-Ak \sin(kx - \omega t)] \\
                                  &= -Ak \cos(kx - \omega t) \cdot (k) \\
                                  &= -Ak^2 \cos(kx - \omega t)
\end{align}
$$

Now, substitute both second partial derivatives into the classical wave equation:

$$
\frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2}
$$

$$
-A\omega^2 \cos(kx - \omega t) = v^2 \left( -Ak^2 \cos(kx - \omega t) \right)
$$

Since $-A \cos(kx - \omega t)$ is common to both sides, we can divide it out (assuming $A \neq 0$ and we are not at a node where the cosine is zero):

$$
\omega^2 = v^2 k^2
$$

This equality holds true as long as we define $v$ appropriately, meaning the function mathematically satisfies the wave equation.

### 2. Determine the relationship between $v$, $k$, and $\omega$

From the verification step, we established the required condition:

$$
\omega^2 = v^2 k^2
$$

Taking the positive square root of both sides (since wave speed, angular frequency, and wave number are defined as positive physical quantities):

$$
\omega = v k
$$

Solving for the phase velocity $v$:

$$
v = \frac{\omega}{k}
$$

## Final Result

- The function mathematically satisfies the wave equation,a resulting in the characteristic identity $\omega^2 = v^2 k^2$.
- The relationship between the parameters is:
$$
v = \frac{\omega}{k}
$$

## Interpretation

The linear wave equation dictates that the acceleration of a point on the wave (the second time derivative) is directly proportional to the curvature of the wave at that point (the second spatial derivative). The constant of proportionality is the square of the wave's propagation speed ($v^2$). The derived relationship $v = \omega / k$ shows that the speed of the wave is exclusively determined by the ratio of how fast it oscillates in time ($\omega$) to how tightly it is packed in space ($k$).