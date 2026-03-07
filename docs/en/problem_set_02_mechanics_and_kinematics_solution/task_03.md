# Task 03 – Elimination of Time and Interpretation of Acceleration

## Problem Statement

The path equation of a particle is given in parametric form:

$$
x(t) = 2t^2, \qquad y(t) = 3t^3
$$

* Eliminate the parameter $t$ to find the Cartesian trajectory.
* Draw the trajectory (qualitative description).
* Calculate $\vec{v}(t)$, $|\vec{v}(t)|$, $\vec{a}(t)$, and $|\vec{a}(t)|$.
* Determine if the acceleration is constant.

## Theory

Parametric equations describe the coordinates of a particle as functions of time. To find the path (trajectory) in Cartesian space, one must isolate $t$ in one equation and substitute it into the others.

The kinematic vectors are derived as follows:

1.  **Velocity vector**: $\vec{v}(t) = \frac{d\vec{r}}{dt} = (\dot{x}, \dot{y})$
2.  **Acceleration vector**: $\vec{a}(t) = \frac{d\vec{v}}{dt} = (\ddot{x}, \ddot{y})$
3.  **Magnitude (Scalar)**: $|\vec{A}| = \sqrt{A_x^2 + A_y^2}$

## Step-by-Step Solution

### 1. Elimination of Parameter $t$

From the expression for $x(t)$:

$$
x = 2t^2 \implies t^2 = \frac{x}{2} \implies t = \left( \frac{x}{2} \right)^{1/2}
$$

Substitute this expression for $t$ into the equation for $y(t)$:

$$
y = 3t^3 = 3 \left[ \left( \frac{x}{2} \right)^{1/2} \right]^3
$$

The Cartesian path equation is:

$$
y(x) = 3 \left( \frac{x}{2} \right)^{3/2}
$$

### 2. Trajectory Description

Since $x \propto t^2$, the particle only exists for $x \ge 0$. The relationship $y \propto x^{3/2}$ describes a semi-cubical parabola. The curve starts at the origin $(0,0)$ and rises with an increasing slope as $x$ increases.

### 3. Velocity and Acceleration Vectors

**Velocity components:**

$$
v_x(t) = \frac{dx}{dt} = 4t
$$

$$
v_y(t) = \frac{dy}{dt} = 9t^2
$$

**Velocity vector and magnitude:**

$$
\vec{v}(t) = \begin{pmatrix} 4t \\ 9t^2 \end{pmatrix}
$$

$$
|\vec{v}(t)| = \sqrt{(4t)^2 + (9t^2)^2} = \sqrt{16t^2 + 81t^4} = t\sqrt{16 + 81t^2}
$$

**Acceleration components:**

$$
a_x(t) = \frac{dv_x}{dt} = 4
$$

$$
a_y(t) = \frac{dv_y}{dt} = 18t
$$

**Acceleration vector and magnitude:**

$$
\vec{a}(t) = \begin{pmatrix} 4 \\ 18t \end{pmatrix}
$$

$$
|\vec{a}(t)| = \sqrt{4^2 + (18t)^2} = \sqrt{16 + 324t^2} = 2\sqrt{4 + 81t^2}
$$

### 4. Analysis of Acceleration

To determine if the acceleration is constant, we examine $\vec{a}(t)$. For an acceleration to be constant, all its components must be independent of time.

While $a_x = 4$ is constant, the vertical component $a_y = 18t$ is a linear function of time.

## Final Result

* **Cartesian Equation**: $y = \frac{3}{(2)^{3/2}} x^{3/2}$
* **Velocity**: $\vec{v}(t) = (4t, 9t^2)$
* **Acceleration**: $\vec{a}(t) = (4, 18t)$
* **Magnitude of Acceleration**: $|\vec{a}(t)| = 2\sqrt{4 + 81t^2}$

## Interpretation

The acceleration is **not constant**. Although the force (and thus acceleration) in the $x$-direction is steady, there is a time-dependent increasing force acting in the $y$-direction. This causes the particle to "curve" more sharply upward over time, leading to the non-linear trajectory observed in the path equation.