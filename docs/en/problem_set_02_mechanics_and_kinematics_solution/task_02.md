# Task 02 – Projectile motion

## Problem Statement

A body moves in the Earth's gravitational field without air resistance. Consider projectile motion with an initial velocity $v_0$ and an launch angle $\alpha$ relative to the horizontal.

The required operations are:
1. Derive the equations of motion in the horizontal and vertical directions.
2. Determine the time of flight $t_f$.
3. Determine the maximum height $H$.
4. Determine the horizontal range $R$.
5. Determine the angle $\alpha$ for which the range is maximum.
6. Prepare an animation of the trajectory for different angles $\alpha$.

## Theory

Projectile motion is a case of two-dimensional motion under constant acceleration. Since gravity acts only vertically, the motion can be decomposed into two independent components:
1. **Horizontal component ($x$):** Uniform motion (zero acceleration).
2. **Vertical component ($y$):** Uniformly accelerated motion (acceleration due to gravity $g$).

The initial velocity vector $\vec v_0$ is decomposed using trigonometric functions:

$$
v_{0x} = v_0 \cos \alpha, \qquad v_{0y} = v_0 \sin \alpha
$$

The equations for position and velocity are derived by integrating the constant acceleration vector $\vec a = (0, -g)$.

## Step-by-Step Solution

### 1. Derive the equations of motion

**Horizontal direction ($x$):**
Acceleration $a_x = 0$. Integrating once gives constant velocity:

$$
v_x(t) = v_0 \cos \alpha
$$

Integrating again gives position (assuming $x_0 = 0$):

$$
x(t) = (v_0 \cos \alpha)t
$$

**Vertical direction ($y$):**
Acceleration $a_y = -g$. Integrating once gives velocity:

$$
v_y(t) = v_0 \sin \alpha - gt
$$

Integrating again gives position (assuming $y_0 = 0$):

$$
y(t) = (v_0 \sin \alpha)t - \frac{1}{2}gt^2
$$

### 2. Determine the time of flight $t_f$

The body returns to the ground when $y(t) = 0$:

$$
0 = (v_0 \sin \alpha)t_f - \frac{1}{2}gt_f^2
$$

Factoring out $t_f$ (where $t_f \neq 0$):

$$
\begin{align}
0 &= t_f \left( v_0 \sin \alpha - \frac{1}{2}gt_f \right) \\
\frac{1}{2}gt_f &= v_0 \sin \alpha \\
t_f &= \frac{2v_0 \sin \alpha}{g}
\end{align}
$$

### 3. Determine the maximum height $H$

Maximum height is reached when the vertical velocity is zero ($v_y = 0$). Let this time be $t_h$:

$$
\begin{align}
0 &= v_0 \sin \alpha - gt_h \\
t_h &= \frac{v_0 \sin \alpha}{g}
\end{align}
$$

Substitute $t_h$ into the $y(t)$ equation:

$$
\begin{align}
H &= (v_0 \sin \alpha) \left( \frac{v_0 \sin \alpha}{g} \right) - \frac{1}{2}g \left( \frac{v_0 \sin \alpha}{g} \right)^2 \\
  &= \frac{v_0^2 \sin^2 \alpha}{g} - \frac{v_0^2 \sin^2 \alpha}{2g} \\
  &= \frac{v_0^2 \sin^2 \alpha}{2g}
\end{align}
$$

### 4. Determine the range $R$

The range is the horizontal distance traveled during the total time of flight $t_f$:

$$
\begin{align}
R &= x(t_f) \\
  &= (v_0 \cos \alpha) \left( \frac{2v_0 \sin \alpha}{g} \right) \\
  &= \frac{v_0^2 (2 \sin \alpha \cos \alpha)}{g}
\end{align}
$$

Using the double-angle identity $2 \sin \alpha \cos \alpha = \sin(2\alpha)$:

$$
R = \frac{v_0^2 \sin(2\alpha)}{g}
$$

### 5. Angle for maximum range

The range $R$ is maximized when $\sin(2\alpha)$ is at its maximum value of $1$:

$$
\begin{align}
\sin(2\alpha) &= 1 \\
2\alpha &= 90^\circ \\
\alpha &= 45^\circ
\end{align}
$$

## Final Result

* Equations of motion: $x(t) = v_0 \cos(\alpha)t$, $y(t) = v_0 \sin(\alpha)t - \frac{1}{2}gt^2$
* Time of flight: $t_f = \frac{2v_0 \sin \alpha}{g}$
* Maximum height: $H = \frac{v_0^2 \sin^2 \alpha}{2g}$
* Range: $R = \frac{v_0^2 \sin(2\alpha)}{g}$
* Max range angle: $\alpha = 45^\circ$

## Interpretation

[Image of projectile motion trajectories for different launch angles]

The parabolic path of a projectile is a result of the competition between constant horizontal inertia and vertical gravitational acceleration. The time of flight and maximum height are determined solely by the vertical component of the initial velocity ($v_0 \sin \alpha$), while the range depends on the product of both horizontal and vertical components. At $45^\circ$, there is a perfect balance between the time spent in the air and the horizontal speed, leading to the furthest travel distance. For any other range (less than the maximum), there exist two complementary angles ($\alpha$ and $90^\circ - \alpha$) that will result in the same landing point, though with different heights and flight times.