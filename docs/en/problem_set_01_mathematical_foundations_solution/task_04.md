# Task 04 – Geometry of parametric curves

## Problem Statement

Investigate the following parametric curves:
A) $x(t) = R\cos t, \quad y(t) = R\sin t$
B) $x(t) = a\cos t, \quad y(t) = b\sin t$
C) $x(t) = t, \quad y(t) = t^2$
D) $x(t) = \cosh t, \quad y(t) = \sinh t$

For each curve, eliminate the parameter (if possible), determine the type of curve, find the velocity $\vec v(t)$ and acceleration $\vec a(t)$, and check if their magnitudes are constant.

## Theory

A parametric curve in two dimensions describes the coordinates $(x,y)$ as functions of a parameter $t$, often representing time. Eliminating $t$ yields the implicit Cartesian equation of the trajectory $f(x,y) = 0$. 

The velocity and acceleration are the first and second time derivatives of the position vector $\vec r(t) = (x(t), y(t))$. A constant velocity magnitude indicates uniform motion, whereas a constant acceleration magnitude implies the net force has a constant magnitude.

## Step-by-Step Solution

### Curve A

Eliminate the parameter using the Pythagorean trigonometric identity.

$$
x^2 + y^2 = R^2\cos^2 t + R^2\sin^2 t
$$

$$
x^2 + y^2 = R^2(\cos^2 t + \sin^2 t)
$$

$$
x^2 + y^2 = R^2
$$

This represents a circle of radius $R$.

Calculate velocity and acceleration.

$$
\vec v(t) = \left( \frac{d}{dt}(R\cos t), \frac{d}{dt}(R\sin t) \right)
$$

$$
\vec v(t) = (-R\sin t, R\cos t)
$$

$$
\vec a(t) = (-R\cos t, -R\sin t)
$$

Calculate their magnitudes.

$$
|\vec v(t)| = \sqrt{(-R\sin t)^2 + (R\cos t)^2}
$$

$$
|\vec v(t)| = \sqrt{R^2(\sin^2 t + \cos^2 t)}
$$

$$
|\vec v(t)| = R
$$

$$
|\vec a(t)| = \sqrt{(-R\cos t)^2 + (-R\sin t)^2}
$$

$$
|\vec a(t)| = R
$$

Both magnitudes are constant.

### Curve B

Eliminate the parameter using the same identity, first isolating the trigonometric functions.

$$
\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = \cos^2 t + \sin^2 t
$$

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

This represents an ellipse with semi-axes $a$ and $b$.

Calculate kinematics.

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

Calculate magnitudes.

$$
|\vec v(t)| = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

$$
|\vec a(t)| = \sqrt{a^2\cos^2 t + b^2\sin^2 t}
$$

Neither magnitude is constant unless $a = b$ (which reduces to the circle case).

### Curve C

Eliminate the parameter by substituting $t = x$ into the equation for $y$.

$$
y = x^2
$$

This represents a parabola.

Calculate kinematics.

$$
\vec v(t) = (1, 2t)
$$

$$
\vec a(t) = (0, 2)
$$

Calculate magnitudes.

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2}
$$

$$
|\vec v(t)| = \sqrt{1 + 4t^2}
$$

$$
|\vec a(t)| = \sqrt{0^2 + 2^2}
$$

$$
|\vec a(t)| = 2
$$

The magnitude of velocity is not constant, but the magnitude of acceleration is constant.

### Curve D

Eliminate the parameter using the hyperbolic identity $\cosh^2 t - \sinh^2 t = 1$.

$$
x^2 - y^2 = \cosh^2 t - \sinh^2 t
$$

$$
x^2 - y^2 = 1
$$

This represents a hyperbola (specifically, the right branch since $x = \cosh t \ge 1$).

Calculate kinematics.

$$
\vec v(t) = (\sinh t, \cosh t)
$$

$$
\vec a(t) = (\cosh t, \sinh t)
$$

Calculate magnitudes.

$$
|\vec v(t)| = \sqrt{\sinh^2 t + \cosh^2 t}
$$

$$
|\vec v(t)| = \sqrt{\cosh(2t)}
$$

$$
|\vec a(t)| = \sqrt{\cosh^2 t + \sinh^2 t}
$$

$$
|\vec a(t)| = \sqrt{\cosh(2t)}
$$

Neither magnitude is constant.

## Final Result

* **Curve A (Circle):** $x^2 + y^2 = R^2$. Both $|\vec v| = R$ and $|\vec a| = R$ are constant.
* **Curve B (Ellipse):** $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$. Neither $|\vec v|$ nor $|\vec a|$ is constant (unless $a=b$).
* **Curve C (Parabola):** $y = x^2$. $|\vec v|$ is not constant; $|\vec a| = 2$ is constant.
* **Curve D (Hyperbola):** $x^2 - y^2 = 1$. Neither $|\vec v|$ nor $|\vec a|$ is constant.

## Interpretation

The condition of constant acceleration magnitude in Curve C corresponds to projectile motion under uniform gravity, where the horizontal velocity is constant and the vertical velocity grows linearly. For the trigonometric parameterizations, circular motion maintains uniform speed and constant centripetal force magnitude, whereas elliptical motion requires variable speed to conserve angular momentum, resulting in variable acceleration.