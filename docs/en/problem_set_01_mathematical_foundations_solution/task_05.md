# Task 05 – Trajectory curvature and normal acceleration

## Problem Statement

For an ellipse parameterized by:

$$
x = a\cos t, \qquad y = b\sin t
$$

The required operations are:
1. Determine the velocity vector $\vec v(t)$ and the acceleration vector $\vec a(t)$.
2. Determine the unit tangent vector to the trajectory $\hat T(t) = \frac{\vec v(t)}{|\vec v(t)|}$.
3. Decompose the acceleration into tangential and normal components, and determine the magnitude of the normal acceleration $a_n(t) = |\vec a_n(t)|$.
4. Determine the radius of curvature of the trajectory at point $t=0$ using the relation $a_n = \frac{v^2}{R}$.
5. Compare the result with the case of a circle $a=b$.

Finally, answer specific physical interpretation questions regarding trajectory curvature and normal acceleration.

## Theory

The velocity vector is the first derivative of the position vector with respect to time, and the acceleration vector is the second derivative.

The unit tangent vector $\hat T(t)$ indicates the instantaneous direction of motion and is obtained by normalizing the velocity vector:

$$
\hat T(t) = \frac{\vec v(t)}{|\vec v(t)|}
$$

The acceleration vector $\vec a$ can be decomposed into two orthogonal components:
1. **Tangential acceleration** ($\vec a_t$): Parallel to the velocity, responsible for the change in the *magnitude* of velocity (speed).
2. **Normal acceleration** ($\vec a_n$): Perpendicular to the velocity, responsible for the change in the *direction* of velocity.

The magnitude of the normal acceleration in two dimensions can be elegantly calculated using the cross product of velocity and acceleration. If we treat the 2D vectors as 3D vectors with a zero $z$-component, the normal acceleration magnitude is:

$$
a_n = \frac{|\vec v \times \vec a|}{|\vec v|}
$$

The radius of curvature $R$ at any point along the trajectory relates the normal acceleration and the square of the speed:

$$
R = \frac{|\vec v|^2}{a_n}
$$

## Step-by-Step Solution

### 1. Determine the velocity and acceleration vectors

We are given the position vector:

$$
\vec r(t) = 
\begin{pmatrix}
a\cos t \\
b\sin t
\end{pmatrix}
$$

Differentiate $\vec r(t)$ with respect to $t$ to find the velocity vector $\vec v(t)$:

$$
\vec v(t) = 
\begin{pmatrix}
\frac{d}{dt}(a\cos t) \\
\frac{d}{dt}(b\sin t)
\end{pmatrix}
$$

$$
\vec v(t) = 
\begin{pmatrix}
-a\sin t \\
b\cos t
\end{pmatrix}
$$

Differentiate $\vec v(t)$ with respect to $t$ to find the acceleration vector $\vec a(t)$:

$$
\vec a(t) = 
\begin{pmatrix}
\frac{d}{dt}(-a\sin t) \\
\frac{d}{dt}(b\cos t)
\end{pmatrix}
$$

$$
\vec a(t) = 
\begin{pmatrix}
-a\cos t \\
-b\sin t
\end{pmatrix}
$$

### 2. Determine the unit tangent vector $\hat T(t)$

First, calculate the magnitude of the velocity vector $|\vec v(t)|$:

$$
\begin{align}
|\vec v(t)| &= \sqrt{(-a\sin t)^2 + (b\cos t)^2} \\
            &= \sqrt{a^2\sin^2 t + b^2\cos^2 t}
\end{align}
$$

Now, divide the velocity vector by its magnitude to get the unit tangent vector:

$$
\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}
\begin{pmatrix}
-a\sin t \\
b\cos t
\end{pmatrix}
$$

### 3. Determine the magnitude of the normal acceleration $a_n(t)$

To find $a_n(t)$, we first compute the magnitude of the cross product $|\vec v \times \vec a|$ in 2D, which is equivalent to the determinant of the matrix formed by the components of $\vec v$ and $\vec a$:

$$
\begin{align}
|\vec v \times \vec a| &= |v_x a_y - v_y a_x| \\
                       &= |(-a\sin t)(-b\sin t) - (b\cos t)(-a\cos t)| \\
                       &= |ab\sin^2 t - (-ab\cos^2 t)| \\
                       &= |ab\sin^2 t + ab\cos^2 t|
