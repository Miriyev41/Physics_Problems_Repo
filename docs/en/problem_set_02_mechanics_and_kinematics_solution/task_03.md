# Task 03 – Elimination of time and interpretation of acceleration

## Problem Statement

The path equation of a particle is given in parametric form:

$$
x(t) = 2t^2, \qquad y(t) = 3t^3
$$

The required operations are:
1. Eliminate the parameter $t$ to find the Cartesian equation of the trajectory.
2. Determine the velocity vector $\vec v(t)$ and its magnitude $|\vec v(t)|$.
3. Determine the acceleration vector $\vec a(t)$ and its magnitude $|\vec a(t)|$.
4. Determine if the acceleration is constant.

## Theory

To eliminate the parameter $t$, we express $t$ as a function of one coordinate (usually $x$) and substitute it into the other coordinate equation ($y$). This results in a direct relationship $y = f(x)$ that describes the geometric shape of the path in the $xy$-plane.

The velocity vector is the time derivative of the position vector:

$$
\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

The acceleration vector is the time derivative of the velocity vector:

$$
\vec a(t) = \left( \frac{dv_x}{dt}, \frac{dv_y}{dt} \right)
$$

The magnitude of any vector $\vec u = (u_x, u_y)$ is calculated using the Euclidean norm:

$$
|\vec u| = \sqrt{u_x^2 + u_y^2}
$$

An acceleration is considered constant only if both its magnitude and its direction do not change with time. If any component of $\vec a(t)$ depends on $t$, the acceleration is non-uniform.

## Step-by-Step Solution

### 1. Eliminate the parameter $t$

**Step 1: Express $t$ in terms of $x$**

From the equation $x = 2t^2$:

$$
t^2 = \frac{x}{2}
$$

Taking the square root (considering $t \geq 0$):

$$
t = \sqrt{\frac{x}{2}}
$$

**Step 2: Substitute into the equation for $y$**

Substitute $t = \left(\frac{x}{2}\right)^{1/2}$ into $y = 3t^3$:

$$
\begin{align}
y &= 3 \left( \sqrt{\frac{x}{2}} \right)^3 \\
  &= 3 \left( \frac{x}{2} \right)^{3/2}
\end{align}
$$

This can also be written as:

$$
y = \frac{3}{2\sqrt{2}} x\sqrt{x}
$$

### 2. Calculate velocity $\vec v(t)$ and magnitude $|\vec v(t)|$

**Step 1: Compute velocity components**

Differentiate $x(t) = 2t^2$:

$$
v_x(t) = \frac{d}{dt}(2t^2) = 4t
$$

Differentiate $y(t) = 3t^3$:

$$
v_y(t) = \frac{d}{dt}(3t^3) = 9t^2
$$

The velocity vector is:

$$
\vec v(t) = (4t, 9t^2)
$$

**Step 2: Compute the magnitude $|\vec v(t)|$**

$$
\begin{align}
|\vec v(t)| &= \sqrt{(4t)^2 + (9t^2)^2} \\
            &= \sqrt{16t^2 + 81t^4}
\end{align}
$$

Factoring out $t^2$:

$$
|\vec v(t)| = t\sqrt{16 + 81t^2}
$$

### 3. Calculate acceleration $\vec a(t)$ and magnitude $|\vec a(t)|$

**Step 1: Compute acceleration components**

Differentiate $v_x(t) = 4t$:

$$
a_x(t) = \frac{d}{dt}(4t) = 4
$$

Differentiate $v_y(t) = 9t^2$:

$$
a_y(t) = \frac{d}{dt}(9t^2) = 18t
$$

The acceleration vector is:

$$
\vec a(t) = (4, 18t)
$$

**Step 2: Compute the magnitude $|\vec a(t)|$**

$$
\begin{align}
|\vec a(t)| &= \sqrt{4^2 + (18t)^2} \\
            &= \sqrt{16 + 324t^2}
\end{align}
$$

### 4. Is the acceleration constant?

An acceleration is constant if and only if $\frac{d\vec a}{dt} = \vec 0$.

Looking at the components:
- $a_x = 4$ (constant)
- $a_y = 18t$ (depends on $t$)

Since the $y$-component of the acceleration increases linearly with time, the vector $\vec a(t)$ changes both its magnitude and its direction as time progresses.

**Conclusion: The acceleration is NOT constant.**

## Final Result

* Cartesian equation: $y = 3 \left( \frac{x}{2} \right)^{3/2}$
* Velocity vector: $\vec v(t) = (4t, 9t^2)$
* Velocity magnitude: $|\vec v(t)| = \sqrt{16t^2 + 81t^4}$
* Acceleration vector: $\vec a(t) = (4, 18t)$
* Acceleration magnitude: $|\vec a(t)| = \sqrt{16 + 324t^2}$
* Acceleration is not constant.

## Interpretation



The trajectory described by $y \propto x^{3/2}$ is known as a semi-cubic parabola. Unlike standard projectile motion where acceleration is a constant vector (gravity), the particle in this task experiences a constant force in the $x$-direction and a time-dependent increasing force in the $y$-direction. This causes the particle to "curve" more sharply upward as time increases, which is reflected in the non-constant acceleration vector. The speed of the particle grows rapidly because both components of the velocity are increasing functions of time.