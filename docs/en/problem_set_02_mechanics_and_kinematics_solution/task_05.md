# Task 05 – Elliptical motion (purely kinematic)

## Problem Statement

The path equation of a particle is given in parametric form:

$$
x(t) = a\cos(\omega t), \qquad y(t) = b\sin(\omega t)
$$

The required operations are:
1. Calculate the velocity vector $\vec v(t)$ and the acceleration vector $\vec a(t)$.
2. Determine if the magnitude of the velocity is constant.
3. Identify the positions where the velocity reaches its maximum magnitude.
4. Draw the trajectory and the graphs of $|\vec v(t)|$ and $|\vec a(t)|$.

## Theory

Elliptical motion is a generalization of circular motion where the radii along the axes (semi-axes $a$ and $b$) are not necessarily equal. 

The velocity vector is the first derivative of the position vector $\vec r(t)$ with respect to time:

$$
\vec v(t) = \frac{d\vec r}{dt} = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

The acceleration vector is the second derivative of the position vector:

$$
\vec a(t) = \frac{d^2\vec r}{dt^2} = \left( \frac{dv_x}{dt}, \frac{dv_y}{dt} \right)
$$

The magnitude of the velocity (speed) is given by:

$$
|\vec v(t)| = \sqrt{v_x^2 + v_y^2}
$$

A vector quantity has a constant magnitude only if its Euclidean norm is independent of the parameter $t$. In non-circular elliptical motion ($a \neq b$), the speed varies as the particle moves along the perimeter.

## Step-by-Step Solution

### 1. Calculate velocity and acceleration

**Step 1: Compute velocity $\vec v(t)$**

Differentiate the components of position $x(t) = a\cos(\omega t)$ and $y(t) = b\sin(\omega t)$:

$$
v_x(t) = \frac{d}{dt}(a\cos(\omega t)) = -a\omega\sin(\omega t)
$$

$$
v_y(t) = \frac{d}{dt}(b\sin(\omega t)) = b\omega\cos(\omega t)
$$

The velocity vector is:

$$
\vec v(t) = (-a\omega\sin(\omega t), b\omega\cos(\omega t))
$$

**Step 2: Compute acceleration $\vec a(t)$**

Differentiate the velocity components:

$$
a_x(t) = \frac{d}{dt}(-a\omega\sin(\omega t)) = -a\omega^2\cos(\omega t)
$$

$$
a_y(t) = \frac{d}{dt}(b\omega\cos(\omega t)) = -b\omega^2\sin(\omega t)
$$

The acceleration vector is:

$$
\vec a(t) = (-a\omega^2\cos(\omega t), -b\omega^2\sin(\omega t))
$$

Note that $\vec a(t) = -\omega^2 \vec r(t)$, which means the acceleration always points toward the origin.

### 2. Is the magnitude of the velocity constant?

Calculate the magnitude $|\vec v(t)|$:

$$
\begin{align}
|\vec v(t)| &= \sqrt{(-a\omega\sin(\omega t))^2 + (b\omega\cos(\omega t))^2} \\
            &= \sqrt{a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t)} \\
            &= \omega\sqrt{a^2\sin^2(\omega t) + b^2\cos^2(\omega t)}
\end{align}
$$

Using the identity $\cos^2(\omega t) = 1 - \sin^2(\omega t)$:

$$
\begin{align}
|\vec v(t)| &= \omega\sqrt{a^2\sin^2(\omega t) + b^2(1 - \sin^2(\omega t))} \\
            &= \omega\sqrt{b^2 + (a^2 - b^2)\sin^2(\omega t)}
\end{align}
$$

The magnitude depends on $\sin^2(\omega t)$. Therefore, unless $a = b$ (the circular case), the magnitude of the velocity is **not constant**.

### 3. Where is the velocity maximum?

Assume without loss of generality that $a > b$ (the major axis is along $x$). 

The expression $|\vec v(t)| = \omega\sqrt{b^2 + (a^2 - b^2)\sin^2(\omega t)}$ is maximized when $\sin^2(\omega t)$ is at its maximum value of $1$.

This occurs when:

$$
\omega t = \frac{\pi}{2}, \frac{3\pi}{2}, \dots
$$

Substituting these into the position equations:
- If $\omega t = \pi/2$, then $x = a\cos(\pi/2) = 0$ and $y = b\sin(\pi/2) = b$.
- If $\omega t = 3\pi/2$, then $x = a\cos(3\pi/2) = 0$ and $y = b\sin(3\pi/2) = -b$.

The velocity is maximum at the ends of the **minor axis** (points $(0, \pm b)$).

*Note: Conversely, the velocity is minimum when $\sin^2(\omega t) = 0$, which occurs at the ends of the major axis $( \pm a, 0)$.*

## Final Result

* Velocity: $\vec v(t) = (-a\omega\sin(\omega t), b\omega\cos(\omega t))$
* Acceleration: $\vec a(t) = (-a\omega^2\cos(\omega t), -b\omega^2\sin(\omega t))$
* Velocity magnitude: $|\vec v(t)| = \omega\sqrt{a^2\sin^2(\omega t) + b^2\cos^2(\omega t)}$
* Velocity is not constant if $a \neq b$.
* Maximum velocity occurs at the vertices of the minor axis: $(0, \pm b)$.

## Interpretation



In elliptical motion, the particle must cover a larger "arc" near the ends of the major axis and a sharper "turn" near the ends of the minor axis within the same time interval $\Delta t$ defined by the constant angular parameter $\omega$. Interestingly, the speed is highest when the particle is closest to the center (at the minor axis) and lowest when it is furthest away (at the major axis). This kinematic behavior is a direct result of the parametric definition where the angular rate $d\phi/dt$ is constant, but the radius $r(t)$ varies.