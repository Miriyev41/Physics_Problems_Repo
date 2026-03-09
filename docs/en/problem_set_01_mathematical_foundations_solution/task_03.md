# Task 03 – Integration of motion

## Problem Statement

### A) For a given velocity:

The velocity vector and initial position are defined as:

$$
\vec v(t) = \bigl(2t, 3, -e^{-t}\bigr), \qquad \vec r(0) = (0, 1, 2)
$$

1. Determine the position vector:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau)\, d\tau
$$

2. Determine the acceleration $\vec a(t)$.

### B) For a given acceleration:

The acceleration vector, initial velocity, and initial position are defined as:

$$
\vec a(t) = \bigl(4, -\sin t, 0\bigr), \qquad \vec v(0) = (1, 0, 2), \qquad \vec r(0) = (0, 0, 0)
$$

1. Determine the velocity vector:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau)\, d\tau
$$

2. Determine the position vector:

$$
\vec r(t) = \int_0^t \vec v(\tau)\, d\tau+ \vec r(0)
$$

## Theory

In kinematics, position, velocity, and acceleration are related through differentiation and integration with respect to time $t$. 

Velocity $\vec v(t)$ is the first derivative of position $\vec r(t)$. Conversely, the position vector can be found by integrating the velocity vector over time and adding the initial position $\vec r(0)$:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau
$$

Acceleration $\vec a(t)$ is the first derivative of velocity $\vec v(t)$. The velocity vector can be found by integrating the acceleration vector over time and adding the initial velocity $\vec v(0)$:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau) \, d\tau
$$

Acceleration can also be found directly by differentiating the velocity vector:

$$
\vec a(t) = \frac{d\vec v(t)}{dt}
$$

When integrating a vector function, the integral is applied independently to each scalar component of the vector. The variable $\tau$ is used as a dummy variable of integration to distinguish it from the upper limit $t$.

## Step-by-Step Solution

### Part A

#### 1. Determine the position vector $\vec r(t)$

Set up the integral for each component using the given $\vec v(\tau) = (2\tau, 3, -e^{-\tau})$ and $\vec r(0) = (0, 1, 2)$.

First component (x):

$$
\begin{align}
r_x(t) &= r_x(0) + \int_0^t v_x(\tau) \, d\tau \\
       &= 0 + \int_0^t 2\tau \, d\tau \\
       &= \left[ \tau^2 \right]_0^t \\
       &= t^2 - 0^2 \\
       &= t^2
\end{align}
$$

Second component (y):

$$
\begin{align}
r_y(t) &= r_y(0) + \int_0^t v_y(\tau) \, d\tau \\
       &= 1 + \int_0^t 3 \, d\tau \\
       &= 1 + \left[ 3\tau \right]_0^t \\
       &= 1 + (3t - 0) \\
       &= 1 + 3t
\end{align}
$$

Third component (z):

$$
\begin{align}
r_z(t) &= r_z(0) + \int_0^t v_z(\tau) \, d\tau \\
       &= 2 + \int_0^t \left( -e^{-\tau} \right) \, d\tau \\
       &= 2 + \left[ e^{-\tau} \right]_0^t \\
       &= 2 + (e^{-t} - e^0)
\end{align}
$$

Since $e^0 = 1$:

$$
\begin{align}
r_z(t) &= 2 + e^{-t} - 1 \\
       &= 1 + e^{-t}
\end{align}
$$

The full position vector is:

$$
\vec r(t) = \bigl(t^2, 1 + 3t, 1 + e^{-t}\bigr)
$$

#### 2. Determine the acceleration $\vec a(t)$

Differentiate the given velocity vector $\vec v(t) = (2t, 3, -e^{-t})$ with respect to time $t$.

First component (x):

$$
a_x(t) = \frac{d}{dt}(2t) = 2
$$

Second component (y):

$$
a_y(t) = \frac{d}{dt}(3) = 0
$$

Third component (z):

$$
a_z(t) = \frac{d}{dt}\left(-e^{-t}\right) = -(-e^{-t}) = e^{-t}
$$

The full acceleration vector is:

