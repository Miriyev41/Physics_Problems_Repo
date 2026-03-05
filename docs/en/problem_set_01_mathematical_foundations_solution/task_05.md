# Task 05 – Trajectory curvature and normal acceleration

## Problem Statement

For an ellipse parameterized by $x = a\cos t, y = b\sin t$:
Determine velocity $\vec v(t)$, acceleration $\vec a(t)$, and the unit tangent vector $\hat T(t)$. Decompose the acceleration into tangential and normal components and determine the magnitude of the normal acceleration $a_n(t)$. Find the radius of curvature $R$ at $t=0$, compare it with a circle, and provide physical interpretations.

## Theory

Acceleration describes both the change in the speed of an object and the change in its direction of motion. It can be decomposed into two orthogonal vectors:

$$
\vec a(t) = \vec a_t(t) + \vec a_n(t)
$$

The tangential acceleration $\vec a_t$ acts along the velocity vector and changes only the magnitude of velocity (speed). The normal acceleration $\vec a_n$ acts perpendicularly to the velocity vector and is exclusively responsible for changing the direction of motion. 

The relationship between normal acceleration, speed $v$, and the local radius of curvature $R$ is given by:

$$
a_n = \frac{v^2}{R}
$$



## Step-by-Step Solution

Determine the velocity and acceleration vectors.

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

Calculate the magnitude of the velocity vector.

$$
|\vec v(t)| = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

Determine the unit tangent vector by normalizing the velocity.

$$
\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)
$$

To find the normal acceleration $a_n$, one can use the 2D cross product magnitude $|\vec v \times \vec a|$ divided by the speed $|\vec v|$.

$$
|\vec v \times \vec a| = |v_x a_y - v_y a_x|
$$

$$
|\vec v \times \vec a| = |(-a\sin t)(-b\sin t) - (b\cos t)(-a\cos t)|
$$

$$
|\vec v \times \vec a| = |ab\sin^2 t + ab\cos^2 t|
$$

$$
|\vec v \times \vec a| = ab
$$

Calculate the normal acceleration magnitude.

$$
a_n(t) = \frac{|\vec v \times \vec a|}{|\vec v(t)|}
$$

$$
a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}
$$

Calculate the radius of curvature using $R = \frac{v^2}{a_n}$.

$$
R(t) = \frac{a^2\sin^2 t + b^2\cos^2 t}{\frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}}
$$

$$
R(t) = \frac{(a^2\sin^2 t + b^2\cos^2 t)^{3/2}}{ab}
$$

Evaluate the radius of curvature at $t = 0$.

$$
R(0) = \frac{(a^2(0) + b^2(1))^{3/2}}{ab}
$$

$$
R(0) = \frac{(b^2)^{3/2}}{ab}
$$

$$
R(0) = \frac{b^3}{ab}
$$

$$
R(0) = \frac{b^2}{a}
$$

Compare with a circle where $a = b$.

$$
R_{\text{circle}}(0) = \frac{a^2}{a}
$$

$$
R_{\text{circle}}(0) = a
$$

## Final Result

* Velocity: $\vec v(t) = (-a\sin t, b\cos t)$
* Acceleration: $\vec a(t) = (-a\cos t, -b\sin t)$
* Unit Tangent: $\hat T(t) = \frac{(-a\sin t, b\cos t)}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}$
* Normal Acceleration: $a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}$
* Radius of Curvature at $t=0$: $R(0) = \frac{b^2}{a}$
* For a circle ($a=b$), the radius of curvature is constantly equal to $a$.

## Interpretation

* **Curvature vs. Acceleration:** A greater trajectory curvature implies a smaller radius of curvature $R$. For a constant velocity $v$, a smaller $R$ necessitates a strictly greater normal acceleration.
* **Maximum Curvature Point:** Assuming $a > b$ (major axis along $x$), the point $t=0$ corresponds to $(a, 0)$, the end of the major semi-axis. Here, the radius of curvature $R = \frac{b^2}{a}$ reaches its minimum, meaning the trajectory is most "curved" at the vertices along the major axis.
* **Role of Normal Acceleration:** Normal acceleration is established by the component of force perpendicular to the velocity vector. Because work is the dot product of force and displacement, a perpendicular force does zero work, meaning kinetic energy (and thus speed) remains constant. Consequently, this force acts solely to rotate the velocity vector, changing the direction of motion.