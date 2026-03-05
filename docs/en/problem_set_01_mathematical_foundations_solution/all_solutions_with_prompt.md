# Problem Set 01 – Solutions

# Task 01 – Vectors and Linear Transformations

## Problem Statement

Given two vectors in three-dimensional space:

$$
\vec a = (2,-1,3)
$$

$$
\vec b = (1,4,-2)
$$

And a transformation matrix:

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

Calculate the vector magnitudes, the normalized vector $\hat a$, the dot product, the cross product, the area of the spanned parallelogram, the transformed vector $A\vec a$, the determinant of $A$, and determine if the transformation preserves spatial orientation.

## Theory

The length (magnitude) of a vector in 3D Euclidean space is given by the square root of the sum of the squares of its components.

$$
|\vec v| = \sqrt{v_x^2 + v_y^2 + v_z^2}
$$

A normalized vector is a vector of length $1$ pointing in the same direction as the original vector.

$$
\hat v = \frac{\vec v}{|\vec v|}
$$

The dot product yields a scalar and relates to the angle $\theta$ between vectors.

$$
\vec a \cdot \vec b = a_x b_x + a_y b_y + a_z b_z = |\vec a| |\vec b| \cos \theta
$$



[Image of vector cross product and right hand rule]


The cross product yields a vector perpendicular to both original vectors. Its magnitude is equal to the area of the parallelogram spanned by the two vectors.

$$
\vec a \times \vec b = (a_y b_z - a_z b_y, a_z b_x - a_x b_z, a_x b_y - a_y b_x)
$$

The determinant of a transformation matrix indicates the scaling factor of the volume. If $\det A > 0$, the transformation preserves the orientation of the space (e.g., right-handedness). If $\det A < 0$, the orientation is reversed.

## Step-by-Step Solution

### 1. Lengths of the vectors

For vector $\vec a$:

$$
|\vec a| = \sqrt{2^2 + (-1)^2 + 3^2}
$$

$$
|\vec a| = \sqrt{4 + 1 + 9} = \sqrt{14}
$$

For vector $\vec b$:

$$
|\vec b| = \sqrt{1^2 + 4^2 + (-2)^2}
$$

$$
|\vec b| = \sqrt{1 + 16 + 4} = \sqrt{21}
$$

### 2. Normalized vector $\hat a$

Dividing each component of $\vec a$ by its magnitude $|\vec a|$:

