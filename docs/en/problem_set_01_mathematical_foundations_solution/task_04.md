# Task 04 – Geometry of Parametric Curves

## Problem Statement

Investigate the following parametric curves:

A) $x(t) = R\cos t, \quad y(t) = R\sin t$

B) $x(t) = a\cos t, \quad y(t) = b\sin t$

C) $x(t) = t, \quad y(t) = t^2$

D) $x(t) = \cosh t, \quad y(t) = \sinh t$

For each curve, the following must be determined:
1. Eliminate the parameter $t$ (if possible) to find the implicit equation of the curve.
2. Determine the geometric type of the curve.
3. Determine the velocity vector $\vec v(t)$ and the acceleration vector $\vec a(t)$.
4. Check if the velocity magnitude $|\vec v(t)|$ or acceleration magnitude $|\vec a(t)|$ is constant.

## Theory

A parametric curve defines coordinates as functions of a single variable, usually time $t$. Eliminating the parameter involves using algebraic, trigonometric, or hyperbolic identities to express $y$ purely as a function of $x$ (or implicitly as an equation relating $x$ and $y$). 

The fundamental identities frequently used are:

$$
\cos^2 t + \sin^2 t = 1
$$

$$
\cosh^2 t - \sinh^2 t = 1
$$

In kinematics, the velocity vector is the first time-derivative of the position vector, and acceleration is the second time-derivative. Their magnitudes (lengths) define the speed and the strength of the acceleration. To determine if a magnitude is constant, one must check if the resulting expression for the magnitude depends on the parameter $t$.

## Step-by-Step Solution

### Curve A: $x(t) = R\cos t, \quad y(t) = R\sin t$

#### 1. Eliminating the parameter

Square both coordinates and add them together:

$$
\begin{align}
x^2 + y^2 &= (R\cos t)^2 + (R\sin t)^2 \\
          &= R^2\cos^2 t + R^2\sin^2 t \\
          &= R^2(\cos^2 t + \sin^2 t)
\end{align}
$$

Using the fundamental trigonometric identity, this simplifies to:

$$
x^2 + y^2 = R^2
$$

#### 2. Type of curve

The equation $x^2 + y^2 = R^2$ describes a **circle** centered at the origin with radius $R$.

#### 3. Velocity and acceleration

Differentiating the position components with respect to $t$:

$$
\vec v(t) = \left( \frac{d}{dt}(R\cos t), \frac{d}{dt}(R\sin t) \right) = (-R\sin t, R\cos t)
$$

Differentiating the velocity components:

$$
\vec a(t) = \left( \frac{d}{dt}(-R\sin t), \frac{d}{dt}(R\cos t) \right) = (-R\cos t, -R\sin t)
$$

#### 4. Constancy of magnitudes

Calculate the magnitude of velocity:

$$
\begin{align}
|\vec v(t)| &= \sqrt{(-R\sin t)^2 + (R\cos t)^2} \\
            &= \sqrt{R^2\sin^2 t + R^2\cos^2 t} \\
            &= \sqrt{R^2(1)} \\
            &= R
\end{align}
$$

Calculate the magnitude of acceleration:

$$
\begin{align}
|\vec a(t)| &= \sqrt{(-R\cos t)^2 + (-R\sin t)^2} \\
            &= \sqrt{R^2\cos^2 t + R^2\sin^2 t} \\
            &= R
\end{align}
$$

Both $|\vec v(t)|$ and $|\vec a(t)|$ are **constant**.

---

### Curve B: $x(t) = a\cos t, \quad y(t) = b\sin t$

#### 1. Eliminating the parameter

Isolate the trigonometric functions:

$$
\frac{x}{a} = \cos t, \quad \frac{y}{b} = \sin t
$$

Square both equations and add them:

$$
\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = \cos^2 t + \sin^2 t
$$

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

#### 2. Type of curve

This is the standard equation of an **ellipse** centered at the origin with semi-major and semi-minor axes $a$ and $b$.

#### 3. Velocity and acceleration

Differentiating with respect to $t$:

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

#### 4. Constancy of magnitudes

Magnitude of velocity:

$$
|\vec v(t)| = \sqrt{(-a\sin t)^2 + (b\cos t)^2} = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

