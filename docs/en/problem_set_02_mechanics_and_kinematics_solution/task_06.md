# Task 06 – Cycloid: Trajectory of a Point on a Rolling Circle

## Problem Statement

A circle of radius $R$ rolls without slipping along the $x$-axis. A point on the rim of the circle traces a cycloid: 

$$
x(t) = R(\omega t - \sin(\omega t)), \qquad y(t) = R(1 - \cos(\omega t))
$$

1. Determine the velocity vector $\vec{v}(t)$ and the acceleration $\vec{a}(t)$.
2. Calculate $|\vec{v}(t)|$ and indicate the moments when the point temporarily "stops" relative to the ground.
3. Determine the maximum values of $|\vec{v}|$ and $|\vec{a}|$.
4. Create an HTML animation description (conceptual).
5. Compare the cycloid with circular motion in a reference frame attached to the circle.

## Theory

The cycloid is the curve traced by a point on the circumference of a circle as it rolls along a straight line without slipping. The condition of "rolling without slipping" implies that the distance the center of the circle moves ($R\omega t$) is equal to the arc length subtended by the rotation.

Kinematically, the motion is the superposition of:
1.  **Translation**: The center moves at constant velocity $v_c = R\omega$.
2.  **Rotation**: The point rotates around the center with angular velocity $\omega$.



## Step-by-Step Solution

### 1. Velocity and Acceleration Vectors

**Position vector:**

$$
\vec{r}(t) = \begin{pmatrix} R(\omega t - \sin(\omega t)) \\ R(1 - \cos(\omega t)) \end{pmatrix}
$$

**Velocity vector $\vec{v}(t)$:**
Differentiating $\vec{r}(t)$ with respect to $t$:

$$
v_x(t) = \frac{dx}{dt} = R(\omega - \omega \cos(\omega t)) = R\omega(1 - \cos(\omega t))
$$

$$
v_y(t) = \frac{dy}{dt} = R(0 - (-\omega \sin(\omega t))) = R\omega \sin(\omega t)
$$

$$
\vec{v}(t) = \begin{pmatrix} R\omega(1 - \cos(\omega t)) \\ R\omega \sin(\omega t) \end{pmatrix}
$$

**Acceleration vector $\vec{a}(t)$:**
Differentiating $\vec{v}(t)$ with respect to $t$:

$$
a_x(t) = \frac{dv_x}{dt} = R\omega(0 - (-\omega \sin(\omega t))) = R\omega^2 \sin(\omega t)
$$

$$
a_y(t) = \frac{dv_y}{dt} = R\omega(\omega \cos(\omega t)) = R\omega^2 \cos(\omega t)
$$

$$
\vec{a}(t) = \begin{pmatrix} R\omega^2 \sin(\omega t) \\ R\omega^2 \cos(\omega t) \end{pmatrix}
$$

### 2. Velocity Magnitude and Stopping Points

**Magnitude of Velocity:**

$$
|\vec{v}(t)| = \sqrt{[R\omega(1 - \cos(\omega t))]^2 + [R\omega \sin(\omega t)]^2}
$$

$$
|\vec{v}(t)| = R\omega \sqrt{1 - 2\cos(\omega t) + \cos^2(\omega t) + \sin^2(\omega t)}
$$

$$
|\vec{v}(t)| = R\omega \sqrt{2 - 2\cos(\omega t)} = R\omega \sqrt{2(1 - \cos(\omega t))}
$$

Using the identity $1 - \cos\theta = 2\sin^2(\theta/2)$:

$$
|\vec{v}(t)| = R\omega \sqrt{4\sin^2\left(\frac{\omega t}{2}\right)} = 2R\omega \left| \sin\left(\frac{\omega t}{2}\right) \right|
$$

**Stopping Points:**
The point "stops" ($|\vec{v}| = 0$) when $\sin(\frac{\omega t}{2}) = 0$. This occurs at:

$$
\frac{\omega t}{2} = k\pi \implies \omega t = 2k\pi \quad (k = 0, 1, 2, \dots)
$$

At these moments, the point is in contact with the $x$-axis (the ground).

### 3. Maximum Values

**Maximum Velocity:**
$|\vec{v}|$ is maximum when $\sin(\frac{\omega t}{2}) = 1$:

$$
|\vec{v}|_{max} = 2R\omega
$$

This occurs at the top of the arch ($y = 2R$).

**Maximum Acceleration:**

$$
|\vec{a}(t)| = \sqrt{(R\omega^2 \sin(\omega t))^2 + (R\omega^2 \cos(\omega t))^2} = R\omega^2 \sqrt{\sin^2(\omega t) + \cos^2(\omega t)}
$$

$$
|\vec{a}|_{max} = R\omega^2
$$

The magnitude of acceleration is constant.

### 4. Comparison with Circular Motion

In a reference frame attached to the **center of the circle**:
* The motion is simple uniform circular motion.
* The velocity is constant in magnitude ($R\omega$) and always tangent to the circle.
* The acceleration is constant in magnitude ($R\omega^2$) and always centripetal.

In the **laboratory frame** (the ground):
* The velocity changes in both magnitude and direction.
* The acceleration magnitude remains $R\omega^2$, identical to the circular motion, but its direction relative to the path changes.

## Final Result

* **Velocity**: $\vec{v}(t) = (R\omega(1 - \cos \omega t), R\omega \sin \omega t)$
* **Acceleration**: $\vec{a}(t) = (R\omega^2 \sin \omega t, R\omega^2 \cos \omega t)$
* **Max Velocity**: $2R\omega$ (at the peak)
* **Max Acceleration**: $R\omega^2$ (constant magnitude)

## Interpretation

The cycloid demonstrates that a point on a rolling wheel has a variable speed relative to the ground, even if the wheel rotates at a constant rate. At the point of contact with the ground, the point has zero instantaneous velocity, which is the fundamental condition for "rolling without slipping."