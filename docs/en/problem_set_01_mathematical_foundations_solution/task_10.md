# Task 10 – Angular Momentum in Circular Motion

## Problem Statement

Consider circular motion in the $xy$ plane given by the position vector:

$$
\vec r(t) = \bigl( R\cos(\omega t), R\sin(\omega t), 0 \bigr)
$$

1. Determine the velocity:
   $$
   \vec v(t) = \dot{\vec r}(t)
   $$
2. Calculate the angular momentum with respect to the origin:
   $$
   \vec L(t) = m \, \vec r(t) \times \vec v(t)
   $$
3. Show that the magnitude $|\vec L| = mR^2\omega$ is constant, and that the vector $\vec L$ is perpendicular to the plane of motion.

## Theory



Angular momentum $\vec L$ of a point mass $m$ with respect to an origin is defined as the cross product of the position vector $\vec r$ and the linear momentum vector $\vec p = m\vec v$. Mathematically, this is expressed as:

$$
\vec L = \vec r \times \vec p = m (\vec r \times \vec v)
$$

The cross product produces a vector that is orthogonal (perpendicular) to both $\vec r$ and $\vec v$. If a particle moves entirely within a 2D plane, its position and velocity vectors lie in that plane, meaning their cross product must point exactly along the normal to that plane.

For a particle in uniform circular motion, the distance from the origin $R$ and the angular velocity $\omega$ are constant. Under these conditions, the angular momentum is a conserved quantity, meaning its magnitude and direction do not change over time.

## Step-by-Step Solution

### 1. Determine the velocity $\vec v(t)$

The velocity vector is the time derivative of the position vector. Differentiate each component of $\vec r(t)$ with respect to time $t$:

$$
\vec v(t) = \frac{d}{dt} \bigl( R\cos(\omega t), R\sin(\omega t), 0 \bigr)
$$

Applying the chain rule (since $\frac{d}{dt}(\omega t) = \omega$):

$$
\vec v(t) = \bigl( -R\omega\sin(\omega t), R\omega\cos(\omega t), 0 \bigr)
$$

### 2. Calculate the angular momentum $\vec L(t)$

The angular momentum is given by $\vec L(t) = m (\vec r(t) \times \vec v(t))$. 

First, let us set up the cross product using the determinant form with standard basis vectors:

$$
\vec r \times \vec v = 
\begin{pmatrix}
y v_z - z v_y \\
z v_x - x v_z \\
x v_y - y v_x
\end{pmatrix}
$$

Substitute the components $x = R\cos(\omega t)$, $y = R\sin(\omega t)$, $z = 0$ and $v_x = -R\omega\sin(\omega t)$, $v_y = R\omega\cos(\omega t)$, $v_z = 0$:

$$
\begin{align}
\vec r \times \vec v &= 
\begin{pmatrix}
(R\sin(\omega t))(0) - (0)(R\omega\cos(\omega t)) \\
(0)(-R\omega\sin(\omega t)) - (R\cos(\omega t))(0) \\
(R\cos(\omega t))(R\omega\cos(\omega t)) - (R\sin(\omega t))(-R\omega\sin(\omega t))
\end{pmatrix} \\
&= 
\begin{pmatrix}
0 \\
0 \\
R^2\omega\cos^2(\omega t) + R^2\omega\sin^2(\omega t)
\end{pmatrix}
\end{align}
$$

Factor out the common term $R^2\omega$ in the $z$-component:

$$
\vec r \times \vec v = 
\begin{pmatrix}
0 \\
0 \\
R^2\omega \left( \cos^2(\omega t) + \sin^2(\omega t) \right)
\end{pmatrix}
$$

Using the fundamental trigonometric identity $\cos^2(\omega t) + \sin^2(\omega t) = 1$, the cross product simplifies to:

$$
\vec r \times \vec v = (0, 0, R^2\omega)
$$

Now, multiply by the mass $m$ to get the angular momentum vector:

$$
\vec L(t) = m (0, 0, R^2\omega) = (0, 0, mR^2\omega)
$$

### 3. Show magnitude is constant and vector is perpendicular

To find the magnitude $|\vec L|$, calculate the Euclidean norm of the angular momentum vector:

$$
\begin{align}
|\vec L| &= \sqrt{0^2 + 0^2 + (mR^2\omega)^2} \\
         &= \sqrt{(mR^2\omega)^2} \\
         &= mR^2\omega
\end{align}
$$

Since $m$, $R$, and $\omega$ are all constants, the magnitude $|\vec L| = mR^2\omega$ does not depend on time $t$ and is therefore **constant**.

Next, we evaluate the direction. The position vector $\vec r(t)$ and velocity vector $\vec v(t)$ have zero $z$-components, meaning the motion is entirely restricted to the $xy$-plane. 

The angular momentum vector $\vec L(t) = (0, 0, mR^2\omega)$ has zero $x$- and $y$-components, meaning it points entirely along the $z$-axis. Since the $z$-axis is, by definition, orthogonal to the $xy$-plane, the vector $\vec L$ is strictly **perpendicular to the plane of motion**.

## Final Result

- **Velocity:** $\vec v(t) = (-R\omega\sin(\omega t), R\omega\cos(\omega t), 0)$
- **Angular Momentum Vector:** $\vec L(t) = (0, 0, mR^2\omega)$
- **Magnitude:** $|\vec L| = mR^2\omega$ (constant)
- **Direction:** The vector lies purely on the $z$-axis, which is perpendicular to the $xy$ plane of motion.

## Interpretation

This result mathematically proves a foundational concept in classical mechanics: for a particle undergoing uniform circular motion around an origin, its angular momentum is strictly conserved in both magnitude and direction. 

Because the net force required to maintain uniform circular motion (centripetal force) points directly toward the origin, it exerts zero torque ($\vec \tau = \vec r \times \vec F = 0$). According to Newton's Second Law for rotation ($\vec \tau = \frac{d\vec L}{dt}$), a zero net torque implies that the angular momentum cannot change over time, which matches our derived constant vector $\vec L = (0, 0, mR^2\omega)$. The direction of this vector is predicted by the Right-Hand Rule: curling the fingers of the right hand in the direction of the rotation (from $x$ towards $y$) leaves the thumb pointing along the positive $z$-axis.