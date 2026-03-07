# Task 02 – Projectile Motion

## Problem Statement

A body moves in the Earth's gravitational field without air resistance. Consider projectile motion with an initial velocity $v_0$ and an angle $\alpha$ relative to the horizontal.

* Derive the equations of motion in the horizontal and vertical directions.
* Determine the time of flight.
* Determine the maximum height.
* Determine the range.
* For what angle is the range maximum?
* Prepare an animation of the trajectory for different $\alpha$.

## Theory

Projectile motion is a two-dimensional motion under the influence of constant gravity $g$. By neglecting air resistance, the motion can be decomposed into two independent components:
1.  **Horizontal (x-axis):** Uniform motion with constant velocity (zero acceleration).
2.  **Vertical (y-axis):** Uniformly accelerated motion due to gravity.

The initial velocity components are:

$$
v_{0x} = v_0 \cos(\alpha)
$$

$$
v_{0y} = v_0 \sin(\alpha)
$$



## Step-by-Step Solution

### 1. Deriving Equations of Motion

Applying Newton's second law ($a_x = 0$ and $a_y = -g$):

**Horizontal Position:**

$$
x(t) = v_0 \cos(\alpha) t
$$

**Vertical Position:**

$$
y(t) = v_0 \sin(\alpha) t - \frac{1}{2} g t^2
$$

### 2. Time of Flight ($T$)

The body returns to the ground when $y(T) = 0$.

$$
0 = v_0 \sin(\alpha) T - \frac{1}{2} g T^2
$$

Factoring out $T$:

$$
T \left( v_0 \sin(\alpha) - \frac{1}{2} g T \right) = 0
$$

The non-zero solution is:

$$
T = \frac{2 v_0 \sin(\alpha)}{g}
$$

### 3. Maximum Height ($H$)

The maximum height occurs when the vertical velocity $v_y(t) = 0$.

$$
v_y(t) = v_0 \sin(\alpha) - gt = 0 \implies t_h = \frac{v_0 \sin(\alpha)}{g}
$$

Substituting $t_h$ into the $y(t)$ equation:

$$
H = y(t_h) = v_0 \sin(\alpha) \left( \frac{v_0 \sin(\alpha)}{g} \right) - \frac{1}{2} g \left( \frac{v_0 \sin(\alpha)}{g} \right)^2
$$

$$
H = \frac{v_0^2 \sin^2(\alpha)}{2g}
$$

### 4. Range ($R$)

The range is the horizontal distance traveled at time $T$:

$$
R = x(T) = v_0 \cos(\alpha) \left( \frac{2 v_0 \sin(\alpha)}{g} \right)
$$

Using the trigonometric identity $2 \sin(\alpha) \cos(\alpha) = \sin(2\alpha)$:

$$
R = \frac{v_0^2 \sin(2\alpha)}{g}
$$

### 5. Angle for Maximum Range

The range $R$ is maximized when $\sin(2\alpha)$ is maximum. The maximum value of the sine function is 1.

$$
\sin(2\alpha) = 1 \implies 2\alpha = 90^\circ \implies \alpha = 45^\circ
$$

## Final Result

* **Time of Flight:** $T = \frac{2 v_0 \sin(\alpha)}{g}$
* **Maximum Height:** $H = \frac{v_0^2 \sin^2(\alpha)}{2g}$
* **Range:** $R = \frac{v_0^2 \sin(2\alpha)}{g}$
* **Optimal Angle:** $\alpha = 45^\circ$

## Interpretation

The trajectory is a parabola. The time of flight and maximum height depend only on the vertical component of the initial velocity, while the range depends on both components. Increasing $\alpha$ increases height and flight time, but the range is a trade-off between time in the air and horizontal speed.