\end{align}
$$

Factor out $ab$:

$$
\begin{align}
|\vec v \times \vec a| &= |ab(\sin^2 t + \cos^2 t)| \\
                       &= |ab(1)| \\
                       &= ab
\end{align}
$$

*(Assuming $a > 0$ and $b > 0$, the absolute value can be dropped).*

Now, use the formula for normal acceleration magnitude:

$$
a_n(t) = \frac{|\vec v \times \vec a|}{|\vec v|}
$$

$$
a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}
$$

### 4. Determine the radius of curvature $R$ at $t=0$

First, evaluate the magnitude of velocity at $t=0$:

$$
\begin{align}
|\vec v(0)| &= \sqrt{a^2\sin^2(0) + b^2\cos^2(0)} \\
            &= \sqrt{a^2(0) + b^2(1)} \\
            &= \sqrt{b^2} \\
            &= b
\end{align}
$$

Next, evaluate the magnitude of the normal acceleration at $t=0$:

$$
\begin{align}
a_n(0) &= \frac{ab}{\sqrt{a^2\sin^2(0) + b^2\cos^2(0)}} \\
       &= \frac{ab}{\sqrt{b^2}} \\
       &= \frac{ab}{b} \\
       &= a
\end{align}
$$

We are given the relation $a_n = \frac{v^2}{R}$. Rearranging this to solve for $R$ gives:

$$
R = \frac{v^2}{a_n}
$$

Substitute the values at $t=0$:

$$
\begin{align}
R(0) &= \frac{|\vec v(0)|^2}{a_n(0)} \\
     &= \frac{b^2}{a}
\end{align}
$$

### 5. Compare with the case of a circle ($a=b$)

If the ellipse is a circle, the semi-major and semi-minor axes are equal, so we set $a=b=r$, where $r$ is the radius of the circle.

Substitute $a=r$ and $b=r$ into our formula for $R(0)$:

$$
R(0) = \frac{r^2}{r} = r
$$

This matches the expected geometric property of a circle, which has a constant radius of curvature $r$ everywhere along its perimeter.

## Final Result

* Velocity: $\vec v(t) = (-a\sin t, b\cos t)$
* Acceleration: $\vec a(t) = (-a\cos t, -b\sin t)$
* Unit tangent vector: $\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)$
* Normal acceleration magnitude: $a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}$
* Radius of curvature at $t=0$: $R(0) = \frac{b^2}{a}$
* For a circle ($a=b$), the radius of curvature reduces to the circle's radius $R=a$.

## Interpretation

* **Does a greater trajectory curvature imply a greater normal acceleration?**
  Yes. Curvature $\kappa$ is defined as the inverse of the radius of curvature ($\kappa = 1/R$). Rearranging the relation $a_n = v^2/R$ yields $a_n = v^2 \kappa$. For a given instantaneous speed $v$, an increase in curvature $\kappa$ results in a directly proportional increase in normal acceleration.

* **Where on the ellipse is the trajectory more "curved": at the end of the major or minor semi-axis?**
  Assume $a > b$, making $a$ the semi-major axis (x-axis) and $b$ the semi-minor axis (y-axis). At $t=0$ (the end of the major axis), the radius of curvature is $R = b^2/a$. Because we divide a smaller number squared ($b^2$) by a larger number ($a$), $R$ is small, meaning the curvature is very high (sharp turn). Conversely, at $t=\pi/2$ (the end of the minor axis), a similar calculation yields $R = a^2/b$. Here, $R$ is large, meaning the curvature is low (gentle curve). Therefore, the trajectory is more "curved" at the end of the major semi-axis.

* **Explain why normal acceleration can be interpreted as the cause of the change in the direction of motion.**
  By decomposing acceleration into tangential and normal components, the tangential component $\vec a_t$ is strictly parallel to the velocity vector and therefore only affects its magnitude (the speed). The normal component $\vec a_n$ is strictly orthogonal to the velocity. In vector kinematics, adding a perpendicular change to a vector rotates it without immediately changing its length. Thus, the normal acceleration is solely responsible for bending the trajectory and changing the direction of the velocity vector over time.