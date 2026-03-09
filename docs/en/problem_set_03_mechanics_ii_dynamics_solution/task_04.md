# Task 04 – Conservation of energy

## Problem Statement

A body falls from a height $h$ without air resistance.

The required operations are:
1. Write down the total mechanical energy $E(h) = T(h) + U(h)$.
2. Determine the velocity as a function of height $v(h)$.
3. Compare the result with the solution derived from Newton's second law.
4. Determine at what height the kinetic energy accounts for 75% of the total energy.

## Theory

The Principle of Conservation of Mechanical Energy states that in the absence of non-conservative forces (like friction or air resistance), the total mechanical energy $E$ of a system remains constant. Total energy is the sum of kinetic energy $T$ and potential energy $U$:

$$
E = T + U
$$

Kinetic energy is defined as:

$$
T = \frac{1}{2} mv^2
$$

Gravitational potential energy near the Earth's surface is defined as:

$$
U = mgy
$$

where $y$ is the height above a chosen reference level ($y=0$). For a body falling from rest at height $h$, the initial energy is purely potential. As it falls, potential energy is converted into kinetic energy, but their sum remains $mgh$ at every point in the trajectory.

## Step-by-Step Solution

### 1. Write down the total energy $E(h)$

Consider the body at its starting point (height $h$) and at an arbitrary height $y$ during the fall.

At the starting point ($y = h$):
- Velocity $v = 0$, so $T = 0$.
- Potential energy $U = mgh$.
- Total energy $E = mgh$.

At an arbitrary height $y$:

$$
E(y) = T(y) + U(y) = \frac{1}{2}mv(y)^2 + mgy
$$

Since energy is conserved, $E(y) = E(h)$ for all $y \in [0, h]$:

$$
E = mgh
$$

### 2. Determine velocity as a function of height $v(h)$

Using the conservation equation $E(y) = E(h)$:

$$
\frac{1}{2}mv^2 + mgy = mgh
$$

Isolate the kinetic energy term:

$$
\frac{1}{2}mv^2 = mgh - mgy
$$

Divide by $m$ and factor out $g$:

$$
\frac{1}{2}v^2 = g(h - y)
$$

Solve for $v$:

$$
v(y) = \sqrt{2g(h - y)}
$$

Here, $(h - y)$ represents the distance fallen.

### 3. Compare with Newton's second law

According to Newton's Second Law, a falling body has constant acceleration $a = g$. Using the kinematic equation (Torricelli's equation) for constant acceleration:

$$
v^2 = v_0^2 + 2a\Delta y
$$

Substituting $v_0 = 0$, $a = g$, and displacement $\Delta y = h - y$:

$$
v^2 = 2g(h - y) \implies v = \sqrt{2g(h - y)}
$$

The results are identical. The energy approach is often simpler because it relates states (initial and final) without requiring integration of the equations of motion over time.

### 4. Height where kinetic energy is 75% of total energy

We are looking for the height $y^*$ where:

$$
T(y^*) = 0.75 E
$$

Substitute the expressions for $T$ and $E$:

$$
mgh - mgy^* = 0.75 (mgh)
$$

Divide by $mgh$:

$$
1 - \frac{y^*}{h} = 0.75
$$

Solve for $y^*$:

$$
\frac{y^*}{h} = 1 - 0.75 = 0.25
$$

$$
y^* = 0.25h
$$

The kinetic energy reaches 75% of the total energy when the body has fallen 75% of the way, which occurs at a height of one-quarter of the original height.

## Final Result

* Total energy: $E = mgh$
* Velocity function: $v(y) = \sqrt{2g(h-y)}$
* Newton's Law comparison: Both yield $v^2 = 2g\Delta y$
* Specific height: $y = 0.25h$

## Interpretation



In free fall, the transformation of energy is perfectly linear with respect to height. Because potential energy depends linearly on $y$ ($U = mgy$), every meter descended converts a fixed amount of potential energy into kinetic energy. This explains why the "75% kinetic energy" mark occurs exactly at the point where 75% of the potential energy has been lost. Note that while energy is linear with height, velocity is not; the velocity increases following a square-root curve, meaning the body gains speed more rapidly at the beginning of the fall than at the end.