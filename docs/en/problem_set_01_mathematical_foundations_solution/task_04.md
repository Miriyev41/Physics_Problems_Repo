# Task 04 – Geometry of parametric curves

## Problem Statement

Investigate the following curves given by their parametric equations:

A) $x(t) = R\cos t, \quad y(t) = R\sin t$

B) $x(t) = a\cos t, \quad y(t) = b\sin t$

C) $x(t) = t, \quad y(t) = t^2$

D) $x(t) = \cosh t, \quad y(t) = \sinh t$

For each curve, the required operations are:
1. Eliminate the parameter (if possible).
2. Determine the type of curve.
3. Determine the velocity $\vec v(t)$ and acceleration $\vec a(t)$.
4. Check if the velocity/acceleration has a constant magnitude ($|\vec v| = \text{const}$ or $|\vec a| = \text{const}$).

## Theory

A parametric curve in two dimensions is defined by a position vector $\vec r(t) = \bigl(x(t), y(t)\bigr)$. 

Eliminating the parameter $t$ means finding an algebraic relationship between $x$ and $y$ that does not depend on $t$. This is often achieved using substitution or fundamental identities, such as the Pythagorean trigonometric identity:

$$
\cos^2 t + \sin^2 t = 1
$$

or the fundamental hyperbolic identity:

$$
\cosh^2 t - \sinh^2 t = 1
$$

The velocity vector is the first derivative of the position vector with respect to time:

$$
\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

The acceleration vector is the second derivative of the position vector, or the first derivative of the velocity vector:

$$
\vec a(t) = \left( \frac{d^2x}{dt^2}, \frac{d^2y}{dt^2} \right)
$$

The magnitude of any vector $\vec u = (u_x, u_y)$ is given by the Euclidean norm:

$$
|\vec u| = \sqrt{u_x^2 + u_y^2}
$$

A vector has a constant magnitude if its length does not depend on the parameter $t$.

## Step-by-Step Solution

### Curve A: $\ x(t) = R\cos t,\quad  y(t) = R\sin t$

#### 1. Eliminate the parameter
Square both $x(t)$ and $y(t)$:

$$
x^2 = R^2 \cos^2 t
$$

$$
y^2 = R^2 \sin^2 t
$$

Add the two equations together:

$$
\begin{align}
x^2 + y^2 &= R^2 \cos^2 t + R^2 \sin^2 t \\
          &= R^2 (\cos^2 t + \sin^2 t)
\end{align}
$$

Using the identity $\cos^2 t + \sin^2 t = 1$, we get:

$$
x^2 + y^2 = R^2
$$

#### 2. Determine the type of curve
The equation $x^2 + y^2 = R^2$ describes a **circle** centered at the origin $(0,0)$ with radius $R$.

#### 3. Determine velocity and acceleration
Differentiate $x(t)$ and $y(t)$ to find velocity:

$$
v_x(t) = \frac{d}{dt}(R\cos t) = -R\sin t
$$

$$
v_y(t) = \frac{d}{dt}(R\sin t) = R\cos t
$$

$$
\vec v(t) = \bigl(-R\sin t, R\cos t\bigr)
$$

Differentiate velocity to find acceleration:

$$
a_x(t) = \frac{d}{dt}(-R\sin t) = -R\cos t
$$

$$
a_y(t) = \frac{d}{dt}(R\cos t) = -R\sin t
$$

$$
\vec a(t) = \bigl(-R\cos t, -R\sin t\bigr)
$$

#### 4. Check magnitudes
Calculate the magnitude of velocity:

$$
\begin{align}
|\vec v(t)| &= \sqrt{(-R\sin t)^2 + (R\cos t)^2} \\
            &= \sqrt{R^2\sin^2 t + R^2\cos^2 t} \\
            &= \sqrt{R^2(\sin^2 t + \cos^2 t)} \\
            &= \sqrt{R^2} \\
            &= R
\end{align}
$$

Calculate the magnitude of acceleration:

$$
\begin{align}
|\vec a(t)| &= \sqrt{(-R\cos t)^2 + (-R\sin t)^2} \\
            &= \sqrt{R^2\cos^2 t + R^2\sin^2 t} \\
            &= \sqrt{R^2(\cos^2 t + \sin^2 t)} \\
            &= \sqrt{R^2} \\
            &= R
\end{align}
$$

Both $|\vec v|$ and $|\vec a|$ are **constant**.

---

### Curve B: $\ x(t) = a\cos t, \quad y(t) = b\sin t$

#### 1. Eliminate the parameter
Divide $x(t)$ by $a$ and $y(t)$ by $b$:

$$
\frac{x}{a} = \cos t
$$

$$
\frac{y}{b} = \sin t
$$

Square both expressions and add them:

$$
\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = \cos^2 t + \sin^2 t
$$

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

#### 2. Determine the type of curve
The equation $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ describes an **ellipse** centered at the origin with semi-axes $a$ and $b$.

#### 3. Determine velocity and acceleration
Differentiate position to find velocity:

$$
\vec v(t) = \bigl(-a\sin t, b\cos t\bigr)
$$

Differentiate velocity to find acceleration:

$$
\vec a(t) = \bigl(-a\cos t, -b\sin t\bigr)
$$

#### 4. Check magnitudes
Calculate the magnitude of velocity:

$$
|\vec v(t)| = \sqrt{(-a\sin t)^2 + (b\cos t)^2}
$$

$$
|\vec v(t)| = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

Calculate the magnitude of acceleration:

$$
|\vec a(t)| = \sqrt{(-a\cos t)^2 + (-b\sin t)^2}
$$

