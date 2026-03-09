# Task 04 – Circular motion

## Problem Statement

A body moves in a circle of radius $R$ with a constant angular velocity $\omega$.

The required operations are:
1. Determine the position vector $\vec r(t)$, the velocity vector $\vec v(t)$, and the acceleration vector $\vec a(t)$.
2. Determine the magnitudes $|\vec r(t)|$, $|\vec v(t)|$, and $|\vec a(t)|$.
3. Show that the acceleration is centripetal (pointing toward the center).
4. Visualize the vectors $\vec r$, $\vec v$, and $\vec a$.

## Theory

Circular motion in a plane can be described using polar coordinates or Cartesian coordinates with trigonometric functions. For a circle of radius $R$ in the $xy$-plane, the position is given by:

$$
x(t) = R\cos(\phi(t)), \qquad y(t) = R\sin(\phi(t))
$$

For constant angular velocity $\omega$, the angle $\phi$ changes linearly with time: $\phi(t) = \omega t$ (assuming $\phi(0) = 0$).

The velocity is the rate of change of position, and acceleration is the rate of change of velocity. In uniform circular motion, while the speed (magnitude of velocity) remains constant, the velocity vector is constantly changing direction, which necessitates a non-zero acceleration.

## Step-by-Step Solution

### 1. Determine the vectors $\vec r(t)$, $\vec v(t)$, and $\vec a(t)$

**Position Vector:**

$$
\vec r(t) = 
\begin{pmatrix}
R\cos(\omega t) \\
R\sin(\omega t)
\end{pmatrix}
$$

**Velocity Vector:**
Differentiate each component of the position vector with respect to $t$:

$$
v_x = \frac{d}{dt}(R\cos(\omega t)) = -R\omega\sin(\omega t)
$$

$$
v_y = \frac{d}{dt}(R\sin(\omega t)) = R\omega\cos(\omega t)
$$

$$
\vec v(t) = 
\begin{pmatrix}
-R\omega\sin(\omega t) \\
R\omega\cos(\omega t)
\end{pmatrix}
$$

**Acceleration Vector:**
Differentiate each component of the velocity vector with respect to $t$:

$$
a_x = \frac{d}{dt}(-R\omega\sin(\omega t)) = -R\omega^2\cos(\omega t)
$$

$$
a_y = \frac{d}{dt}(R\omega\cos(\omega t)) = -R\omega^2\sin(\omega t)
$$

$$
\vec a(t) = 
\begin{pmatrix}
-R\omega^2\cos(\omega t) \\
-R\omega^2\sin(\omega t)
\end{pmatrix}
$$

### 2. Determine the magnitudes

**Magnitude of Position:**

$$
|\vec r(t)| = \sqrt{(R\cos\omega t)^2 + (R\sin\omega t)^2} = \sqrt{R^2(\cos^2\omega t + \sin^2\omega t)} = R
$$

**Magnitude of Velocity (Speed):**

$$
|\vec v(t)| = \sqrt{(-R\omega\sin\omega t)^2 + (R\omega\cos\omega t)^2} = \sqrt{R^2\omega^2(\sin^2\omega t + \cos^2\omega t)} = R\omega
$$

**Magnitude of Acceleration:**

$$
|\vec a(t)| = \sqrt{(-R\omega^2\cos\omega t)^2 + (-R\omega^2\sin\omega t)^2} = \sqrt{R^2\omega^4(\cos^2\omega t + \sin^2\omega t)} = R\omega^2
$$

### 3. Show that the acceleration is centripetal

We can express the acceleration vector $\vec a(t)$ in terms of the position vector $\vec r(t)$:

$$
\vec a(t) = 
\begin{pmatrix}
-R\omega^2\cos(\omega t) \\
-R\omega^2\sin(\omega t)
\end{pmatrix}
= -\omega^2 
\begin{pmatrix}
R\cos(\omega t) \\
R\sin(\omega t)
\end{pmatrix}
$$

$$
\vec a(t) = -\omega^2 \vec r(t)
$$

Since $\omega^2$ is a positive scalar, the acceleration vector $\vec a(t)$ is directly proportional to the position vector $\vec r(t)$ but points in the opposite direction (toward the origin). In circular motion, the origin is the center of the circle; therefore, the acceleration is centripetal.

## Final Result

* Position: $\vec r(t) = (R\cos\omega t, R\sin\omega t)$
* Velocity: $\vec v(t) = (-R\omega\sin\omega t, R\omega\cos\omega t)$
* Acceleration: $\vec a(t) = (-R\omega^2\cos\omega t, -R\omega^2\sin\omega t) = -\omega^2 \vec r(t)$
* Magnitudes: $|\vec r| = R$, $|\vec v| = R\omega$, $|\vec a| = R\omega^2$

## Interpretation



In uniform circular motion, the three vectors $\vec r$, $\vec v$, and $\vec a$ maintain a rigid geometric relationship. The velocity $\vec v$ is always tangent to the circle and perpendicular to the position vector $\vec r$. The acceleration $\vec a$ is always perpendicular to the velocity and points directly toward the center. This centripetal acceleration does not change the speed of the object; its sole physical function is to continuously change the direction of the velocity vector, forcing the object to maintain its curved path rather than flying off in a straight line.