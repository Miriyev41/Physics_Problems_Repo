# Task 05 – Trajectory Curvature and Normal Acceleration

## Problem Statement


For an ellipse parameterized by:

$$
x = a \cos t, \quad y = b \sin t
$$



1. Determine the velocity vector $\vec{v}(t)$ and the acceleration vector $\vec{a}(t)$.

2. Determine the unit tangent vector to the trajectory:

$$
\hat{T}(t) = \frac{\vec{v}(t)}{|\vec{v}(t)|}
$$

3. Decompose the acceleration into tangential and normal components:

$$
\vec{a}(t) = \vec{a}_t(t) + \vec{a}_n(t)
$$

and determine the magnitude of the normal acceleration $a_n(t) = |\vec{a}_n(t)|$.

4. Using the relation:

$$
a_n = \frac{v^2}{R}
$$

determine the radius of curvature $R$ of the trajectory at point $t=0$.

5. Compare the result with the case of a circle where $a = b$.

### Physical Interpretation

Answer the following questions:
* Does a greater trajectory curvature imply a greater normal acceleration?
* Where on the ellipse is the trajectory more "curved": at the end of the major or minor semi-axis?
* Explain why normal acceleration can be interpreted as the cause of the change in the direction of motion.

## Theory

The acceleration of a moving particle can be decomposed into two orthogonal components based on the local trajectory:
1. **Tangential acceleration** ($\vec a_t$): Parallel to the velocity vector, it describes the rate of change of the particle's *speed* (magnitude of velocity).
2. **Normal (centripetal) acceleration** ($\vec a_n$): Perpendicular to the velocity vector, it describes the rate of change of the particle's *direction*.

The magnitude of the normal acceleration is given by:

$$
a_n = \frac{|\vec v \times \vec a|}{|\vec v|}
$$

Alternatively, from purely kinematic principles, the normal acceleration is related to the speed $v = |\vec v|$ and the instantaneous radius of curvature $R$ by:

$$
a_n = \frac{v^2}{R}
$$

The curvature $\kappa$ is defined as $\frac{1}{R}$.

## Step-by-Step Solution

### 1. Velocity and acceleration vectors

The position vector is:

$$
\vec r(t) = (a\cos t, b\sin t)
$$

The velocity vector is the first derivative with respect to time:

$$
\vec v(t) = \left( \frac{d}{dt}(a\cos t), \frac{d}{dt}(b\sin t) \right) = (-a\sin t, b\cos t)
$$

The acceleration vector is the second derivative with respect to time (or the first derivative of velocity):

$$
\vec a(t) = \left( \frac{d}{dt}(-a\sin t), \frac{d}{dt}(b\cos t) \right) = (-a\cos t, -b\sin t)
$$

### 2. Unit tangent vector $\hat T(t)$

First, calculate the magnitude (speed) of the velocity vector:

$$
|\vec v(t)| = \sqrt{(-a\sin t)^2 + (b\cos t)^2} = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

The unit tangent vector is the velocity vector divided by its magnitude:

$$
\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)
$$

### 3. Normal acceleration magnitude $a_n(t)$

To find the normal acceleration without computing the full tangential vector projection, we can use the 2D cross-product magnitude formula. Treating our 2D vectors as 3D vectors with a zero $z$-component:

$$
\vec v = (-a\sin t, b\cos t, 0)
$$

$$
\vec a = (-a\cos t, -b\sin t, 0)
$$

The magnitude of their cross product is the absolute value of the determinant of their $xy$ components:

$$
\begin{align}
|\vec v \times \vec a| &= |(-a\sin t)(-b\sin t) - (b\cos t)(-a\cos t)| \\
                       &= |ab\sin^2 t + ab\cos^2 t| \\
                       &= |ab(\sin^2 t + \cos^2 t)| \\
                       &= ab
\end{align}
$$

*(Assuming $a > 0$ and $b > 0$, we can drop the absolute value).*

The normal acceleration magnitude is:

$$
a_n(t) = \frac{|\vec v \times \vec a|}{|\vec v(t)|} = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}
$$

### 4. Radius of curvature at $t=0$

At time $t=0$, the velocity magnitude (speed) is:

$$
v(0) = \sqrt{a^2\sin^2(0) + b^2\cos^2(0)} = \sqrt{0 + b^2} = b
$$

The normal acceleration at $t=0$ is:

$$
a_n(0) = \frac{ab}{\sqrt{a^2\sin^2(0) + b^2\cos^2(0)}} = \frac{ab}{b} = a
$$

Using the relation $a_n = \frac{v^2}{R}$, we solve for $R$:

$$
R = \frac{v^2}{a_n}
$$

Substitute the values at $t=0$:

$$
R(0) = \frac{b^2}{a}
$$

### 5. Comparison with a circle ($a=b$)

If the ellipse is a circle, then the semi-major and semi-minor axes are equal to the radius of the circle, let's call it $r$. So, $a = b = r$.

Substituting this into our radius of curvature formula at $t=0$:

$$
R(0) = \frac{r^2}{r} = r
$$

This matches exactly with our geometric intuition: the radius of curvature of a circle is constant and is simply equal to its radius $r$.

## Final Result

- **Velocity:** $\vec v(t) = (-a\sin t, b\cos t)$
- **Acceleration:** $\vec a(t) = (-a\cos t, -b\sin t)$
- **Unit Tangent:** $\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)$
- **Normal Acceleration Magnitude:** $a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}$
- **Radius of Curvature at $t=0$:** $R(0) = \frac{b^2}{a}$
- **Circle Case:** When $a=b=r$, the radius of curvature is simply $R=r$.

## Interpretation

### Does a greater trajectory curvature imply a greater normal acceleration?
Not necessarily on its own. The normal acceleration formula is $a_n = v^2 \kappa$ (where curvature $\kappa = 1/R$). While a greater curvature $\kappa$ increases $a_n$ proportionally, the normal acceleration is profoundly influenced by the square of the speed ($v^2$). A particle could navigate a very sharp curve (high curvature) with a low normal acceleration if it is moving extremely slowly. However, *for a constant speed*, a greater curvature strictly implies a greater normal acceleration.

### Where on the ellipse is the trajectory more "curved"?
Let's assume $a > b$, making $a$ the semi-major axis (x-axis) and $b$ the semi-minor axis (y-axis).
At $t=0$ (the end of the major axis), $R = \frac{b^2}{a}$. Since $b < a$, this value is relatively small.
At $t=\pi/2$ (the end of the minor axis), the roles of $a$ and $b$ swap in the formula, giving $R = \frac{a^2}{b}$, which is relatively large.
Since curvature is inversely proportional to the radius of curvature ($\kappa = 1/R$), a smaller $R$ means a larger curvature. Therefore, the trajectory is **most curved at the ends of the major semi-axis** (the "pointier" ends of the ellipse).

### Why normal acceleration is the cause of the change in direction
Velocity is a vector quantity, meaning it has both magnitude (speed) and direction. By definition, acceleration is the rate of change of the velocity vector. Any component of acceleration that acts parallel to the velocity vector can only stretch or shrink it, meaning it changes the speed (tangential acceleration). Conversely, any component of acceleration acting perpendicular to the velocity vector will rotate it without altering its length. Therefore, the normal component is exclusively responsible for turning the particle and changing its direction of motion.