# Task 02 – Parametric Trajectory, Velocity, and Acceleration

## Problem Statement

The parametric equation of a point's trajectory in space is given by:

$$
\vec r(t) = \bigl(t^2, \sin t, 5\bigr)
$$

Determine the following:
1. The velocity vector $\vec v(t) = \frac{d\vec r}{dt}$.
2. The acceleration vector $\vec a(t) = \frac{d^2 \vec r}{dt^2}$.
3. The magnitude of the velocity at $t=1$, $|\vec v(1)|$.
4. The dot product $\vec v \cdot \vec a$.
5. The cross product $\vec v \times \vec a$.

## Theory

In kinematics, the position of a particle as a function of time is described by the position vector $\vec r(t)$. The first derivative of the position vector with respect to time defines the velocity vector $\vec v(t)$, which represents the rate of change of position and is always tangent to the trajectory.

The second derivative of the position vector with respect to time defines the acceleration vector $\vec a(t)$, which represents the rate of change of velocity.

The dot product $\vec v \cdot \vec a$ relates to the rate of change of the particle's speed. If the dot product is positive, the particle is speeding up; if negative, it is slowing down. The cross product $\vec v \times \vec a$ provides a vector normal to the plane of motion formed by velocity and acceleration, and its magnitude relates to the curvature of the trajectory.

## Step-by-Step Solution

### 1. Velocity vector

The velocity is obtained by differentiating each component of the position vector $\vec r(t)$ with respect to time $t$:

$$
\vec v(t) = \left( \frac{d}{dt}(t^2), \frac{d}{dt}(\sin t), \frac{d}{dt}(5) \right)
$$

Applying elementary differentiation rules:

$$
\vec v(t) = \bigl(2t, \cos t, 0\bigr)
$$

### 2. Acceleration vector

The acceleration is obtained by differentiating each component of the velocity vector $\vec v(t)$ with respect to time $t$:

$$
\vec a(t) = \left( \frac{d}{dt}(2t), \frac{d}{dt}(\cos t), \frac{d}{dt}(0) \right)
$$

Evaluating the derivatives:

$$
\vec a(t) = \bigl(2, -\sin t, 0\bigr)
$$

### 3. Magnitude of velocity at $t = 1$

First, substitute $t = 1$ into the velocity vector:

$$
\vec v(1) = \bigl(2(1), \cos(1), 0\bigr) = \bigl(2, \cos 1, 0\bigr)
$$

The magnitude is the Euclidean norm of this vector:

$$
\begin{align}
|\vec v(1)| &= \sqrt{2^2 + (\cos 1)^2 + 0^2} \\
            &= \sqrt{4 + \cos^2 1}
\end{align}
$$

### 4. Dot product $\vec v \cdot \vec a$

To calculate the dot product of $\vec v(t)$ and $\vec a(t)$, multiply corresponding components and sum them:

$$
\vec v \cdot \vec a = (2t)(2) + (\cos t)(-\sin t) + (0)(0)
$$

Simplifying the expression:

$$
\vec v \cdot \vec a = 4t - \sin t \cos t
$$

Using the double-angle identity for sine, $\sin(2t) = 2\sin t \cos t$, this can optionally be written as:

$$
\vec v \cdot \vec a = 4t - \frac{1}{2}\sin(2t)
$$

### 5. Cross product $\vec v \times \vec a$

The cross product is computed using the formal determinant method:

$$
\vec v \times \vec a =
\begin{pmatrix}
v_y a_z - v_z a_y \\
v_z a_x - v_x a_z \\
v_x a_y - v_y a_x
\end{pmatrix}
$$

Substituting the components $v = (2t, \cos t, 0)$ and $a = (2, -\sin t, 0)$:

$$
\begin{align}
\vec v \times \vec a &=
\begin{pmatrix}
(\cos t)(0) - (0)(-\sin t) \\
(0)(2) - (2t)(0) \\
(2t)(-\sin t) - (\cos t)(2)
\end{pmatrix} \\
&=
\begin{pmatrix}
0 \\
0 \\
-2t\sin t - 2\cos t
\end{pmatrix}
\end{align}
$$

This can be written in row vector format as $(0, 0, -2t\sin t - 2\cos t)$.

## Final Result

- Velocity: $\vec v(t) = (2t, \cos t, 0)$
- Acceleration: $\vec a(t) = (2, -\sin t, 0)$
- Speed at $t=1$: $|\vec v(1)| = \sqrt{4 + \cos^2 1}$
- Dot product: $\vec v \cdot \vec a = 4t - \sin t \cos t$
- Cross product: $\vec v \times \vec a = (0, 0, -2t\sin t - 2\cos t)$

## Interpretation

The $z$-component of the position is constant ($z=5$), indicating that the motion is restricted to a horizontal plane at height $5$. As a result, both the velocity and acceleration have a zero $z$-component, maintaining the particle entirely within this plane.

Because the motion is planar, the cross product $\vec v \times \vec a$ has only a $z$-component. This aligns with the geometric property of the cross product, which always yields a vector perpendicular to both operand vectors. Since both $\vec v$ and $\vec a$ lie in planes parallel to the $xy$-plane, their cross product must point entirely along the $z$-axis.