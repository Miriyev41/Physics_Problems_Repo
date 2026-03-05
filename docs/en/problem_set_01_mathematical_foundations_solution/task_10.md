# Task 10 – Angular momentum in circular motion

## Problem Statement

Consider circular motion in the $xy$ plane:

$$
\vec r(t) = \bigl(R\cos(\omega t), R\sin(\omega t), 0\bigr)
$$

Determine the velocity $\vec v(t)$ and calculate the angular momentum $\vec L(t)$ with respect to the origin. Show that the magnitude $|\vec L|$ is constant and that the vector $\vec L$ is perpendicular to the plane of motion. Interpret the direction of $\vec L$ using the right-hand rule. Finally, introduce a constant centripetal force, calculate the resulting torque $\vec \tau$, and verify the relationship $\vec \tau = \frac{d\vec L}{dt}$.

## Theory

Angular momentum is a vector quantity that represents the rotational analogue of linear momentum. For a single particle, the angular momentum $\vec L$ with respect to a chosen origin is defined as the cross product of the position vector $\vec r$ and the linear momentum $\vec p = m\vec v$.

$$
\vec L = \vec r \times \vec p = m(\vec r \times \vec v)
$$

The direction of the angular momentum vector is determined by the right-hand rule and is always perpendicular to the plane spanned by the position and velocity vectors. 



[Image of angular momentum right hand rule]


Torque $\vec \tau$ is the rotational analogue of force, defined as the cross product of the position vector and the applied force. The fundamental rotational equation of motion relates the net torque on a system to the time rate of change of its angular momentum.

$$
\vec \tau = \vec r \times \vec F = \frac{d\vec L}{dt}
$$

## Step-by-Step Solution

First, determine the velocity vector by taking the time derivative of the position vector.

$$
\vec v(t) = \frac{d}{dt} \bigl(R\cos(\omega t), R\sin(\omega t), 0\bigr)
$$

$$
\vec v(t) = \bigl(-R\omega\sin(\omega t), R\omega\cos(\omega t), 0\bigr)
$$

Next, calculate the cross product $\vec r(t) \times \vec v(t)$ to find the angular momentum.

$$
\vec r \times \vec v = 
\begin{pmatrix}
\hat i & \hat j & \hat k \\
R\cos(\omega t) & R\sin(\omega t) & 0 \\
-R\omega\sin(\omega t) & R\omega\cos(\omega t) & 0
\end{pmatrix}
$$

Expand the determinant.

$$
\vec r \times \vec v = \left( 0, 0, (R\cos(\omega t))(R\omega\cos(\omega t)) - (R\sin(\omega t))(-R\omega\sin(\omega t)) \right)
$$

$$
\vec r \times \vec v = \left( 0, 0, R^2\omega\cos^2(\omega t) + R^2\omega\sin^2(\omega t) \right)
$$

Factor out $R^2\omega$ and apply the Pythagorean trigonometric identity.

$$
\vec r \times \vec v = \bigl( 0, 0, R^2\omega(\cos^2(\omega t) + \sin^2(\omega t)) \bigr)
$$

$$
\vec r \times \vec v = (0, 0, R^2\omega)
$$

Multiply by the mass $m$ to find the angular momentum vector $\vec L(t)$.

$$
\vec L(t) = (0, 0, mR^2\omega)
$$

Calculate the magnitude of the angular momentum vector.

$$
|\vec L| = \sqrt{0^2 + 0^2 + (mR^2\omega)^2}
$$

$$
|\vec L| = mR^2\omega
$$

Because $m$, $R$, and $\omega$ are all constants, the magnitude $|\vec L|$ is constant. Since the $x$ and $y$ components are zero, the vector lies entirely along the $z$-axis, which is strictly perpendicular to the $xy$ plane of motion.

Now, introduce a centripetal force. A centripetal force is always directed toward the center of the circular path, meaning it is anti-parallel to the position vector $\vec r$. Let its magnitude be $F_c = m\omega^2 R$. The force vector can be expressed in terms of the position vector.

$$
\vec F = -m\omega^2 \vec r
$$

Calculate the torque $\vec \tau$.

$$
\vec \tau = \vec r \times \vec F
$$

$$
\vec \tau = \vec r \times (-m\omega^2 \vec r)
$$

Since the cross product of any vector with itself (or a scalar multiple of itself) is the zero vector, this evaluates to zero.

$$
\vec \tau = -m\omega^2 (\vec r \times \vec r)
$$

$$
\vec \tau = (0, 0, 0) = \vec 0
$$

Verify the relationship between torque and the time derivative of angular momentum. Evaluate $\frac{d\vec L}{dt}$.

$$
\frac{d\vec L}{dt} = \frac{d}{dt} (0, 0, mR^2\omega)
$$

Because the vector contains only constant values, its time derivative is the zero vector.

$$
\frac{d\vec L}{dt} = (0, 0, 0) = \vec 0
$$

Thus, $\vec \tau = \frac{d\vec L}{dt}$ is confirmed.

## Final Result

* Velocity: $\vec v(t) = \bigl(-R\omega\sin(\omega t), R\omega\cos(\omega t), 0\bigr)$
* Angular Momentum: $\vec L(t) = (0, 0, mR^2\omega)$
* Magnitude: $|\vec L| = mR^2\omega$ (constant)
* Torque from centripetal force: $\vec \tau = \vec 0$
* Verification: $\vec \tau = \frac{d\vec L}{dt} = \vec 0$

## Interpretation

The angular momentum vector for this trajectory always points along the $z$-axis. According to the right-hand rule, if the fingers of the right hand curl in the direction of rotation (from the $x$-axis toward the $y$-axis for positive $\omega$), the thumb points in the positive $z$-direction, indicating the orientation of $\vec L$. The magnitude $mR^2\omega$ represents the product of the moment of inertia for a point mass ($I = mR^2$) and its angular velocity ($\omega$). 

The centripetal force maintains the circular trajectory by continuously changing the direction of the velocity vector, but because its line of action passes exactly through the origin, it has a lever arm of zero. Consequently, it produces no torque. Without a net torque, the system's angular momentum is strictly conserved in both magnitude and direction, satisfying Newton's laws for rotational dynamics.