$$
\hat a = \left( \frac{2}{\sqrt{14}}, \frac{-1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)
$$

### 3. Dot product and angle

Calculating the dot product:

$$
\begin{align}
\vec a \cdot \vec b &= (2)(1) + (-1)(4) + (3)(-2) \\
                    &= 2 - 4 - 6 \\
                    &= -8
\end{align}
$$

Calculating the angle $\theta$:

$$
\cos \theta = \frac{\vec a \cdot \vec b}{|\vec a| |\vec b|}
$$

$$
\cos \theta = \frac{-8}{\sqrt{14} \sqrt{21}} = \frac{-8}{\sqrt{294}}
$$

$$
\theta = \arccos\left(\frac{-8}{\sqrt{294}}\right) \approx 117.8^\circ
$$

### 4. Cross product and area

Calculating the cross product:

$$
\begin{align}
\vec a \times \vec b &= ((-1)(-2) - (3)(4), (3)(1) - (2)(-2), (2)(4) - (-1)(1)) \\
                     &= (2 - 12, 3 + 4, 8 + 1) \\
                     &= (-10, 7, 9)
\end{align}
$$

The area of the parallelogram is the magnitude of the cross product:

$$
\text{Area} = |\vec a \times \vec b| = \sqrt{(-10)^2 + 7^2 + 9^2}
$$

$$
\text{Area} = \sqrt{100 + 49 + 81} = \sqrt{230}
$$

### 5. Matrix operations

Applying the linear transformation to $\vec a$:

$$
A \vec a =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
3
\end{pmatrix}
$$

$$
A \vec a =
\begin{pmatrix}
(2)(2) + (1)(-1) + (0)(3) \\
(0)(2) + (1)(-1) + (-1)(3) \\
(1)(2) + (0)(-1) + (1)(3)
\end{pmatrix}
$$

$$
A \vec a =
\begin{pmatrix}
4 - 1 + 0 \\
0 - 1 - 3 \\
2 + 0 + 3
\end{pmatrix}
=
\begin{pmatrix}
3 \\
-4 \\
5
\end{pmatrix}
$$

Calculating the determinant of $A$ using cofactor expansion along the first row:

$$
\det A = 2(1 \cdot 1 - (-1) \cdot 0) - 1(0 \cdot 1 - (-1) \cdot 1) + 0
$$

$$
\det A = 2(1) - 1(1) = 1
$$

## Final Result

- $|\vec a| = \sqrt{14}$, $|\vec b| = \sqrt{21}$
- $\hat a = \left( \frac{2}{\sqrt{14}}, \frac{-1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)$
- $\vec a \cdot \vec b = -8$, $\theta \approx 117.8^\circ$
- $\vec a \times \vec b = (-10, 7, 9)$, Area $= \sqrt{230}$
- $A\vec a = (3, -4, 5)^T$
- $\det A = 1$

## Interpretation

The negative dot product indicates that the angle between the two vectors is obtuse (greater than $90^\circ$). The determinant of the transformation matrix is positive ($\det A = 1 > 0$), which proves that the matrix represents an orientation-preserving transformation.

---

# Task 02 – Parametric Trajectory, Velocity, and Acceleration

## Problem Statement

The parametric equation of a trajectory is given by:

$$
\vec r(t) = \bigl(t^2,\sin t, 5\bigr)
$$

Determine the velocity $\vec v(t)$, the acceleration $\vec a(t)$, the magnitude of velocity at $t=1$, the dot product $\vec v \cdot \vec a$, and the cross product $\vec v \times \vec a$.

## Theory

The velocity vector is the first derivative of the position vector with respect to time. It describes the rate of change of position.

$$
\vec v(t) = \frac{d\vec r}{dt}
$$

The acceleration vector is the second derivative of the position vector, or the first derivative of the velocity vector. It describes the rate of change of velocity.

$$
\vec a(t) = \frac{d^2 \vec r}{dt^2} = \frac{d\vec v}{dt}
$$

## Step-by-Step Solution

### 1. Velocity vector

Differentiating the components of the position vector:

$$
\vec v(t) = \left( \frac{d}{dt}(t^2), \frac{d}{dt}(\sin t), \frac{d}{dt}(5) \right)
$$

$$
\vec v(t) = (2t, \cos t, 0)
$$

### 2. Acceleration vector

Differentiating the components of the velocity vector:

$$
\vec a(t) = \left( \frac{d}{dt}(2t), \frac{d}{dt}(\cos t), \frac{d}{dt}(0) \right)
$$

$$
\vec a(t) = (2, -\sin t, 0)
$$

### 3. Magnitude of velocity at $t=1$

Substitute $t=1$ into the velocity vector:

$$
\vec v(1) = (2(1), \cos(1), 0) = (2, \cos 1, 0)
$$

Calculate the magnitude:

$$
|\vec v(1)| = \sqrt{2^2 + (\cos 1)^2 + 0^2}
$$

$$
|\vec v(1)| = \sqrt{4 + \cos^2 1}
$$

### 4. Dot product of velocity and acceleration

Using the previously calculated symbolic vectors:

$$
\vec v \cdot \vec a = (2t)(2) + (\cos t)(-\sin t) + (0)(0)
$$

$$
\vec v \cdot \vec a = 4t - \sin t \cos t
$$

### 5. Cross product of velocity and acceleration

Setting up the cross product calculation:

$$
\begin{align}
\vec v \times \vec a &= \bigl( (\cos t)(0) - (0)(-\sin t), (0)(2) - (2t)(0), (2t)(-\sin t) - (\cos t)(2) \bigr) \\
                     &= \bigl( 0, 0, -2t \sin t - 2 \cos t \bigr)
\end{align}
$$

## Final Result

- $\vec v(t) = (2t, \cos t, 0)$
- $\vec a(t) = (2, -\sin t, 0)$
- $|\vec v(1)| = \sqrt{4 + \cos^2 1}$
- $\vec v \cdot \vec a = 4t - \sin t \cos t$
- $\vec v \times \vec a = (0, 0, -2t \sin t - 2 \cos t)$

## Interpretation

The $z$-component of the position is constant ($z=5$), resulting in zero velocity and zero acceleration in the $z$-direction. The motion is strictly confined to the plane $z=5$. The non-zero dot product implies that the angle between velocity and acceleration is not $90^\circ$, meaning the object is experiencing both tangential acceleration (changing speed) and normal acceleration (changing direction).

---

# Task 03 – Integration of Motion

## Problem Statement

### Part A
Given velocity and initial position:

$$
\vec v(t) = \bigl(2t,3,-e^{-t}\bigr)
$$

$$
\vec r(0) = (0,1,2)
$$

Determine the position vector $\vec r(t)$ and acceleration vector $\vec a(t)$.

### Part B
Given acceleration, initial velocity, and initial position:

$$
\vec a(t) = \bigl(4,-\sin t,0\bigr)
$$

$$
\vec v(0) = (1,0,2)
$$

$$
\vec r(0) = (0,0,0)
$$

Determine the velocity vector $\vec v(t)$ and position vector $\vec r(t)$.

## Theory

Kinematic variables are related through integration with respect to time. To find the velocity from acceleration, integrate acceleration and add the initial velocity condition.

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau) \, d\tau
$$

To find position from velocity, integrate velocity and add the initial position condition.

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau) \, d\tau
$$

