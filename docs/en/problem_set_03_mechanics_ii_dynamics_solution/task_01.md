# Task 01 – Newton's second law (constant force)

## Problem Statement

A constant force acts on a body of mass $m = 2\ \text{kg}$:

$$
\vec F = (6, 2)\ \text{N}
$$

The body starts with an initial velocity $\vec v(0) = (1, -1)\ \text{m/s}$ from the initial position $\vec r(0) = (0, 0)\ \text{m}$.

The required operations are:
1. Determine the acceleration $\vec a(t)$.
2. Determine the velocity $\vec v(t)$.
3. Determine the position $\vec r(t)$.
4. Calculate the work $W$ done by the force at time $t = 3\ \text{s}$.
5. Verify the consistency with the work-energy theorem.

## Theory

Newton's Second Law states that the acceleration of an object is directly proportional to the net force acting on it and inversely proportional to its mass:

$$
\vec F = m\vec a \implies \vec a = \frac{\vec F}{m}
$$

For a constant force, the acceleration is also constant. The velocity $\vec v(t)$ and position $\vec r(t)$ can be found by integrating the acceleration with respect to time:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau) \, d\tau
$$

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau
$$

The work done by a constant force is the dot product of the force and the displacement:

$$
W = \vec F \cdot \Delta \vec r
$$

The work-energy theorem states that the work done by the net force is equal to the change in kinetic energy:

$$
W = \Delta K = \frac{1}{2} m |\vec v(t)|^2 - \frac{1}{2} m |\vec v(0)|^2
$$

## Step-by-Step Solution

### 1. Determine the acceleration $\vec a(t)$

Using Newton's Second Law:

$$
\vec a = \frac{\vec F}{m} = \frac{1}{2}
\begin{pmatrix}
6 \\
2
\end{pmatrix}
$$

Calculate each component:

$$
a_x = \frac{6}{2} = 3\ \text{m/s}^2
$$

$$
a_y = \frac{2}{2} = 1\ \text{m/s}^2
$$

Therefore:

$$
\vec a(t) = (3, 1)\ \text{m/s}^2
$$

### 2. Determine the velocity $\vec v(t)$

Integrate the constant acceleration and add the initial velocity $\vec v(0) = (1, -1)$:

First component ($v_x$):

$$
v_x(t) = v_x(0) + a_x t = 1 + 3t
$$

Second component ($v_y$):

$$
v_y(t) = v_y(0) + a_y t = -1 + 1t
$$

The velocity vector is:

$$
\vec v(t) = (1 + 3t, -1 + t)\ \text{m/s}
$$

### 3. Determine the position $\vec r(t)$

Integrate the velocity vector and add the initial position $\vec r(0) = (0, 0)$:

First component ($x$):

$$
x(t) = x(0) + \int_0^t (1 + 3\tau) \, d\tau = 0 + [ \tau + 1.5\tau^2 ]_0^t = t + 1.5t^2
$$

Second component ($y$):

$$
y(t) = y(0) + \int_0^t (-1 + \tau) \, d\tau = 0 + [ -\tau + 0.5\tau^2 ]_0^t = -t + 0.5t^2
$$

The position vector is:

$$
\vec r(t) = (t + 1.5t^2, -t + 0.5t^2)\ \text{m}
$$

### 4. Calculate the work done at $t = 3\ \text{s}$

**Step 1: Calculate the displacement $\Delta \vec r$ at $t = 3$**

$$
x(3) = 3 + 1.5(3^2) = 3 + 1.5(9) = 3 + 13.5 = 16.5\ \text{m}
$$

$$
y(3) = -3 + 0.5(3^2) = -3 + 4.5 = 1.5\ \text{m}
$$

So, $\Delta \vec r = (16.5, 1.5)\ \text{m}$.

**Step 2: Calculate work $W = \vec F \cdot \Delta \vec r$**

$$
\begin{align}
W &= (6, 2) \cdot (16.5, 1.5) \\
  &= 6(16.5) + 2(1.5) \\
  &= 99 + 3 \\
  &= 102\ \text{J}
\end{align}
$$

### 5. Verify the Work-Energy Theorem

**Step 1: Initial Kinetic Energy $K_0$**

$$
|\vec v(0)|^2 = 1^2 + (-1)^2 = 2
$$

$$
K_0 = \frac{1}{2}(2)(2) = 2\ \text{J}
$$

**Step 2: Final Kinetic Energy $K_f$ at $t = 3$**

$$
v_x(3) = 1 + 3(3) = 10\ \text{m/s}
$$

$$
v_y(3) = -1 + 3 = 2\ \text{m/s}
$$

$$
|\vec v(3)|^2 = 10^2 + 2^2 = 104
$$

$$
K_f = \frac{1}{2}(2)(104) = 104\ \text{J}
$$

**Step 3: Change in Kinetic Energy $\Delta K$**

$$
\Delta K = 104 - 2 = 102\ \text{J}
$$

Since $W = 102\ \text{J}$ and $\Delta K = 102\ \text{J}$, the theorem is verified.

## Final Result

* Acceleration: $\vec a(t) = (3, 1)\ \text{m/s}^2$
* Velocity: $\vec v(t) = (1 + 3t, -1 + t)\ \text{m/s}$
* Position: $\vec r(t) = (t + 1.5t^2, -t + 0.5t^2)\ \text{m}$
* Work done: $W = 102\ \text{J}$
* Verification: $W = \Delta K = 102\ \text{J}$

## Interpretation



Under a constant force, the particle follows a parabolic trajectory. The work done by the force directly increases the speed of the particle, which is reflected in the gain of kinetic energy. The fact that the work-energy theorem holds confirms that our kinematic derivations (integration of acceleration) and our dynamical calculations (work done by force) are perfectly consistent.