Magnitude of acceleration:

$$
|\vec a(t)| = \sqrt{(-a\cos t)^2 + (-b\sin t)^2} = \sqrt{a^2\cos^2 t + b^2\sin^2 t}
$$

Because $a \neq b$ (in the general case), these expressions depend on $t$. Therefore, neither $|\vec v(t)|$ nor $|\vec a(t)|$ is **constant**.

---

### Curve C: $x(t) = t, \quad y(t) = t^2$

#### 1. Eliminating the parameter

Substitute the expression for $t$ from the first equation ($t = x$) directly into the second equation:

$$
y = x^2
$$

#### 2. Type of curve

This represents a standard **parabola**.

#### 3. Velocity and acceleration

Differentiating with respect to $t$:

$$
\vec v(t) = (1, 2t)
$$

$$
\vec a(t) = (0, 2)
$$

#### 4. Constancy of magnitudes

Magnitude of velocity:

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2} = \sqrt{1 + 4t^2}
$$

This clearly depends on $t$.

Magnitude of acceleration:

$$
|\vec a(t)| = \sqrt{0^2 + 2^2} = 2
$$

The magnitude of acceleration is **constant**, but the magnitude of velocity is **not constant**.

---

### Curve D: $x(t) = \cosh t, \quad y(t) = \sinh t$

#### 1. Eliminating the parameter

Square both coordinates and subtract the second from the first:

$$
x^2 - y^2 = \cosh^2 t - \sinh^2 t
$$

Using the fundamental hyperbolic identity:

$$
x^2 - y^2 = 1
$$

Note that since $\cosh t \ge 1$ for all real $t$, this only traces the part of the curve where $x \ge 1$.

#### 2. Type of curve

The equation describes a **hyperbola**. Specifically, the parametric equations trace only the **right branch** of the hyperbola.

#### 3. Velocity and acceleration

Recall the derivatives of hyperbolic functions: $\frac{d}{dt}\cosh t = \sinh t$ and $\frac{d}{dt}\sinh t = \cosh t$.

$$
\vec v(t) = (\sinh t, \cosh t)
$$

$$
\vec a(t) = (\cosh t, \sinh t)
$$

#### 4. Constancy of magnitudes

Magnitude of velocity:

$$
|\vec v(t)| = \sqrt{\sinh^2 t + \cosh^2 t}
$$

Using the identity $\cosh(2t) = \cosh^2 t + \sinh^2 t$:

$$
|\vec v(t)| = \sqrt{\cosh(2t)}
$$

Magnitude of acceleration:

$$
|\vec a(t)| = \sqrt{\cosh^2 t + \sinh^2 t} = \sqrt{\cosh(2t)}
$$

Since $\cosh(2t)$ varies with $t$, neither magnitude is **constant**.

## Final Result

- **Curve A**: Circle ($x^2 + y^2 = R^2$). $|\vec v| = R$ (constant), $|\vec a| = R$ (constant).
- **Curve B**: Ellipse ($\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$). $|\vec v|$ is not constant, $|\vec a|$ is not constant.
- **Curve C**: Parabola ($y = x^2$). $|\vec v| = \sqrt{1+4t^2}$ (not constant), $|\vec a| = 2$ (constant).
- **Curve D**: Hyperbola right branch ($x^2 - y^2 = 1, x \ge 1$). $|\vec v| = \sqrt{\cosh(2t)}$ (not constant), $|\vec a| = \sqrt{\cosh(2t)}$ (not constant).

## Interpretation

The physical properties of the motion reflect the geometric nature of the curves. 

For the circle (Curve A), motion parameterized by $t$ represents uniform circular motion, meaning the speed is constant. Consequently, the acceleration is purely centripetal, maintaining a constant magnitude as it continuously changes the direction of the velocity vector.

For the parabola (Curve C), the constant acceleration vector $(0,2)$ represents motion under a uniform force field, mathematically identical to idealized projectile motion under constant gravity. The speed changes because the component of velocity parallel to the acceleration increases linearly over time.

For the ellipse and hyperbola, the parameterization given implies non-uniform motion where both the speed of the particle and the magnitude of the forces acting upon it vary depending on its position along the trajectory.