$$
|\vec a(t)| = \sqrt{a^2\cos^2 t + b^2\sin^2 t}
$$

Neither $|\vec v|$ nor $|\vec a|$ is constant (unless $a = b$, which reduces to the circle case). They depend on the parameter $t$.

---

### Curve C: $\ x(t) = t, \quad   y(t) = t^2$

#### 1. Eliminate the parameter
From the first equation, we have $t = x$. Substitute this directly into the second equation:

$$
y = x^2
$$

#### 2. Determine the type of curve
The equation $y = x^2$ describes a **parabola** opening upwards, with its vertex at the origin.

#### 3. Determine velocity and acceleration
Differentiate position to find velocity:

$$
v_x(t) = \frac{d}{dt}(t) = 1
$$

$$
v_y(t) = \frac{d}{dt}(t^2) = 2t
$$

$$
\vec v(t) = \bigl(1, 2t\bigr)
$$

Differentiate velocity to find acceleration:

$$
a_x(t) = \frac{d}{dt}(1) = 0
$$

$$
a_y(t) = \frac{d}{dt}(2t) = 2
$$

$$
\vec a(t) = \bigl(0, 2\bigr)
$$

#### 4. Check magnitudes
Calculate the magnitude of velocity:

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2}
$$

$$
|\vec v(t)| = \sqrt{1 + 4t^2}
$$

Calculate the magnitude of acceleration:

$$
|\vec a(t)| = \sqrt{0^2 + 2^2}
$$

$$
|\vec a(t)| = 2
$$

The magnitude of velocity $|\vec v(t)|$ is **not constant** (it depends on $t$). The magnitude of acceleration $|\vec a(t)|$ is **constant**.

---

### Curve D: $\ x(t) = \cosh t, \quad y(t) = \sinh t$

#### 1. Eliminate the parameter
Square both equations:

$$
x^2 = \cosh^2 t
$$

$$
y^2 = \sinh^2 t
$$

Subtract the second equation from the first:

$$
x^2 - y^2 = \cosh^2 t - \sinh^2 t
$$

Using the hyperbolic identity $\cosh^2 t - \sinh^2 t = 1$, we get:

$$
x^2 - y^2 = 1
$$

Since $x(t) = \cosh t$, and the range of hyperbolic cosine is $\cosh t \geq 1$ for all real $t$, $x$ is always positive.

#### 2. Determine the type of curve
The equation $x^2 - y^2 = 1$ with $x \geq 1$ describes the **right branch of a unit hyperbola**.

#### 3. Determine velocity and acceleration
Recall the derivatives of hyperbolic functions: $\frac{d}{dt}(\cosh t) = \sinh t$ and $\frac{d}{dt}(\sinh t) = \cosh t$.

Differentiate position to find velocity:

$$
\vec v(t) = \bigl(\sinh t, \cosh t\bigr)
$$

Differentiate velocity to find acceleration:

$$
\vec a(t) = \bigl(\cosh t, \sinh t\bigr)
$$

#### 4. Check magnitudes
Calculate the magnitude of velocity:

$$
|\vec v(t)| = \sqrt{\sinh^2 t + \cosh^2 t}
$$

Using the identity $\cosh^2 t + \sinh^2 t = \cosh(2t)$:

$$
|\vec v(t)| = \sqrt{\cosh(2t)}
$$

Calculate the magnitude of acceleration:

$$
|\vec a(t)| = \sqrt{\cosh^2 t + \sinh^2 t}
$$

$$
|\vec a(t)| = \sqrt{\cosh(2t)}
$$

Neither $|\vec v|$ nor $|\vec a|$ is constant; both depend on the parameter $t$.

## Final Result

| Curve | Cartesian Equation | Type of Curve | $\vec v(t)$ | $\vec a(t)$ | $|\vec v|$ Const? | $|\vec a|$ Const? |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **A** | $x^2 + y^2 = R^2$ | Circle | $(-R\sin t, R\cos t)$ | $(-R\cos t, -R\sin t)$ | Yes ($R$) | Yes ($R$) |
| **B** | $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ | Ellipse | $(-a\sin t, b\cos t)$ | $(-a\cos t, -b\sin t)$ | No | No |
| **C** | $y = x^2$ | Parabola | $(1, 2t)$ | $(0, 2)$ | No | Yes ($2$) |
| **D** | $x^2 - y^2 = 1, x\ge 1$ | Hyperbola | $(\sinh t, \cosh t)$ | $(\cosh t, \sinh t)$ | No | No |

## Interpretation



[Image of conic sections: circle, ellipse, parabola, hyperbola]


The parameterization of a curve defines not just its geometric shape, but the specific kinematics (motion) of a particle traversing it. 

In **Curve A (Circle)**, using pure sine and cosine with identical coefficients results in uniform circular motion. The distance to the center is fixed, and the speed is strictly constant. 

In **Curve B (Ellipse)**, the different semi-axes ($a \neq b$) mean the particle must "speed up" and "slow down" depending on its position relative to the origin, making neither speed nor acceleration magnitude constant. 

**Curve C (Parabola)** is classic projectile motion. The horizontal velocity is constant ($v_x = 1$), but the vertical velocity increases linearly with time, leading to a constant downward (or in this case, upward) acceleration of magnitude $2$.

**Curve D (Hyperbola)** utilizes hyperbolic functions which grow exponentially. Even though the trajectory follows a geometric hyperbola, the particle's speed and acceleration magnitude increase continuously and boundlessly as $|t|$ increases.