# Task 02 – Projectile Motion

## Problem Statement

A body moves in the Earth's gravitational field without air resistance. Consider projectile motion with an initial velocity $v_0$ and an angle $\alpha$ relative to the horizontal. 

1. Derive the equations of motion in the horizontal and vertical directions.
2. Determine the time of flight.
3. Determine the maximum height.
4. Determine the range.
5. For what angle is the range maximum?
6. Prepare an animation of the trajectory for different $\alpha$.

## Theory

[Image of projectile motion trajectory with velocity components]

Projectile motion is a form of two-dimensional motion experienced by an object that is thrown near the Earth's surface and moves along a curved path under the action of gravity only. The key principle is the independence of motions in orthogonal directions:
- **Horizontal motion ($x$-axis):** In the absence of air resistance, there is no acceleration in the horizontal direction. Thus, the horizontal velocity component remains constant.
- **Vertical motion ($y$-axis):** The object experiences a constant downward acceleration due to gravity ($g \approx 9.81\ \text{m/s}^2$).

The initial velocity vector $\vec v_0$ can be decomposed into horizontal and vertical components using trigonometry:

$$
v_{0x} = v_0 \cos \alpha
$$

$$
v_{0y} = v_0 \sin \alpha
$$

## Step-by-Step Solution

### 1. Equations of motion

In the horizontal direction, acceleration $a_x = 0$. Using the kinematic equation for position:

$$
x(t) = x_0 + v_{0x} t + \frac{1}{2} a_x t^2
$$

Assuming the projectile starts at the origin ($x_0 = 0$, $y_0 = 0$), the horizontal position as a function of time is:

$$
x(t) = (v_0 \cos \alpha) t
$$

In the vertical direction, the acceleration is strictly due to gravity, so $a_y = -g$. The kinematic equation yields:

$$
y(t) = y_0 + v_{0y} t + \frac{1}{2} a_y t^2
$$

Substituting the initial conditions:

$$
y(t) = (v_0 \sin \alpha) t - \frac{1}{2} g t^2
$$

### 2. Time of flight

The time of flight $t_f$ is the total time the projectile remains in the air before hitting the ground. This occurs when the vertical position $y(t_f) = 0$ (for $t_f > 0$):

$$
0 = (v_0 \sin \alpha) t_f - \frac{1}{2} g t_f^2
$$

Factoring out $t_f$:

$$
t_f \left( v_0 \sin \alpha - \frac{1}{2} g t_f \right) = 0
$$

The non-zero solution gives the time of flight:

$$
\begin{align}
\frac{1}{2} g t_f &= v_0 \sin \alpha \\
t_f &= \frac{2 v_0 \sin \alpha}{g}
\end{align}
$$

### 3. Maximum height

The projectile reaches its maximum height when its vertical velocity $v_y(t)$ is zero. The vertical velocity equation is:

$$
v_y(t) = v_{0y} - gt = v_0 \sin \alpha - gt
$$

Set $v_y(t_h) = 0$ to find the time $t_h$ at which maximum height is reached:

$$
\begin{align}
v_0 \sin \alpha - g t_h &= 0 \\
t_h &= \frac{v_0 \sin \alpha}{g}
\end{align}
$$

Notice that $t_h = \frac{t_f}{2}$, meaning the time to reach the peak is exactly half the total flight time (due to the symmetry of the parabola).

Substitute $t_h$ into the vertical position equation $y(t)$ to find the maximum height $H$:

$$
\begin{align}
H &= y(t_h) \\
  &= (v_0 \sin \alpha) \left( \frac{v_0 \sin \alpha}{g} \right) - \frac{1}{2} g \left( \frac{v_0 \sin \alpha}{g} \right)^2 \\
  &= \frac{v_0^2 \sin^2 \alpha}{g} - \frac{v_0^2 \sin^2 \alpha}{2g} \\
  &= \frac{v_0^2 \sin^2 \alpha}{2g}
\end{align}
$$

### 4. Range

The range $R$ is the total horizontal distance traveled by the time the projectile hits the ground ($t = t_f$). Substitute $t_f$ into the horizontal position equation $x(t)$:

$$
\begin{align}
R &= x(t_f) \\
  &= (v_0 \cos \alpha) \left( \frac{2 v_0 \sin \alpha}{g} \right) \\
  &= \frac{v_0^2 (2 \sin \alpha \cos \alpha)}{g}
\end{align}
$$

Using the double-angle trigonometric identity $\sin(2\alpha) = 2 \sin \alpha \cos \alpha$, this simplifies to:

$$
R = \frac{v_0^2 \sin(2\alpha)}{g}
$$

### 5. Angle for maximum range

To find the angle $\alpha$ that maximizes the range $R$ for a given initial velocity $v_0$, we must maximize the function $\sin(2\alpha)$. The sine function reaches its maximum value of $1$ when its argument is $90^\circ$ (or $\frac{\pi}{2}$ radians):

$$
\begin{align}
\sin(2\alpha) &= 1 \\
2\alpha &= 90^\circ \\
\alpha &= 45^\circ
\end{align}
$$

## Final Result

- **Equations of motion:** $x(t) = (v_0 \cos \alpha) t$
  $y(t) = (v_0 \sin \alpha) t - \frac{1}{2} g t^2$
- **Time of flight:** $t_f = \frac{2 v_0 \sin \alpha}{g}$
- **Maximum height:** $H = \frac{v_0^2 \sin^2 \alpha}{2g}$
- **Range:** $R = \frac{v_0^2 \sin(2\alpha)}{g}$
- **Angle for maximum range:** $\alpha = 45^\circ$

## Interpretation

The derivation confirms that projectile motion traces a parabolic path. The horizontal and vertical motions are independent, coupled only by the variable of time. The angle $\alpha = 45^\circ$ provides the optimal trade-off between keeping the projectile in the air long enough (which requires a larger vertical velocity component) and moving it horizontally fast enough (which requires a larger horizontal velocity component) to maximize the total range on flat ground. Additionally, the range equation reveals that complementary angles (e.g., $30^\circ$ and $60^\circ$) yield the exact same range, although their trajectories and flight times differ.