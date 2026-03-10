# Task 03 – Integration of Motion

## Problem Statement

### Part A
Given the velocity vector and initial position:

$$
\vec v(t) = \bigl(2t, 3, -e^{-t}\bigr), \qquad \vec r(0) = (0,1,2)
$$

1. Determine the position vector $\vec r(t)$.
2. Determine the acceleration vector $\vec a(t)$.

### Part B
Given the acceleration vector, initial velocity, and initial position:

$$
\vec a(t) = \bigl(4, -\sin t, 0\bigr), \qquad \vec v(0) = (1,0,2), \qquad \vec r(0) = (0,0,0)
$$

1. Determine the velocity vector $\vec v(t)$.
2. Determine the position vector $\vec r(t)$.

## Theory

The kinematic relationships between position $\vec r(t)$, velocity $\vec v(t)$, and acceleration $\vec a(t)$ are governed by calculus. Acceleration is the time derivative of velocity, and velocity is the time derivative of position. 

Conversely, if the rate of change is known, the original quantity can be recovered through integration, provided an initial condition is given to establish the integration constant. The Fundamental Theorem of Calculus allows us to express these relationships as definite integrals from $t=0$ to $t$:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau) \, d\tau
$$

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau
$$

## Step-by-Step Solution

### Part A: Known Velocity

#### 1. Determine position $\vec r(t)$

The position vector is found by integrating the velocity vector component by component:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau
$$

Substitute the given expressions:

$$
\vec r(t) = (0, 1, 2) + \int_0^t \bigl(2\tau, 3, -e^{-\tau}\bigr) \, d\tau
$$

Evaluate the integral for each component:

$$
\begin{align}
\int_0^t 2\tau \, d\tau &= \left[ \tau^2 \right]_0^t = t^2 \\
\int_0^t 3 \, d\tau &= \left[ 3\tau \right]_0^t = 3t \\
\int_0^t -e^{-\tau} \, d\tau &= \left[ e^{-\tau} \right]_0^t = e^{-t} - 1
\end{align}
$$

Add the initial position to the integrated vector:

$$
\begin{align}
\vec r(t) &= (0, 1, 2) + (t^2, 3t, e^{-t} - 1) \\
          &= (t^2, 1 + 3t, 2 + e^{-t} - 1) \\
          &= (t^2, 1 + 3t, 1 + e^{-t})
\end{align}
$$

#### 2. Determine acceleration $\vec a(t)$

Acceleration is the derivative of velocity:

$$
\vec a(t) = \frac{d\vec v}{dt}
$$

Differentiate each component of $\vec v(t) = (2t, 3, -e^{-t})$:

$$
\begin{align}
\vec a(t) &= \left( \frac{d}{dt}(2t), \frac{d}{dt}(3), \frac{d}{dt}(-e^{-t}) \right) \\
          &= \bigl(2, 0, e^{-t}\bigr)
\end{align}
$$

---

### Part B: Known Acceleration

#### 1. Determine velocity $\vec v(t)$

The velocity vector is found by integrating the acceleration vector:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau) \, d\tau
$$

Substitute the given expressions:

$$
\vec v(t) = (1, 0, 2) + \int_0^t \bigl(4, -\sin \tau, 0\bigr) \, d\tau
$$

Evaluate the integral for each component:

$$
\begin{align}
\int_0^t 4 \, d\tau &= 4t \\
\int_0^t -\sin \tau \, d\tau &= \left[ \cos \tau \right]_0^t = \cos t - 1 \\
\int_0^t 0 \, d\tau &= 0
\end{align}
$$

Add the initial velocity to the integrated vector:

$$
\begin{align}
\vec v(t) &= (1, 0, 2) + (4t, \cos t - 1, 0) \\
          &= (1 + 4t, \cos t - 1, 2)
\end{align}
$$

#### 2. Determine position $\vec r(t)$

The position vector is found by integrating the newly derived velocity vector:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau
$$

Substitute the given expressions:

$$
\vec r(t) = (0, 0, 0) + \int_0^t \bigl(1 + 4\tau, \cos \tau - 1, 2\bigr) \, d\tau
$$

Evaluate the integral for each component:

$$
\begin{align}
\int_0^t (1 + 4\tau) \, d\tau &= \left[ \tau + 2\tau^2 \right]_0^t = t + 2t^2 \\
\int_0^t (\cos \tau - 1) \, d\tau &= \left[ \sin \tau - \tau \right]_0^t = \sin t - t \\
\int_0^t 2 \, d\tau &= \left[ 2\tau \right]_0^t = 2t
\end{align}
$$

Add the initial position to the integrated vector:

$$
\vec r(t) = \bigl(t + 2t^2, \sin t - t, 2t\bigr)
$$

## Final Result

### Part A
- Position: $\vec r(t) = (t^2, 1 + 3t, 1 + e^{-t})$
- Acceleration: $\vec a(t) = (2, 0, e^{-t})$

### Part B
- Velocity: $\vec v(t) = (1 + 4t, \cos t - 1, 2)$
- Position: $\vec r(t) = (t + 2t^2, \sin t - t, 2t)$

## Interpretation

In kinematics, integration strictly demands proper handling of initial conditions. A common error is evaluating the indefinite integral and forgetting the constants of integration. Using definite integrals from $0$ to $t$, as demonstrated here, elegantly avoids this pitfall by ensuring the boundaries accurately reflect the physical initial states. 

In Part B, we see that an acceleration lacking a $z$-component does not mean the position in the $z$-direction is stationary; the initial velocity ensures a steady drift along the $z$-axis ($z = 2t$), exemplifying Newton's First Law.