## Step-by-Step Solution

### Part A Solution

**1. Determine position $\vec r(t)$:**

Integrate the given velocity vector over the interval $[0, t]$:

$$
\vec r(t) = (0,1,2) + \int_0^t (2\tau, 3, -e^{-\tau}) \, d\tau
$$

Evaluate the integral for each component:

$$
\int_0^t 2\tau \, d\tau = \left[ \tau^2 \right]_0^t = t^2
$$

$$
\int_0^t 3 \, d\tau = \left[ 3\tau \right]_0^t = 3t
$$

$$
\int_0^t -e^{-\tau} \, d\tau = \left[ e^{-\tau} \right]_0^t = e^{-t} - 1
$$

Add the integrated vector to the initial position vector:

$$
\vec r(t) = (0, 1, 2) + (t^2, 3t, e^{-t} - 1)
$$

$$
\vec r(t) = (t^2, 3t + 1, e^{-t} + 1)
$$

**2. Determine acceleration $\vec a(t)$:**

Differentiate the velocity vector:

$$
\vec a(t) = \frac{d}{dt} (2t, 3, -e^{-t})
$$

$$
\vec a(t) = (2, 0, e^{-t})
$$

### Part B Solution

**1. Determine velocity $\vec v(t)$:**

Integrate the given acceleration vector over the interval $[0, t]$:

$$
\vec v(t) = (1,0,2) + \int_0^t (4, -\sin \tau, 0) \, d\tau
$$

Evaluate the integral:

$$
\int_0^t 4 \, d\tau = 4t
$$

$$
\int_0^t -\sin \tau \, d\tau = \left[ \cos \tau \right]_0^t = \cos t - 1
$$

Add the result to the initial velocity:

$$
\vec v(t) = (1, 0, 2) + (4t, \cos t - 1, 0)
$$

$$
\vec v(t) = (4t + 1, \cos t - 1, 2)
$$

**2. Determine position $\vec r(t)$:**

Integrate the newly found velocity vector:

$$
\vec r(t) = (0,0,0) + \int_0^t (4\tau + 1, \cos \tau - 1, 2) \, d\tau
$$

Evaluate the integral:

$$
\int_0^t (4\tau + 1) \, d\tau = \left[ 2\tau^2 + \tau \right]_0^t = 2t^2 + t
$$

$$
\int_0^t (\cos \tau - 1) \, d\tau = \left[ \sin \tau - \tau \right]_0^t = \sin t - t
$$

$$
\int_0^t 2 \, d\tau = 2t
$$

Assemble the position vector:

$$
\vec r(t) = (2t^2 + t, \sin t - t, 2t)
$$

## Final Result

**Part A:**
- $\vec r(t) = (t^2, 3t + 1, e^{-t} + 1)$
- $\vec a(t) = (2, 0, e^{-t})$

**Part B:**
- $\vec v(t) = (4t + 1, \cos t - 1, 2)$
- $\vec r(t) = (2t^2 + t, \sin t - t, 2t)$

## Interpretation

Integration allows the complete reconstruction of a system's kinematic history given a starting state (initial conditions). The constants of integration are physically resolved by these initial conditions, anchoring the mathematical solution to the actual physical starting point of the object.

# Task 04 – Geometry of Parametric Curves

## Problem Statement

Investigate the following parametric curves:
A) $x(t) = R\cos t, \quad y(t) = R\sin t$
B) $x(t) = a\cos t, \quad y(t) = b\sin t$
C) $x(t) = t, \quad y(t) = t^2$
D) $x(t) = \cosh t, \quad y(t) = \sinh t$

