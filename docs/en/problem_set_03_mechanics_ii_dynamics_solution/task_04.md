# Task 04 – Conservation of energy

## Problem Statement

A body falls from a height $h$ without air resistance.

1. Write down the total energy $E(y) = T(y) + U(y)$.
2. Determine the velocity as a function of height $v(y)$.
3. Compare with the solution from Newton's second law.
4. At what height does the kinetic energy account for 75% of the total energy?

*(Note: We will use $y$ as the variable representing the current height, and $h$ as the initial drop height).*

## Theory

The principle of conservation of mechanical energy states that in the absence of non-conservative forces (like air resistance or friction), the total mechanical energy of a system remains constant throughout the motion. The total mechanical energy $E$ is the sum of kinetic energy $T$ and potential energy $U$.

For a body in free fall near the Earth's surface:
- Kinetic energy is given by $T = \frac{1}{2}mv^2$.
- Gravitational potential energy is given by $U = mgy$, where $y$ is the height above a chosen reference level (usually the ground).

Alternatively, the motion can be analyzed using kinematics and Newton's Second Law, which relates the constant gravitational force to a constant downward acceleration. Both approaches must yield identical results.

## Step-by-Step Solution

### 1. Total energy $E(y) = T(y) + U(y)$

Let the body be released from rest at an initial height $y = h$. At this moment, the velocity is zero, so the kinetic energy is zero ($T = 0$). The total initial energy is purely potential:

$$
E_{initial} = mgh
$$

By the conservation of energy, the total energy at any arbitrary height $y$ (where $0 \le y \le h$) must equal this initial energy:

$$
E(y) = T(y) + U(y) = mgh
$$

Substituting the explicit forms for kinetic and potential energy:

$$
\frac{1}{2}mv(y)^2 + mgy = mgh
$$

### 2. Determine velocity as a function of height $v(y)$

Starting from the energy conservation equation:

$$
\frac{1}{2}mv(y)^2 + mgy = mgh
$$

Subtract $mgy$ from both sides:

$$
\frac{1}{2}mv(y)^2 = mg(h - y)
$$

Divide both sides by the mass $m$ (which cancels out) and multiply by 2:

$$
v(y)^2 = 2g(h - y)
$$

Taking the square root gives the magnitude of the velocity (speed) at height $y$:

$$
v(y) = \sqrt{2g(h - y)}
$$

### 3. Compare with the solution from Newton's second law

Using Newton's Second Law, the only force acting on the body is gravity:

$$
\sum F_y = -mg
$$

$$
ma_y = -mg \implies a_y = -g
$$

Since the acceleration is constant, we can use the time-independent kinematic equation (Torricelli's equation):

$$
v_f^2 = v_i^2 + 2a_y \Delta y
$$

Substitute the known values:
- Initial velocity $v_i = 0$
- Acceleration $a_y = -g$
- Displacement $\Delta y = y - h$ (final height minus initial height)

$$
\begin{align}
v(y)^2 &= 0 + 2(-g)(y - h) \\
v(y)^2 &= -2g(y - h) \\
v(y)^2 &= 2g(h - y)
\end{align}
$$

Taking the square root yields:

$$
v(y) = \sqrt{2g(h - y)}
$$

This result perfectly matches the one derived from the conservation of energy.

### 4. Height where kinetic energy is 75% of total energy

We are looking for the height $y$ at which the kinetic energy $T(y)$ is exactly $75\%$ (or $\frac{3}{4}$) of the total energy $E$:

$$
T(y) = 0.75 E
$$

Since $E = T(y) + U(y)$, this implies that the remaining $25\%$ must be potential energy:

$$
U(y) = 0.25 E = \frac{1}{4} E
$$

Substitute $U(y) = mgy$ and $E = mgh$:

$$
mgy = \frac{1}{4} mgh
$$

Divide both sides by $mg$:

$$
y = \frac{1}{4} h
$$

## Final Result

- **Total Energy:** $E(y) = \frac{1}{2}mv(y)^2 + mgy = mgh$
- **Velocity function:** $v(y) = \sqrt{2g(h - y)}$
- **Comparison:** Newton's second law yields $v_f^2 = v_i^2 + 2a\Delta y \implies v(y) = \sqrt{2g(h-y)}$, which matches exactly.
- **75% Kinetic Energy Height:** $y = \frac{h}{4}$

## Interpretation

The principle of conservation of energy provides a powerful scalar method to solve motion problems without needing to integrate vectors or track time. As the body falls, its potential energy linearly decreases while its kinetic energy linearly increases by the exact same amount. Because potential energy is directly proportional to height, when the body has lost 75% of its potential energy (converting it into kinetic energy), it must have fallen 75% of the way down, placing it at exactly one-quarter ($h/4$) of its original height.