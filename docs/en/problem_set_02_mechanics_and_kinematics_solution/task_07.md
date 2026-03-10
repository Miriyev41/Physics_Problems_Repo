# Task 07 – 2D motion with a given acceleration

## Problem Statement

Given is the acceleration $\vec a = (2, -3)$ and the initial conditions: $\vec v(0)=(1,0)$, $\vec r(0)=(0,0)$.

1. Determine $\vec v(t)$.
2. Determine $\vec r(t)$.
3. Draw the trajectory, velocity vector, and acceleration vector at a few selected moments in time, or create an HTML animation.

## Theory

When the acceleration of a particle is constant, the velocity and position vectors can be determined by integrating the constant acceleration with respect to time. The relationships are given by the fundamental kinematic equations for constant acceleration in vector form:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a \, d\tau = \vec v_0 + \vec a t
$$

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau = \vec r_0 + \vec v_0 t + \frac{1}{2} \vec a t^2
$$

Since the motion is in two dimensions (a plane) and the acceleration vector is not collinear with the initial velocity vector, the resulting trajectory will be a parabola.

## Step-by-Step Solution

### 1. Determine the velocity $\vec v(t)$

We start by identifying the components of the initial velocity and constant acceleration vectors:

$$
\vec v_0 = 
\begin{pmatrix}
1 \\
0
\end{pmatrix}
$$

$$
\vec a = 
\begin{pmatrix}
2 \\
-3
\end{pmatrix}
$$

Integrating the acceleration to find the velocity:

$$
\begin{align}
\vec v(t) &= \vec v_0 + \vec a t \\
          &= 
\begin{pmatrix}
1 \\
0
\end{pmatrix}
+ 
\begin{pmatrix}
2 \\
-3
\end{pmatrix} t \\
          &= 
\begin{pmatrix}
1 + 2t \\
-3t
\end{pmatrix}
\end{align}
$$

Written in coordinate form, the velocity vector is $\vec v(t) = (1 + 2t, -3t)$.

### 2. Determine the position $\vec{r}(t)$

The initial position is at the origin:

$$
\vec{r}_0 = \begin{pmatrix} 0 \\ 0 \end{pmatrix}
$$

Integrating the velocity vector to find the position:



$$
\begin{aligned}
\vec{r}(t) &= \vec{r}_0 + \int_0^t \vec{v}(\tau) \, d\tau \\
&= \begin{pmatrix} 0 \\ 0 \end{pmatrix} + \int_0^t \begin{pmatrix} 1 + 2\tau \\ -3\tau \end{pmatrix} \, d\tau \\
&= \begin{pmatrix} \left[ \tau + \tau^2 \right]_0^t \\ \left[ -\frac{3}{2}\tau^2 \right]_0^t \end{pmatrix} \\
&= \begin{pmatrix} t + t^2 \\ -\frac{3}{2}t^2 \end{pmatrix}
\end{aligned}
$$

Written in coordinate form, the position vector is $\vec{r}(t) = (t + t^2, -1.5t^2)$.

## Final Result

- **Velocity:** $\vec v(t) = (1 + 2t, -3t)$
- **Position:** $\vec r(t) = (t + t^2, -1.5t^2)$

## Interpretation

The motion combines a constant velocity in the x-direction modified by a constant positive acceleration, and a motion from rest in the y-direction driven by a constant negative acceleration. Because the acceleration is uniform and acts at an angle to the initial velocity, the particle describes a parabolic trajectory opening towards the negative y-axis. The acceleration vector $\vec a$ remains fixed in both magnitude and direction throughout the motion, while the velocity vector $\vec v(t)$ continuously rotates to align more closely with the direction of the acceleration vector as time approaches infinity.