For each, eliminate the parameter, determine the type of curve, calculate velocity and acceleration, and check if their magnitudes are constant.

## Theory

Parametric equations represent coordinates as functions of a variable $t$. Eliminating $t$ yields the implicit Cartesian equation $f(x,y) = 0$. The geometric properties (type of curve) follow from standard conic section equations. Velocity and acceleration magnitudes are:

$$
|\vec v| = \sqrt{\dot{x}^2 + \dot{y}^2}
$$

$$
|\vec a| = \sqrt{\ddot{x}^2 + \ddot{y}^2}
$$

## Step-by-Step Solution

### Curve A

Given $x = R\cos t$ and $y = R\sin t$.
Using the trigonometric identity $\cos^2 t + \sin^2 t = 1$:

$$
\left(\frac{x}{R}\right)^2 + \left(\frac{y}{R}\right)^2 = 1 \implies x^2 + y^2 = R^2
$$

Type: **Circle** of radius $R$.

Velocity and acceleration:

$$
\vec v(t) = (-R\sin t, R\cos t)
$$

$$
|\vec v| = \sqrt{R^2\sin^2 t + R^2\cos^2 t} = R \quad (\text{Constant})
$$

$$
\vec a(t) = (-R\cos t, -R\sin t)
$$

$$
|\vec a| = \sqrt{R^2\cos^2 t + R^2\sin^2 t} = R \quad (\text{Constant})
$$

### Curve B

Given $x = a\cos t$ and $y = b\sin t$.
Using the same trigonometric identity:

$$
\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = 1
$$

Type: **Ellipse** with semi-axes $a$ and $b$.

Velocity and acceleration:

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
|\vec v| = \sqrt{a^2\sin^2 t + b^2\cos^2 t} \quad (\text{Not constant})
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

$$
|\vec a| = \sqrt{a^2\cos^2 t + b^2\sin^2 t} \quad (\text{Not constant})
$$

### Curve C

Given $x = t$ and $y = t^2$.
Substituting $t = x$ into the second equation:

$$
y = x^2
$$

Type: **Parabola**.

Velocity and acceleration:

$$
\vec v(t) = (1, 2t)
$$

$$
|\vec v| = \sqrt{1 + 4t^2} \quad (\text{Not constant})
$$

$$
\vec a(t) = (0, 2)
$$

$$
|\vec a| = \sqrt{0^2 + 2^2} = 2 \quad (\text{Constant})
$$

### Curve D

Given $x = \cosh t$ and $y = \sinh t$.
Using the hyperbolic identity $\cosh^2 t - \sinh^2 t = 1$:

$$
x^2 - y^2 = 1
$$

Type: **Hyperbola** (right branch, since $x = \cosh t \ge 1$).

Velocity and acceleration:

$$
\vec v(t) = (\sinh t, \cosh t)
$$

$$
|\vec v| = \sqrt{\sinh^2 t + \cosh^2 t} = \sqrt{\cosh(2t)} \quad (\text{Not constant})
$$

$$
\vec a(t) = (\cosh t, \sinh t)
$$

$$
|\vec a| = \sqrt{\cosh^2 t + \sinh^2 t} = \sqrt{\cosh(2t)} \quad (\text{Not constant})
$$

## Final Result

- **A)** Circle, $x^2 + y^2 = R^2$. Both $|\vec v|$ and $|\vec a|$ are constant.
- **B)** Ellipse, $x^2/a^2 + y^2/b^2 = 1$. Neither $|\vec v|$ nor $|\vec a|$ is constant.
- **C)** Parabola, $y = x^2$. Only $|\vec a|$ is constant.
- **D)** Hyperbola, $x^2 - y^2 = 1$. Neither $|\vec v|$ nor $|\vec a|$ is constant.

## Interpretation

A constant velocity magnitude implies uniform motion along the path, but a constant acceleration magnitude only occurs when the forces acting on the particle are constant in magnitude (as in uniform circular motion or projectile motion). 

---

# Task 05 – Trajectory Curvature and Normal Acceleration

## Problem Statement

For an ellipse $x = a\cos t$, $y = b\sin t$, determine the velocity, acceleration, unit tangent vector, normal acceleration magnitude, and the radius of curvature at $t=0$. Answer the physical interpretation questions.

## Theory

Acceleration can be decomposed into tangential and normal components:

$$
\vec a = \vec a_t + \vec a_n
$$

The tangential acceleration changes the speed, while the normal acceleration changes the direction. The magnitude of normal acceleration is related to speed $v = |\vec v|$ and the radius of curvature $R$ by:

$$
a_n = \frac{v^2}{R}
$$



## Step-by-Step Solution

### 1. Velocity and Acceleration

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

### 2. Unit Tangent Vector

The magnitude of the velocity is:

$$
|\vec v(t)| = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

The unit tangent vector is:

$$
\hat T(t) = \frac{\vec v(t)}{|\vec v(t)|} = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)
$$

### 3. Normal Acceleration

At $t=0$:

$$
\vec v(0) = (0, b)
$$

$$
\vec a(0) = (-a, 0)
$$

The tangential component of acceleration is the projection of $\vec a$ onto $\vec v$:

$$
a_t = \frac{\vec a \cdot \vec v}{|\vec v|}
$$

At $t=0$:

$$
\vec a(0) \cdot \vec v(0) = (-a)(0) + (0)(b) = 0
$$

Since the dot product is zero, the entire acceleration is purely normal. Therefore, the normal acceleration magnitude is:

$$
a_n(0) = |\vec a(0)| = a
$$

### 4. Radius of Curvature at $t=0$

Using the relation $a_n = v^2/R$:

$$
R = \frac{v^2}{a_n}
$$

At $t=0$, $v = |\vec v(0)| = b$, and $a_n = a$. Thus:

$$
R = \frac{b^2}{a}
$$

### 5. Comparison with a Circle

For a circle, $a = b$. Substituting this into the radius of curvature formula:

$$
R = \frac{a^2}{a} = a
$$

This is consistent with the constant radius of a circle.

## Final Result

- $\vec v(t) = (-a\sin t, b\cos t)$
- $\vec a(t) = (-a\cos t, -b\sin t)$
- $\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)$
- $a_n(0) = a$
- $R(0) = \frac{b^2}{a}$

## Interpretation

- **Does a greater trajectory curvature imply a greater normal acceleration?** Yes. Curvature is $\kappa = 1/R$. Since $a_n = v^2 \kappa$, for a given speed $v$, a larger curvature directly implies a larger normal acceleration.
- **Where is the trajectory more "curved"?** At the end of the major axis. If $a > b$, $R = b^2/a$ is minimal at $x=a$ (end of the major axis), meaning the curvature is maximal there.
- **Why does normal acceleration change direction?** Normal acceleration is perpendicular to the velocity vector. It does no work ($P = \vec F \cdot \vec v = 0$), meaning it cannot change the kinetic energy or speed of the particle; it can only rotate the velocity vector.

---

# Task 06 – Curve Length and Numerical Integration

## Problem Statement

For $x(t) = t$, $y(t) = t^2$, $t \in [0,1]$, determine velocity, magnitude of velocity, formulate the arc length integral, and design a numerical scheme (trapezoidal rule).

## Theory

The arc length of a parametric curve from $t=a$ to $t=b$ is the integral of the velocity magnitude:

$$
s = \int_a^b |\vec v(t)| \, dt
$$

## Step-by-Step Solution

### 1. Velocity Vector

$$
\vec v(t) = \left( \frac{d}{dt}(t), \frac{d}{dt}(t^2) \right) = (1, 2t)
$$

### 2. Magnitude of Velocity

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2} = \sqrt{1 + 4t^2}
$$

### 3. Arc Length Integral

$$
s = \int_0^1 \sqrt{1 + 4t^2} \, dt
$$

### 4. Analytical Evaluation

This integral can be solved analytically using the substitution $2t = \sinh u$:

$$
s = \left[ \frac{t}{2}\sqrt{1+4t^2} + \frac{1}{4}\ln\left(2t + \sqrt{1+4t^2}\right) \right]_0^1
$$

$$
s = \frac{\sqrt{5}}{2} + \frac{1}{4}\ln(2 + \sqrt{5}) \approx 1.4789
$$

### 5. Numerical Implementation Logic (Trapezoidal Rule)

For computational physics applications, the integral can be approximated by dividing the interval into $N$ segments of width $h = 1/N$.

```javascript
function calculateArcLength(N) {
    let h = 1.0 / N;
    let sum = 0;
    let f = (t) => Math.sqrt(1 + 4 * t * t);
    
    // Trapezoidal rule: (h/2) * [f(x0) + 2f(x1) + ... + 2f(xn-1) + f(xn)]
    sum += f(0) / 2.0;
    for (let i = 1; i < N; i++) {
        sum += f(i * h);
    }
    sum += f(1) / 2.0;
    
    return sum * h;
}
