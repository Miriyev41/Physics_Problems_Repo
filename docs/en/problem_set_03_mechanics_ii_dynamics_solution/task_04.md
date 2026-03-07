# Task 04 – Conservation of Energy

## Problem Statement

A body falls from a height $h$ without air resistance.

* Write down the total energy $E(h) = T(h) + U(h)$.
* Determine the velocity as a function of height $v(h)$.
* Compare with the solution from Newton's second law.
* At what height does the kinetic energy account for 75% of the total energy?

## Theory

The Principle of Conservation of Mechanical Energy states that in an isolated system where only conservative forces act, the total mechanical energy remains constant. For a falling body, the mechanical energy is the sum of:
1.  **Kinetic Energy ($T$):** Energy of motion, defined as $T = \frac{1}{2}mv^2$.
2.  **Potential Energy ($U$):** Energy of position, defined as $U = mgy$ in a uniform gravitational field.

As the body falls, potential energy is converted into kinetic energy, but their sum $E$ does not change.



## Step-by-Step Solution

### 1. Total Energy Equation

At the starting height $h$, the body is at rest ($v=0$). The total energy is purely potential:

$$
E_{total} = T(h) + U(h) = 0 + mgh = mgh
$$

As the body reaches an arbitrary height $y$ (where $0 \le y \le h$), the total energy expression is:

$$
E(y) = \frac{1}{2}mv(y)^2 + mgy
$$

### 2. Velocity as a Function of Height

Since energy is conserved, $E(y) = E_{total}$:

$$
\frac{1}{2}mv^2 + mgy = mgh
$$

Subtracting $mgy$ from both sides and dividing by $m$:

$$
\frac{1}{2}v^2 = g(h - y)
$$

Solving for $v$:

$$
v(y) = \sqrt{2g(h - y)}
$$

### 3. Comparison with Newton's Second Law

According to Newton's Second Law, a falling body has a constant acceleration $a = -g$. Using the kinematic equation:

$$
v_f^2 = v_i^2 + 2a\Delta y
$$

With $v_i = 0$ and displacement $\Delta y = -(h - y)$:

$$
v^2 = 0 + 2(-g)(-(h - y)) = 2g(h - y)
$$

The result $v = \sqrt{2g(h - y)}$ is identical to the one derived from energy conservation, demonstrating that the energy method is consistent with Newtonian dynamics.

### 4. Calculation for 75% Kinetic Energy

We seek the height $y$ where $T(y) = 0.75 E_{total}$. Substituting the energy expressions:

$$
\frac{1}{2}mv^2 = 0.75(mgh)
$$

Since $T(y) = E_{total} - U(y)$:

$$
mgh - mgy = 0.75mgh
$$

Dividing by $mg$:

$$
h - y = 0.75h
$$

$$
y = h - 0.75h = 0.25h
$$

## Final Result

* **Total Energy**: $E = mgh$
* **Velocity Function**: $v(y) = \sqrt{2g(h - y)}$
* **Newtonian Consistency**: Both methods yield $v^2 = 2g\Delta h$.
* **Specific Height**: The kinetic energy reaches 75% of the total energy at $y = \frac{1}{4}h$.

## Interpretation

In the absence of air resistance, the conversion of potential energy to kinetic energy is linear with respect to the distance fallen. At the midpoint of the fall ($y = 0.5h$), the energy is split equally between $T$ and $U$. To reach 75% kinetic energy, the body must fall through 75% of the total height, leaving it at a position 25% above the ground.