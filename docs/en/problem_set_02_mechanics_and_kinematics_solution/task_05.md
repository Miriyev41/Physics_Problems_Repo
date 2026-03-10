# Task 05 – Elliptical motion (purely kinematic)

## Problem Statement

The path equation is given in parametric form:

$$
x(t) = a\cos(\omega t), \qquad y(t) = b\sin(\omega t)
$$

1. Calculate the velocity and acceleration.
2. Is the magnitude of the velocity constant?
3. Where is the velocity maximum?
4. Draw the trajectory and the graphs of $|\vec v(t)|$ and $|\vec a(t)|$.

## Theory


An object whose coordinates are described by $x(t) = a\cos(\omega t)$ and $y(t) = b\sin(\omega t)$ undergoes motion along an elliptical path. The parameters $a$ and $b$ represent the semi-major and semi-minor axes of the ellipse (depending on which is larger), and $\omega$ is the angular frequency parameter. 

This type of motion models a two-dimensional isotropic harmonic oscillator (where restoring forces in $x$ and $y$ are proportional to the displacement). 

The velocity vector $\vec v(t)$ is the first time derivative of the position vector, and the acceleration vector $\vec a(t)$ is the second time derivative. 

## Step-by-Step Solution

### 1. Calculate velocity and acceleration

The position vector is:

$$
\vec r(t) = \bigl( a\cos(\omega t), b\sin(\omega t) \bigr)
$$

The velocity vector is found by taking the derivative of each component with respect to time $t$:

$$
\begin{align}
\vec v(t) &= \left( \frac{d}{dt}(a\cos(\omega t)), \frac{d}{dt}(b\sin(\omega t)) \right) \\
          &= \bigl( -a\omega\sin(\omega t), b\omega\cos(\omega t) \bigr)
\end{align}
$$

The acceleration vector is found by taking the derivative of the velocity components:

$$
\begin{align}
\vec a(t) &= \left( \frac{d}{dt}(-a\omega\sin(\omega t)), \frac{d}{dt}(b\omega\cos(\omega t)) \right) \\
          &= \bigl( -a\omega^2\cos(\omega t), -b\omega^2\sin(\omega t) \bigr)
\end{align}
$$

Notice that the acceleration can be written in terms of the position vector:

$$
\vec a(t) = -\omega^2 \bigl( a\cos(\omega t), b\sin(\omega t) \bigr) = -\omega^2 \vec r(t)
$$

### 2. Is the magnitude of the velocity constant?

To determine if the speed is constant, we calculate the magnitude of the velocity vector:

$$
\begin{align}
|\vec v(t)| &= \sqrt{ (-a\omega\sin(\omega t))^2 + (b\omega\cos(\omega t))^2 } \\
            &= \sqrt{ a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t) } \\
            &= \omega \sqrt{ a^2\sin^2(\omega t) + b^2\cos^2(\omega t) }
\end{align}
$$

Because $\sin^2(\omega t)$ and $\cos^2(\omega t)$ vary with time, the sum $a^2\sin^2(\omega t) + b^2\cos^2(\omega t)$ will also vary with time unless $a = b$. Since $a$ and $b$ are generally different in an ellipse, **the magnitude of the velocity is not constant**. 

*Note: If $a=b$, the path is a circle and the expression simplifies to $\omega \sqrt{a^2(1)} = a\omega$, which is constant.*

### 3. Where is the velocity maximum?

To find the maximum of $|\vec v(t)|$, we must maximize the function inside the square root:

$$
f(t) = a^2\sin^2(\omega t) + b^2\cos^2(\omega t)
$$

Assume $a > b$ (meaning the $x$-axis is the major axis and the $y$-axis is the minor axis). 
Since $\sin^2(\omega t) \le 1$ and $\cos^2(\omega t) \le 1$, the function $f(t)$ is maximized when all the "weight" is on the larger coefficient, $a^2$. This occurs when:

$$
\sin^2(\omega t) = 1 \implies \cos^2(\omega t) = 0
$$

This happens at $\omega t = \frac{\pi}{2}, \frac{3\pi}{2}, \frac{5\pi}{2}, \dots$

Let's check the position of the particle at these times:

$$
\vec r\left(t = \frac{\pi}{2\omega}\right) = \bigl( a(0), b(1) \bigr) = (0, b)
$$

$$
\vec r\left(t = \frac{3\pi}{2\omega}\right) = \bigl( a(0), b(-1) \bigr) = (0, -b)
$$

These points correspond to the ends of the **minor axis** of the ellipse. Conversely, the velocity is at a minimum at the ends of the major axis $(\pm a, 0)$.

If $b > a$, the roles are reversed, and the velocity is maximum at $(\pm a, 0)$, which would then be the minor axis. 

**Conclusion:** The velocity is maximum at the intersections of the trajectory with the minor axis of the ellipse.

### 4. Magnitudes of acceleration for plotting

The magnitude of the acceleration is:

$$
\begin{align}
|\vec a(t)| &= \sqrt{ (-a\omega^2\cos(\omega t))^2 + (-b\omega^2\sin(\omega t))^2 } \\
            &= \omega^2 \sqrt{ a^2\cos^2(\omega t) + b^2\sin^2(\omega t) }
\end{align}
$$

Notice the symmetry: while velocity is maximized when the $\sin$ term is $1$ (at the minor axis), acceleration is maximized when the $\cos$ term is $1$ (at the major axis).

## Final Result

- **Velocity:** $\vec v(t) = (-a\omega\sin(\omega t), b\omega\cos(\omega t))$
- **Acceleration:** $\vec a(t) = -\omega^2 \vec r(t)$
- **Velocity magnitude:** $|\vec v(t)| = \omega \sqrt{ a^2\sin^2(\omega t) + b^2\cos^2(\omega t) }$. It is **not constant**.
- **Maximum velocity location:** At the ends of the **minor axis** of the ellipse.

## Interpretation

In this parameterization of elliptical motion, the angular momentum of the particle relative to the origin is constant ($L = m(x v_y - y v_x) = m a b \omega$). Because angular momentum is conserved, the particle must move faster when it is closer to the origin to sweep out equal areas in equal times (similar to Kepler's Second Law). The closest approaches to the origin occur at the minor axis, which perfectly explains why the speed reaches its maximum at those exact points.