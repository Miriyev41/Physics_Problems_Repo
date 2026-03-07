# Task 05 – Momentum and One-Dimensional Head-on Collision

## Problem Statement

Two bodies with masses $m_1, m_2$ move along a single straight line. The collision is elastic.

* Write down the principles of conservation of momentum and energy.
* Determine the velocities after the collision.
* Consider the case $m_1 = m_2$.
* Consider the limit $m_2 \gg m_1$.
* Interpret the results physically.

## Theory

In a one-dimensional elastic collision, two fundamental conservation laws apply:
1.  **Conservation of Linear Momentum:** The total momentum of the system remains constant if no external forces act on it.
2.  **Conservation of Kinetic Energy:** In an elastic collision, the total kinetic energy is conserved, meaning no energy is dissipated as heat or sound.

Let $u_1, u_2$ be the initial velocities and $v_1, v_2$ be the final velocities.



## Step-by-Step Solution

### 1. Conservation Equations

**Momentum:**

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2
$$

**Kinetic Energy:**

$$
\frac{1}{2} m_1 u_1^2 + \frac{1}{2} m_2 u_2^2 = \frac{1}{2} m_1 v_1^2 + \frac{1}{2} m_2 v_2^2
$$

### 2. Solving for Final Velocities

Rearranging the momentum equation:

$$
m_1(u_1 - v_1) = m_2(v_2 - u_2)
$$

Rearranging the energy equation (using $a^2 - b^2 = (a-b)(a+b)$):

$$
m_1(u_1 - v_1)(u_1 + v_1) = m_2(v_2 - u_2)(v_2 + u_2)
$$

Dividing the energy result by the momentum result yields the velocity relationship:

$$
u_1 + v_1 = v_2 + u_2 \implies v_2 - v_1 = u_1 - u_2
$$

Combining this with the momentum equation leads to the general solutions:

$$
v_1 = \frac{m_1 - m_2}{m_1 + m_2}u_1 + \frac{2m_2}{m_1 + m_2}u_2
$$

$$
v_2 = \frac{2m_1}{m_1 + m_2}u_1 + \frac{m_2 - m_1}{m_1 + m_2}u_2
$$

### 3. Case: $m_1 = m_2$

If the masses are equal, the coefficients simplify significantly:

$$
v_1 = \frac{0}{2m}u_1 + \frac{2m}{2m}u_2 = u_2
$$

$$
v_2 = \frac{2m}{2m}u_1 + \frac{0}{2m}u_2 = u_1
$$

### 4. Limit: $m_2 \gg m_1$ (Stationary Target $u_2 = 0$)

If the second mass is much larger (like a ball hitting a wall):

$$
v_1 \approx \frac{-m_2}{m_2}u_1 = -u_1
$$

$$
v_2 \approx \frac{2m_1}{m_2}u_1 \approx 0
$$

## Final Result

* **General Velocities**: 
  $v_1 = \frac{(m_1-m_2)u_1 + 2m_2u_2}{m_1+m_2}$
  $v_2 = \frac{2m_1u_1 + (m_2-m_1)u_2}{m_1+m_2}$
* **Equal Masses**: The bodies exchange velocities.
* **Massive Target**: The light body bounces back with the same speed; the heavy body remains nearly stationary.

## Interpretation

The case of equal masses shows a perfect "transfer" of state, common in billiards. The limit $m_2 \gg m_1$ illustrates why a light object cannot significantly move a much heavier one; instead, the momentum of the light object is reversed, resulting in a nearly $2u_1$ change in velocity, while the heavy object absorbs the momentum with negligible speed change.