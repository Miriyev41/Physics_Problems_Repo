# Task 02 – Parametric trajectory, velocity, and acceleration

## Problem Statement

The parametric equation of the trajectory is given by:

$$
\vec r(t) = \bigl(t^2,\sin t, 5\bigr)
$$

The required operations are:
1. Determine the velocity $\vec v(t) = \frac{d\vec r}{dt}$.
2. Determine the acceleration $\vec a(t) = \frac{d^2 \vec r}{dt^2}$.
3. Calculate $|\vec v(1)|$.
4. Calculate $\vec v \cdot \vec a$.
5. Calculate $\vec v \times \vec a$.
6. Draw a graph of the trajectory and the velocity and acceleration vectors at selected points.

## Theory

The position vector $\vec r(t)$ describes the location of a particle in three-dimensional space at time $t$. 

Velocity is the first derivative of the position vector with respect to time. It represents the rate of change of position:

$$
\vec v(t) = \frac{d\vec r}{dt} = \left( \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)
$$

Acceleration is the first derivative of velocity, or the second derivative of the position vector, with respect to time. It represents the rate of change of velocity:

$$
\vec a(t) = \frac{d\vec v}{dt} = \frac{d^2\vec r}{dt^2} = \left( \frac{d^2x}{dt^2}, \frac{d^2y}{dt^2}, \frac{d^2z}{dt^2} \right)
$$

The magnitude (length) of the velocity vector at a specific time $t$ is calculated using the Euclidean norm:

$$
|\vec v(t)| = \sqrt{v_x(t)^2 + v_y(t)^2 + v_z(t)^2}
$$

The dot product is a scalar value calculated by multiplying corresponding components and summing them. The cross product is a vector calculated using the determinant of the components.

## Step-by-Step Solution

### 1. Determine the velocity $\vec v(t)$

We are given the position vector:

$$
\vec r(t) = \bigl(t^2, \sin t, 5\bigr)
$$

We compute the derivative of each component with respect to time $t$.

First component (x):

$$
\frac{d}{dt}(t^2) = 2t
$$

Second component (y):

$$
\frac{d}{dt}(\sin t) = \cos t
$$

Third component (z):

$$
\frac{d}{dt}(5) = 0
$$

Therefore, the velocity vector is:

$$
\vec v(t) = \bigl(2t, \cos t, 0\bigr)
$$

### 2. Determine the acceleration $\vec a(t)$

We take the derivative of the velocity vector:

$$
\vec v(t) = \bigl(2t, \cos t, 0\bigr)
$$

Compute the derivative of each component.

First component (x):

$$
\frac{d}{dt}(2t) = 2
$$

Second component (y):

$$
\frac{d}{dt}(\cos t) = -\sin t
$$

Third component (z):

$$
\frac{d}{dt}(0) = 0
$$

Therefore, the acceleration vector is:

$$
\vec a(t) = \bigl(2, -\sin t, 0\bigr)
$$

### 3. Calculate $|\vec v(1)|$

Step 1: Substitute $t = 1$ into the velocity vector.

$$
\vec v(1) = \bigl(2(1), \cos(1), 0\bigr)
$$

$$
\vec v(1) = \bigl(2, \cos 1, 0\bigr)
$$

Step 2: Calculate the magnitude using the formula.

$$
\begin{align}
|\vec v(1)| &= \sqrt{2^2 + (\cos 1)^2 + 0^2} \\
            &= \sqrt{4 + \cos^2 1}
\end{align}
$$

### 4. Calculate the dot product $\vec v \cdot \vec a$

Recall the vectors:

$$
\vec v(t) = \bigl(2t, \cos t, 0\bigr)
$$

$$
\vec a(t) = \bigl(2, -\sin t, 0\bigr)
$$

Multiply the corresponding components and sum them up.

First components:

$$
(2t) \cdot (2) = 4t
$$

Second components:

$$
(\cos t) \cdot (-\sin t) = -\sin t \cos t
$$

Third components:

$$
0 \cdot 0 = 0
$$

Summing these terms:

$$
\begin{align}
\vec v \cdot \vec a &= 4t + (-\sin t \cos t) + 0 \\
                    &= 4t - \sin t \cos t
\end{align}
$$

Note: Using the double angle identity $\sin(2t) = 2\sin t \cos t$, this can also be written as $4t - \frac{1}{2}\sin(2t)$.

### 5. Calculate the cross product $\vec v \times \vec a$

Set up the components for the cross product formula:

$$
\vec v \times \vec a =
\begin{pmatrix}
v_y a_z - v_z a_y \\
v_z a_x - v_x a_z \\
v_x a_y - v_y a_x
\end{pmatrix}
$$

Substitute the components of $\vec v = (2t, \cos t, 0)$ and $\vec a = (2, -\sin t, 0)$.

First component:

$$
(\cos t)(0) - (0)(-\sin t) = 0 - 0 = 0
$$

Second component:

$$
(0)(2) - (2t)(0) = 0 - 0 = 0
$$

Third component:

$$
(2t)(-\sin t) - (\cos t)(2) = -2t \sin t - 2\cos t
$$

Therefore, the cross product vector is:

$$
\vec v \times \vec a = \bigl(0, 0, -2t \sin t - 2\cos t\bigr)
$$

## Final Result

* Velocity: $\vec v(t) = (2t, \cos t, 0)$
* Acceleration: $\vec a(t) = (2, -\sin t, 0)$
* Magnitude of velocity at $t=1$: $|\vec v(1)| = \sqrt{4 + \cos^2 1}$
* Dot product: $\vec v \cdot \vec a = 4t - \sin t \cos t$
* Cross product: $\vec v \times \vec a = (0, 0, -2t \sin t - 2\cos t)$

## Interpretation



Because the $z$-component of the position vector is constant ($z=5$), the velocity and acceleration in the $z$-direction are entirely zero. This indicates that the motion is strictly confined to a two-dimensional plane that is parallel to the $xy$-plane, specifically at height $z=5$. 

Consequently, the velocity and acceleration vectors only have $x$ and $y$ components. When computing the cross product $\vec v \times \vec a$, the result lies entirely along the $z$-axis (the third component), which is geometrically consistent because the cross product of two vectors in the $xy$-plane must be perpendicular to that plane.