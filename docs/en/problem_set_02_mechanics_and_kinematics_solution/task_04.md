# Task 04 – Circular motion

## Problem Statement

A body moves in a circle of radius $R$ with angular velocity $\omega$. 

1. Determine $\vec r(t)$, $\vec v(t)$, $\vec a(t)$.
2. Determine $|\vec r(t)|$, $|\vec v(t)|$, $|\vec a(t)|$.
3. Show that the acceleration is centripetal.
4. Visualize the vectors $\vec r$, $\vec v$, $\vec a$.

## Theory



Uniform circular motion occurs when an object travels along a circular path with a constant angular velocity $\omega$. The position vector $\vec r(t)$ continuously changes direction but maintains a constant magnitude equal to the radius $R$. 

In kinematics, velocity is the first time derivative of position, and acceleration is the second time derivative. For an object to remain in a circular path, it must experience a continuous change in the direction of its velocity. This change in direction is caused by an acceleration directed exactly towards the center of the circle, known as **centripetal acceleration**. Mathematically, an acceleration is centripetal if the acceleration vector is antiparallel (points in the exact opposite direction) to the position vector when the origin is placed at the center of the circle.

## Step-by-Step Solution

### 1. Vector functions $\vec r(t)$, $\vec v(t)$, $\vec a(t)$

Assuming the center of the circle is at the origin $(0,0)$ and the motion begins on the positive $x$-axis, the position vector as a function of time is given by basic trigonometry:

$$
\vec r(t) = \bigl( R\cos(\omega t), R\sin(\omega t) \bigr)
$$

The velocity vector is the time derivative of the position vector:

$$
\begin{align}
\vec v(t) &= \frac{d\vec r}{dt} \\
          &= \left( \frac{d}{dt}(R\cos(\omega t)), \frac{d}{dt}(R\sin(\omega t)) \right) \\
          &= \bigl( -R\omega\sin(\omega t), R\omega\cos(\omega t) \bigr)
\end{align}
$$

The acceleration vector is the time derivative of the velocity vector:

$$
\begin{align}
\vec a(t) &= \frac{d\vec v}{dt} \\
          &= \left( \frac{d}{dt}(-R\omega\sin(\omega t)), \frac{d}{dt}(R\omega\cos(\omega t)) \right) \\
          &= \bigl( -R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t) \bigr)
\end{align}
$$

### 2. Magnitudes of the vectors

The magnitude of the position vector is the distance from the origin:

$$
\begin{align}
|\vec r(t)| &= \sqrt{ (R\cos(\omega t))^2 + (R\sin(\omega t))^2 } \\
            &= \sqrt{ R^2 (\cos^2(\omega t) + \sin^2(\omega t)) } \\
            &= \sqrt{ R^2(1) } \\
            &= R
\end{align}
$$

The magnitude of the velocity vector (the linear speed) is:

$$
\begin{align}
|\vec v(t)| &= \sqrt{ (-R\omega\sin(\omega t))^2 + (R\omega\cos(\omega t))^2 } \\
            &= \sqrt{ R^2\omega^2\sin^2(\omega t) + R^2\omega^2\cos^2(\omega t) } \\
            &= \sqrt{ R^2\omega^2 (\sin^2(\omega t) + \cos^2(\omega t)) } \\
            &= R\omega
\end{align}
$$

The magnitude of the acceleration vector is:

$$
\begin{align}
|\vec a(t)| &= \sqrt{ (-R\omega^2\cos(\omega t))^2 + (-R\omega^2\sin(\omega t))^2 } \\
            &= \sqrt{ R^2\omega^4\cos^2(\omega t) + R^2\omega^4\sin^2(\omega t) } \\
            &= \sqrt{ R^2\omega^4 (\cos^2(\omega t) + \sin^2(\omega t)) } \\
            &= R\omega^2
\end{align}
$$

### 3. Show that the acceleration is centripetal

To show that the acceleration is centripetal, we must demonstrate that it points directly toward the center of the circle (the origin). Let's factor out $-\omega^2$ from the components of the acceleration vector:

$$
\begin{align}
\vec a(t) &= \bigl( -R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t) \bigr) \\
          &= -\omega^2 \bigl( R\cos(\omega t), R\sin(\omega t) \bigr)
\end{align}
$$

We recognize the term inside the parentheses as the position vector $\vec r(t)$:

$$
\vec a(t) = -\omega^2 \vec r(t)
$$

Since $\omega^2$ is a strictly positive scalar, multiplying $\vec r(t)$ by $-\omega^2$ produces a vector that is perfectly aligned with $\vec r(t)$ but points in the opposite direction. Since $\vec r(t)$ points outward from the origin to the particle, $\vec a(t)$ must point inward from the particle to the origin. Therefore, the acceleration is purely centripetal.

## Final Result

- **Position:** $\vec r(t) = (R\cos(\omega t), R\sin(\omega t))$
- **Velocity:** $\vec v(t) = (-R\omega\sin(\omega t), R\omega\cos(\omega t))$
- **Acceleration:** $\vec a(t) = (-R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t))$
- **Magnitudes:** $|\vec r| = R$, $|\vec v| = R\omega$, $|\vec a| = R\omega^2$
- **Centripetal proof:** $\vec a(t) = -\omega^2 \vec r(t)$, showing it points opposite to the radius vector towards the center.

## Interpretation

In uniform circular motion, neither the position, nor the velocity, nor the acceleration is zero, yet their magnitudes are all strictly constant. The velocity vector is always perpendicular to the position vector (which can be proven by showing their dot product is zero: $\vec r \cdot \vec v = 0$), meaning the particle moves tangentially. The acceleration vector ensures the velocity vector rotates at a constant rate $\omega$ without changing the particle's speed.