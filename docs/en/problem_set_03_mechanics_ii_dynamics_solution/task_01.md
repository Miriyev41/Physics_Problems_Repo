# Task 01 – Newton's second law (constant force)

## Problem Statement

A constant force acts on a body of mass $m = 2\ \mathrm{kg}$:

$$
\vec F = [6, 2]\ \mathrm{N}
$$

The body starts with an initial velocity $\vec v(0) = (1, -1)\ \mathrm{\frac{m}{s}}$ from the point $\vec r(0)=(0,0)\ \mathrm{m}$. 

Calculate the following:
1. Determine $\vec a(t)$.
2. Determine $\vec v(t)$.
3. Determine $\vec r(t)$.
4. Draw the trajectory of the motion.
5. Calculate the work done by the force at time $t=3\ \mathrm{s}$.
6. Check the consistency with the work-energy theorem.

## Theory

Newton's Second Law states that the acceleration of an object is directly proportional to the net force acting on it and inversely proportional to its mass:

$$
\vec a = \frac{\vec F}{m}
$$

If the force is constant, the acceleration is also constant. We can determine the velocity and position vectors by integrating the acceleration with respect to time using the standard kinematic equations:

$$
\vec v(t) = \vec v(0) + \vec a t
$$

$$
\vec r(t) = \vec r(0) + \vec v(0)t + \frac{1}{2}\vec a t^2
$$

The **work-energy theorem** states that the total work $W$ done by the net force on an object equals its change in kinetic energy $\Delta K$:

$$
W = \Delta K = K_f - K_i
$$

For a constant force, work can also be calculated directly using the dot product of the force vector and the displacement vector:

$$
W = \vec F \cdot \Delta \vec r
$$

## Step-by-Step Solution

### 1. Determine acceleration $\vec a(t)$

Using Newton's Second Law:

$$
\begin{align}
\vec a(t) &= \frac{\vec F}{m} \\
          &= \frac{(6, 2)}{2} \\
          &= (3, 1)\ \mathrm{\frac{m}{s^2}}
\end{align}
$$

The acceleration is constant over time.

### 2. Determine velocity $\vec v(t)$

Integrate the constant acceleration and apply the initial condition $\vec v(0) = (1, -1)$:

$$
\begin{align}
\vec v(t) &= \vec v(0) + \vec a t \\
          &= (1, -1) + (3, 1)t \\
          &= (1 + 3t, -1 + t)\ \mathrm{\frac{m}{s}}
\end{align}
$$

### 3. Determine position $\vec r(t)$

Integrate the velocity and apply the initial condition $\vec r(0) = (0, 0)$:

$$
\begin{align}
\vec r(t) &= \vec r(0) + \vec v(0)t + \frac{1}{2}\vec a t^2 \\
          &= (0, 0) + (1, -1)t + \frac{1}{2}(3, 1)t^2 \\
          &= \left( t + 1.5t^2, -t + 0.5t^2 \right)\ \mathrm{m}
\end{align}
$$

### 4. Work done by the force at $t=3\ \mathrm{s}$

First, find the displacement at $t = 3\ \mathrm{s}$. Since the initial position is the origin, the displacement is simply the position vector at $t = 3$:

$$
\begin{align}
\vec r(3) &= \left( 3 + 1.5(3)^2, -3 + 0.5(3)^2 \right) \\
          &= (3 + 13.5, -3 + 4.5) \\
          &= (16.5, 1.5)\ \mathrm{m}
\end{align}
$$

Now calculate the work using the dot product:

$$
\begin{align}
W &= \vec F \cdot \vec r(3) \\
  &= (6)(16.5) + (2)(1.5) \\
  &= 99 + 3 \\
  &= 102\ \mathrm{J}
\end{align}
$$

### 5. Check consistency with the work-energy theorem

Calculate the initial kinetic energy at $t=0$:

$$
\begin{align}
K_i &= \frac{1}{2} m |\vec v(0)|^2 \\
    &= \frac{1}{2} (2) \left( 1^2 + (-1)^2 \right) \\
    &= 1(1 + 1) \\
    &= 2\ \mathrm{J}
\end{align}
$$

Calculate the final velocity at $t=3\ \mathrm{s}$:

$$
\begin{align}
\vec v(3) &= (1 + 3(3), -1 + 3) \\
          &= (10, 2)\ \mathrm{\frac{m}{s}}
\end{align}
$$

Calculate the final kinetic energy at $t=3\ \mathrm{s}$:

$$
\begin{align}
K_f &= \frac{1}{2} m |\vec v(3)|^2 \\
    &= \frac{1}{2} (2) \left( 10^2 + 2^2 \right) \\
    &= 100 + 4 \\
    &= 104\ \mathrm{J}
\end{align}
$$

Calculate the change in kinetic energy:

$$
\begin{align}
\Delta K &= K_f - K_i \\
         &= 104 - 2 \\
         &= 102\ \mathrm{J}
\end{align}
$$

## Final Result

- **Acceleration:** $\vec a(t) = (3, 1)\ \mathrm{\frac{m}{s^2}}$
- **Velocity:** $\vec v(t) = (1 + 3t, -1 + t)\ \mathrm{\frac{m}{s}}$
- **Position:** $\vec r(t) = (t + 1.5t^2, -t + 0.5t^2)\ \mathrm{m}$
- **Work done ($t=3$):** $W = 102\ \mathrm{J}$
- **Kinetic energy change:** $\Delta K = 102\ \mathrm{J}$ (matches the work done).

## Interpretation

The exact match between the direct mechanical work calculation ($102\ \mathrm{J}$) and the change in kinetic energy ($102\ \mathrm{J}$) perfectly validates the work-energy theorem. The initial negative y-velocity slightly pulled the particle down, but the constant positive acceleration eventually turns the particle's path into a rightward, upward-sweeping parabola.