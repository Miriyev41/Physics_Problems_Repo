# Task 07 – 2D Motion with a Given Acceleration

## Problem Statement

Given a constant acceleration vector $\vec{a} = (2, -3)$ and the following initial conditions at $t=0$:
* Initial velocity: $\vec{v}(0) = (1, 0)$
* Initial position: $\vec{r}(0) = (0, 0)$

1. Determine the velocity vector $\vec{v}(t)$ as a function of time.
2. Determine the position vector $\vec{r}(t)$ as a function of time.
3. Describe the trajectory and the orientation of the velocity and acceleration vectors over time.

## Theory

For motion with constant acceleration in two dimensions, the kinematic equations can be solved by integrating each component of the acceleration vector independently.

The velocity vector is the integral of acceleration:

$$
\vec{v}(t) = \int \vec{a} \, dt = \vec{v}_0 + \vec{a}t
$$

The position vector is the integral of velocity:

$$
\vec{r}(t) = \int \vec{v}(t) \, dt = \vec{r}_0 + \vec{v}_0 t + \frac{1}{2}\vec{a}t^2
$$

Since the acceleration is constant, the resulting trajectory in the $xy$-plane will be parabolic.

## Step-by-Step Solution

### 1. Determining Velocity $\vec{v}(t)$

Given $\vec{a} = \begin{pmatrix} 2 \\ -3 \end{pmatrix}$ and $\vec{v}_0 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

Integrating each component:

$$
v_x(t) = v_{0x} + a_x t = 1 + 2t
$$

$$
v_y(t) = v_{0y} + a_y t = 0 - 3t = -3t
$$

Thus, the velocity vector is:

$$
\vec{v}(t) = \begin{pmatrix} 1 + 2t \\ -3t \end{pmatrix}
$$

### 2. Determining Position $\vec{r}(t)$

Given $\vec{r}_0 = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$.

Integrating the velocity components:

$$
x(t) = x_0 + \int v_x(t) \, dt = 0 + \int (1 + 2t) \, dt = t + t^2
$$

$$
y(t) = y_0 + \int v_y(t) \, dt = 0 + \int (-3t) \, dt = -\frac{3}{2}t^2
$$

Thus, the position vector is:

$$
\vec{r}(t) = \begin{pmatrix} t + t^2 \\ -1.5t^2 \end{pmatrix}
$$

### 3. Trajectory and Vector Analysis

* **Trajectory**: To find the path, we can eliminate $t$. From $y = -1.5t^2$, we have $t^2 = -y/1.5$. Substituting into $x(t)$ reveals a quadratic relationship, confirming the path is a parabola.
* **Acceleration Vector**: Remains fixed at $\vec{a} = (2, -3)$ for all $t$.
* **Velocity Vector**: At $t=0$, $\vec{v}$ is purely horizontal $(1, 0)$. As $t$ increases, the $y$-component becomes increasingly negative while the $x$-component grows, causing the velocity vector to rotate clockwise and increase in magnitude.

## Final Result

* **Velocity**: $\vec{v}(t) = (1 + 2t, -3t)$
* **Position**: $\vec{r}(t) = (t + t^2, -1.5t^2)$

## Interpretation

The motion starts with a purely horizontal push, but the constant diagonal acceleration immediately begins pulling the particle "down" (negative $y$) and "right" (positive $x$). Because the acceleration has a constant direction, the particle follows a smooth parabolic arc that aligns more closely with the direction of the acceleration vector as time approaches infinity.