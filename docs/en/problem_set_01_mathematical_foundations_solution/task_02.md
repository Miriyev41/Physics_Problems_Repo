# Task 02 – Parametric trajectory, velocity, and acceleration

## Problem Statement

The parametric equation of a trajectory is given by:

$$
\vec r(t) = \bigl(t^2,\sin t, 5\bigr)
$$

Determine the velocity $\vec v(t)$ and acceleration $\vec a(t)$ vectors. Calculate the magnitude of velocity at $t=1$, the dot product $\vec v \cdot \vec a$, and the cross product $\vec v \times \vec a$.

## Theory

The position vector $\vec r(t)$ describes the location of a particle in space as a function of time. The velocity vector is the first derivative of the position vector with respect to time, representing the instantaneous rate of change of position. 

$$
\vec v(t) = \frac{d\vec r}{dt}
$$

The acceleration vector is the second time derivative of the position vector, or the first time derivative of the velocity vector.

$$
\vec a(t) = \frac{d\vec v}{dt} = \frac{d^2 \vec r}{dt^2}
$$

The dot product of velocity and acceleration provides information about the tangential acceleration (whether the particle is speeding up or slowing down), while the cross product relates to the normal acceleration and the curvature of the trajectory.


## Step-by-Step Solution

Differentiate the position vector component by component to find the velocity.

$$
\vec v(t) = \left( \frac{d}{dt}(t^2), \frac{d}{dt}(\sin t), \frac{d}{dt}(5) \right)
$$

$$
\vec v(t) = (2t, \cos t, 0)
$$

Differentiate the velocity vector to find the acceleration.

$$
\vec a(t) = \left( \frac{d}{dt}(2t), \frac{d}{dt}(\cos t), \frac{d}{dt}(0) \right)
$$

$$
\vec a(t) = (2, -\sin t, 0)
$$

Evaluate the magnitude of the velocity vector at $t = 1$.

$$
\vec v(1) = (2(1), \cos(1), 0)
$$

$$
|\vec v(1)| = \sqrt{2^2 + \cos^2(1) + 0^2}
$$

$$
|\vec v(1)| = \sqrt{4 + \cos^2(1)}
$$

Calculate the dot product of $\vec v(t)$ and $\vec a(t)$.

$$
\begin{align}
\vec v \cdot \vec a &= (2t)(2) + (\cos t)(-\sin t) + (0)(0) \\
                    &= 4t - \sin t \cos t
\end{align}
$$

Calculate the cross product $\vec v \times \vec a$.

$$
\vec v \times \vec a =
\begin{pmatrix}
\hat i & \hat j & \hat k \\
2t & \cos t & 0 \\
2 & -\sin t & 0
\end{pmatrix}
$$

$$
\vec v \times \vec a = \left( 0, 0, (2t)(-\sin t) - (2)(\cos t) \right)
$$

$$
\vec v \times \vec a = (0, 0, -2t\sin t - 2\cos t)
$$

## Final Result

* Velocity: $\vec v(t) = (2t, \cos t, 0)$
* Acceleration: $\vec a(t) = (2, -\sin t, 0)$
* Magnitude of velocity at $t=1$: $|\vec v(1)| = \sqrt{4 + \cos^2(1)}$
* Dot product: $\vec v \cdot \vec a = 4t - \sin t \cos t$
* Cross product: $\vec v \times \vec a = (0, 0, -2t\sin t - 2\cos t)$

## Interpretation

The constant $z$-component in the position vector ensures the entire motion is restricted to the plane $z = 5$. Consequently, the $z$-components of both velocity and acceleration are zero, and their cross product yields a vector strictly pointing along the $z$-axis. To dynamically visualize this planar constraint and the changing vectors, one could construct a web interface using HTML and CSS to structure the layout, alongside a scripting language like Python or JavaScript to handle the continuous rendering of the $(x,y)$ coordinates.