# Task 03 – Elimination of time and interpretation of acceleration

## Problem Statement

The path equation is given in parametric form:

$$
x(t)=2t^2, \qquad y(t)=3t^3
$$

1. Eliminate the parameter $t$.
2. Draw the trajectory.
3. Calculate $\vec v(t)$, $|\vec v(t)|$, $\vec a(t)$ and $|\vec a(t)|$.
4. Is the acceleration constant?

## Theory

A trajectory described by parametric equations defines the coordinates $x$ and $y$ as functions of time $t$. Eliminating the parameter $t$ gives the implicit equation of the curve $f(x, y) = 0$, which describes the path solely in the spatial domain.

The velocity vector is the first derivative of the position vector with respect to time, and the acceleration vector is the first derivative of the velocity vector (or the second derivative of the position vector). If any component of the acceleration vector depends on time, the acceleration is not constant.

## Step-by-Step Solution

### 1. Elimination of the parameter $t$

Given the equations:

$$
x = 2t^2 \implies t^2 = \frac{x}{2}
$$

Since $t^2 \ge 0$, we must have $x \ge 0$. To find $y$ in terms of $x$, it is easier to match the powers of $t$. We know that $t^6 = (t^2)^3 = (t^3)^2$.

Let us cube the $x$ equation and square the $y$ equation:

$$
x^3 = (2t^2)^3 = 8t^6
$$

$$
y^2 = (3t^3)^2 = 9t^6
$$

From the first equation, substitute $t^6 = \frac{x^3}{8}$ into the second equation:

$$
\begin{align}
y^2 &= 9 \left( \frac{x^3}{8} \right) \\
y^2 &= \frac{9}{8} x^3
\end{align}
$$

Taking the square root (assuming $t \ge 0 \implies y \ge 0$), the explicit function is:

$$
y = \sqrt{\frac{9}{8} x^3} = \frac{3}{2\sqrt{2}} x^{3/2}
$$

This curve is known as a semi-cubical parabola.

### 2. Calculation of velocity and its magnitude

The position vector is:

$$
\vec r(t) = (2t^2, 3t^3)
$$

The velocity vector is the derivative of position:

$$
\begin{align}
\vec v(t) &= \left( \frac{d}{dt}(2t^2), \frac{d}{dt}(3t^3) \right) \\
          &= (4t, 9t^2)
\end{align}
$$

The magnitude (speed) is:

$$
\begin{align}
|\vec v(t)| &= \sqrt{(4t)^2 + (9t^2)^2} \\
            &= \sqrt{16t^2 + 81t^4} \\
            &= t \sqrt{16 + 81t^2}
\end{align}
$$
*(Assuming $t \ge 0$)*.

### 3. Calculation of acceleration and its magnitude

The acceleration vector is the derivative of velocity:

$$
\begin{align}
\vec a(t) &= \left( \frac{d}{dt}(4t), \frac{d}{dt}(9t^2) \right) \\
          &= (4, 18t)
\end{align}
$$

The magnitude of the acceleration is:

$$
\begin{align}
|\vec a(t)| &= \sqrt{4^2 + (18t)^2} \\
            &= \sqrt{16 + 324t^2} \\
            &= 2 \sqrt{4 + 81t^2}
\end{align}
$$

### 4. Is the acceleration constant?

No, the acceleration is **not constant**. 

While the horizontal component $a_x = 4$ is constant, the vertical component $a_y = 18t$ explicitly depends on time. Consequently, both the direction and the magnitude $|\vec a(t)| = 2\sqrt{4 + 81t^2}$ of the acceleration vector change as time progresses.

## Final Result

- **Implicit equation:** $y^2 = \frac{9}{8} x^3$
- **Velocity:** $\vec v(t) = (4t, 9t^2)$
- **Speed:** $|\vec v(t)| = t \sqrt{16 + 81t^2}$
- **Acceleration:** $\vec a(t) = (4, 18t)$
- **Acceleration Magnitude:** $|\vec a(t)| = 2 \sqrt{4 + 81t^2}$
- **Constancy:** The acceleration is **not constant** because its $y$-component and magnitude depend on $t$.

## Interpretation

The motion begins from rest at the origin since $\vec v(0) = (0,0)$. However, there is an initial non-zero horizontal acceleration $\vec a(0) = (4,0)$, which kicks the particle along the $x$-axis. As time increases, the vertical acceleration $18t$ grows linearly, meaning the particle is pulled increasingly stronger in the positive $y$-direction. This explains the characteristic shape of the semi-cubical parabola $y \propto x^{3/2}$, which curves upwards progressively steeper as $x$ increases.