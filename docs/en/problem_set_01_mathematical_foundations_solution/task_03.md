# Task 03 – Integration of motion

## Problem Statement

### Part A
Given the velocity vector and initial position:

$$
\vec v(t) = \bigl(2t,3,-e^{-t}\bigr), \qquad
\vec r(0) = (0,1,2)
$$

Determine the position vector $\vec r(t)$ and the acceleration vector $\vec a(t)$.

### Part B
Given the acceleration vector, initial velocity, and initial position:

$$
\vec a(t) = \bigl(4,-\sin t,0\bigr), \qquad
\vec v(0) = (1,0,2), \qquad
\vec r(0) = (0,0,0)
$$

Determine the velocity vector $\vec v(t)$ and the position vector $\vec r(t)$.

## Theory

The kinematic relationships between position $\vec r(t)$, velocity $\vec v(t)$, and acceleration $\vec a(t)$ are established through the Fundamental Theorem of Calculus. 

To find position from velocity, one integrates the velocity function over time and adds the initial position:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau)\, d\tau
$$

Conversely, acceleration is the derivative of velocity:

$$
\vec a(t) = \frac{d\vec v(t)}{dt}
$$

The same integral logic applies to finding velocity from acceleration:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau)\, d\tau
$$

## Step-by-Step Solution

### Part A

Integrate the given velocity $\vec v(t)$ with respect to time $\tau$ from $0$ to $t$.

$$
\int_0^t \vec v(\tau)\, d\tau = \int_0^t \bigl(2\tau, 3, -e^{-\tau}\bigr)\, d\tau
$$

$$
\int_0^t \vec v(\tau)\, d\tau = \left( \tau^2, 3\tau, e^{-\tau} \right) \Big|_0^t
$$

Evaluate the definite integral boundaries.

$$
\int_0^t \vec v(\tau)\, d\tau = \bigl(t^2, 3t, e^{-t}\bigr) - \bigl(0, 0, 1\bigr)
$$

$$
\int_0^t \vec v(\tau)\, d\tau = \bigl(t^2, 3t, e^{-t} - 1\bigr)
$$

Add the initial position $\vec r(0)$ to find $\vec r(t)$.

$$
\vec r(t) = (0, 1, 2) + \bigl(t^2, 3t, e^{-t} - 1\bigr)
$$

$$
\vec r(t) = \bigl(t^2, 1 + 3t, 1 + e^{-t}\bigr)
$$

Differentiate the given velocity $\vec v(t)$ to find the acceleration $\vec a(t)$.

$$
\vec a(t) = \frac{d}{dt} \bigl(2t, 3, -e^{-t}\bigr)
$$

$$
\vec a(t) = \bigl(2, 0, e^{-t}\bigr)
$$

### Part B

Integrate the given acceleration $\vec a(t)$ to find the change in velocity.

$$
\int_0^t \vec a(\tau)\, d\tau = \int_0^t \bigl(4, -\sin\tau, 0\bigr)\, d\tau
$$

$$
\int_0^t \vec a(\tau)\, d\tau = \bigl(4\tau, \cos\tau, 0\bigr) \Big|_0^t
$$

$$
\int_0^t \vec a(\tau)\, d\tau = \bigl(4t, \cos t, 0\bigr) - \bigl(0, 1, 0\bigr)
$$

$$
\int_0^t \vec a(\tau)\, d\tau = \bigl(4t, \cos t - 1, 0\bigr)
$$

Add the initial velocity $\vec v(0)$ to obtain $\vec v(t)$.

$$
\vec v(t) = (1, 0, 2) + \bigl(4t, \cos t - 1, 0\bigr)
$$

$$
\vec v(t) = \bigl(1 + 4t, \cos t - 1, 2\bigr)
$$

Integrate the newly found velocity $\vec v(t)$ to find the position $\vec r(t)$.

$$
\int_0^t \vec v(\tau)\, d\tau = \int_0^t \bigl(1 + 4\tau, \cos\tau - 1, 2\bigr)\, d\tau
$$

$$
\int_0^t \vec v(\tau)\, d\tau = \left( \tau + 2\tau^2, \sin\tau - \tau, 2\tau \right) \Big|_0^t
$$

$$
\int_0^t \vec v(\tau)\, d\tau = \bigl(t + 2t^2, \sin t - t, 2t\bigr)
$$

Add the initial position $\vec r(0) = (0,0,0)$.

$$
\vec r(t) = \bigl(t + 2t^2, \sin t - t, 2t\bigr)
$$

## Final Result

### Part A
* Position: $\vec r(t) = \bigl(t^2, 1 + 3t, 1 + e^{-t}\bigr)$
* Acceleration: $\vec a(t) = \bigl(2, 0, e^{-t}\bigr)$

### Part B
* Velocity: $\vec v(t) = \bigl(1 + 4t, \cos t - 1, 2\bigr)$
* Position: $\vec r(t) = \bigl(t + 2t^2, \sin t - t, 2t\bigr)$

## Interpretation

Integrating kinematic vectors demands careful attention to initial conditions, as these constants of integration anchor the mathematical description to a specific physical reality. In Part A, an exponentially decaying term in the velocity profile yields a position coordinate that approaches an asymptote, representing a system subjected to a drag-like continuous braking force.