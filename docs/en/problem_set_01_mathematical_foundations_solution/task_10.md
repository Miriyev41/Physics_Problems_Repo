# Task 10 – Angular momentum in circular motion

## Problem Statement

Consider circular motion in the $xy$ plane with the following position vector:

$$
\vec r(t) = \bigl(R\cos(\omega t), R\sin(\omega t), 0\bigr)
$$

The required operations are:
1. Determine the velocity vector $\vec v(t) = \dot{\vec r}(t)$.
2. Calculate the angular momentum with respect to the origin: $\vec L(t) = m\vec r(t) \times \vec v(t)$.
3. Show that the magnitude $|\vec L| = mR^2\omega$ is constant.
4. Show that the vector $\vec L$ is perpendicular to the plane of motion.

## Theory

Angular momentum $\vec L$ is a vector quantity that represents the product of a body's rotational inertia and rotational velocity about a particular axis. For a point mass $m$ with position vector $\vec r$ and velocity $\vec v$, it is defined by the cross product:

$$
\vec L = m(\vec r \times \vec v)
$$

The velocity vector $\vec v(t)$ is the time derivative of the position vector $\vec r(t)$:

$$
\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)
$$

The cross product of two vectors $\vec A = (A_x, A_y, A_z)$ and $\vec B = (B_x, B_y, B_z)$ is calculated as:

$$
\vec A \times \vec B = 
\begin{pmatrix}
A_y B_z - A_z B_y \\
A_z B_x - A_x B_z \\
A_x B_y - A_y B_x
\end{pmatrix}
$$

The magnitude of the angular momentum vector is:

$$
|\vec L| = \sqrt{L_x^2 + L_y^2 + L_z^2}
$$

A vector is perpendicular to the $xy$ plane if its $x$ and $y$ components are zero, leaving only a $z$ component.

## Step-by-Step Solution

### 1. Determine the velocity vector $\vec v(t)$

We differentiate each component of $\vec r(t) = \bigl(R\cos(\omega t), R\sin(\omega t), 0\bigr)$ with respect to $t$. Use the chain rule: $\frac{d}{dt}\cos(\omega t) = -\omega\sin(\omega t)$ and $\frac{d}{dt}\sin(\omega t) = \omega\cos(\omega t)$.

First component ($v_x$):

$$
v_x(t) = \frac{d}{dt}(R\cos(\omega t)) = -R\omega\sin(\omega t)
$$

Second component ($v_y$):

$$
v_y(t) = \frac{d}{dt}(R\sin(\omega t)) = R\omega\cos(\omega t)
$$

Third component ($v_z$):

$$
v_z(t) = \frac{d}{dt}(0) = 0
$$

Therefore, the velocity vector is:

$$
\vec v(t) = \bigl(-R\omega\sin(\omega t), R\omega\cos(\omega t), 0\bigr)
$$

### 2. Calculate the angular momentum $\vec L(t)$

Set up the cross product $\vec L = m(\vec r \times \vec v)$. Let's first compute $\vec r \times \vec v$:

$$
\vec r \times \vec v = 
\begin{pmatrix}
R\cos(\omega t) \\
R\sin(\omega t) \\
0
\end{pmatrix}
\times
\begin{pmatrix}
-R\omega\sin(\omega t) \\
R\omega\cos(\omega t) \\
0
\end{pmatrix}
$$

First component ($L_x$):

$$
(R\sin(\omega t) \cdot 0) - (0 \cdot R\omega\cos(\omega t)) = 0 - 0 = 0
$$

Second component ($L_y$):

$$
(0 \cdot -R\omega\sin(\omega t)) - (R\cos(\omega t) \cdot 0) = 0 - 0 = 0
$$

Third component ($L_z$):

$$
\begin{align}
L_z &= (R\cos(\omega t))(R\omega\cos(\omega t)) - (R\sin(\omega t))(-R\omega\sin(\omega t)) \\
    &= R^2\omega\cos^2(\omega t) - (-R^2\omega\sin^2(\omega t)) \\
    &= R^2\omega\cos^2(\omega t) + R^2\omega\sin^2(\omega t)
\end{align}
$$

Factor out $R^2\omega$:

$$
\begin{align}
L_z &= R^2\omega (\cos^2(\omega t) + \sin^2(\omega t)) \\
    &= R^2\omega (1) \\
    &= R^2\omega
\end{align}
$$

Multiplying by the mass $m$:

$$
\vec L(t) = (0, 0, mR^2\omega)
$$

### 3. Show that $|\vec L|$ is constant

Calculate the magnitude of the resulting vector:

$$
\begin{align}
|\vec L| &= \sqrt{0^2 + 0^2 + (mR^2\omega)^2} \\
         &= \sqrt{(mR^2\omega)^2} \\
         &= mR^2\omega
\end{align}
$$

Since $m$, $R$, and $\omega$ are given as constants of the motion, the magnitude $|\vec L|$ does not depend on time $t$. Therefore, it is constant.

### 4. Show that $\vec L$ is perpendicular to the plane of motion

The motion occurs in the $xy$ plane (as seen by the $z=0$ component in the position vector). 

The angular momentum vector we calculated is:

$$
\vec L = 
\begin{pmatrix}
0 \\
0 \\
mR^2\omega
\end{pmatrix}
$$

Because the $x$ and $y$ components are zero, the vector points exclusively along the $z$-axis. The $z$-axis is, by definition, perpendicular to the $xy$ plane.

## Final Result

* Velocity: $\vec v(t) = \bigl(-R\omega\sin(\omega t), R\omega\cos(\omega t), 0\bigr)$
* Angular Momentum: $\vec L(t) = \bigl(0, 0, mR^2\omega\bigr)$
* Magnitude: $|\vec L| = mR^2\omega$ (Constant)
* The vector $\vec L$ points along the $z$-axis, which is perpendicular to the $xy$ plane of motion.

## Interpretation



In uniform circular motion, the position and velocity vectors are always perpendicular to each other ($\vec r \cdot \vec v = 0$). Their cross product results in a vector that is perpendicular to the plane containing them. 

The fact that $\vec L$ is constant (both in magnitude and direction) is a consequence of the conservation of angular momentum. In this system, the force (centripetal force) points toward the origin. Because the force is parallel to the position vector, the torque $\vec \tau = \vec r \times \vec F$ is zero. Since torque is the rate of change of angular momentum ($\vec \tau = d\vec L/dt$), a zero torque implies that $\vec L$ must remain constant throughout the motion.