$$
\vec a(t) = \bigl(2, 0, e^{-t}\bigr)
$$

### Part B

#### 1. Determine the velocity vector $\vec v(t)$

Set up the integral for each component using the given $\vec a(\tau) = (4, -\sin \tau, 0)$ and $\vec v(0) = (1, 0, 2)$.

First component (x):

$$
\begin{align}
v_x(t) &= v_x(0) + \int_0^t a_x(\tau) \, d\tau \\
       &= 1 + \int_0^t 4 \, d\tau \\
       &= 1 + \left[ 4\tau \right]_0^t \\
       &= 1 + 4t - 0 \\
       &= 1 + 4t
\end{align}
$$

Second component (y):

$$
\begin{align}
v_y(t) &= v_y(0) + \int_0^t a_y(\tau) \, d\tau \\
       &= 0 + \int_0^t (-\sin \tau) \, d\tau \\
       &= \left[ \cos \tau \right]_0^t \\
       &= \cos t - \cos 0
\end{align}
$$

Since $\cos 0 = 1$:

$$
v_y(t) = \cos t - 1
$$

Third component (z):

$$
\begin{align}
v_z(t) &= v_z(0) + \int_0^t a_z(\tau) \, d\tau \\
       &= 2 + \int_0^t 0 \, d\tau \\
       &= 2 + 0 \\
       &= 2
\end{align}
$$

The full velocity vector is:

$$
\vec v(t) = \bigl(1 + 4t, \cos t - 1, 2\bigr)
$$

#### 2. Determine the position vector $\vec r(t)$

Set up the integral for each component using the derived $\vec v(\tau) = (1 + 4\tau, \cos \tau - 1, 2)$ and the given $\vec r(0) = (0, 0, 0)$.

First component (x):

$$
\begin{align}
r_x(t) &= r_x(0) + \int_0^t v_x(\tau) \, d\tau \\
       &= 0 + \int_0^t (1 + 4\tau) \, d\tau \\
       &= \left[ \tau + 2\tau^2 \right]_0^t \\
       &= (t + 2t^2) - (0 + 0) \\
       &= t + 2t^2
\end{align}
$$

Second component (y):

$$
\begin{align}
r_y(t) &= r_y(0) + \int_0^t v_y(\tau) \, d\tau \\
       &= 0 + \int_0^t (\cos \tau - 1) \, d\tau \\
       &= \left[ \sin \tau - \tau \right]_0^t \\
       &= (\sin t - t) - (\sin 0 - 0)
\end{align}
$$

Since $\sin 0 = 0$:

$$
r_y(t) = \sin t - t
$$

Third component (z):

$$
\begin{align}
r_z(t) &= r_z(0) + \int_0^t v_z(\tau) \, d\tau \\
       &= 0 + \int_0^t 2 \, d\tau \\
       &= \left[ 2\tau \right]_0^t \\
       &= 2t - 0 \\
       &= 2t
\end{align}
$$

The full position vector is:

$$
\vec r(t) = \bigl(t + 2t^2, \sin t - t, 2t\bigr)
$$

## Final Result

### Part A
* Position vector: $\vec r(t) = \bigl(t^2, 1 + 3t, 1 + e^{-t}\bigr)$
* Acceleration vector: $\vec a(t) = \bigl(2, 0, e^{-t}\bigr)$

### Part B
* Velocity vector: $\vec v(t) = \bigl(1 + 4t, \cos t - 1, 2\bigr)$
* Position vector: $\vec r(t) = \bigl(t + 2t^2, \sin t - t, 2t\bigr)$

## Interpretation

In kinematics, integration applies the area under the curve of a derivative vector to determine the total change in the corresponding state variable. The constants of integration correspond directly to the initial conditions of the system. 

In Part A, evaluating the initial state explicitly ensures the term $e^{-t}$ correctly contributes to a valid position at $t=0$, overcoming the non-zero value of $e^0$. In Part B, integrating a sinusoidal acceleration yields a velocity that oscillates, which subsequently integrates into a position function containing both a bounded sinusoidal term and a linear drift ($-t$).