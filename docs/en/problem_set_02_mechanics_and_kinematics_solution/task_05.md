# Task 05 – Elliptical Motion

## Problem Statement

The path equation of a particle is given in parametric form:

$$
x(t) = a \cos(\omega t), \qquad y(t) = b \sin(\omega t)
$$

* Calculate the velocity $\vec{v}(t)$ and acceleration $\vec{a}(t)$.
* Is the magnitude of the velocity constant?
* Where is the velocity maximum?
* Draw the trajectory and the graphs of $|\vec{v}(t)|$ and $|\vec{a}(t)|$ (qualitative description).

## Theory

Elliptical motion occurs when a particle follows a path defined by the ellipse equation in Cartesian coordinates:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

This is a generalization of circular motion where the semi-axes $a$ and $b$ are not necessarily equal. The kinematics are derived by differentiating the position vector $\vec{r}(t)$ with respect to time.



## Step-by-Step Solution

### 1. Velocity and Acceleration Vectors

**Position vector:**

$$
\vec{r}(t) = \begin{pmatrix} a \cos(\omega t) \\ b \sin(\omega t) \end{pmatrix}
$$

**Velocity vector:**
Differentiating $\vec{r}(t)$ once with respect to $t$:

$$
\vec{v}(t) = \frac{d\vec{r}}{dt} = \begin{pmatrix} -a \omega \sin(\omega t) \\ b \omega \cos(\omega t) \end{pmatrix}
$$

**Acceleration vector:**
Differentiating $\vec{v}(t)$ once with respect to $t$:

$$
\vec{a}(t) = \frac{d\vec{v}}{dt} = \begin{pmatrix} -a \omega^2 \cos(\omega t) \\ -b \omega^2 \sin(\omega t) \end{pmatrix}
$$

### 2. Magnitude of Velocity

The magnitude of the velocity (speed) is calculated as:

$$
|\vec{v}(t)| = \sqrt{(-a \omega \sin(\omega t))^2 + (b \omega \cos(\omega t))^2}
$$

$$
|\vec{v}(t)| = \omega \sqrt{a^2 \sin^2(\omega t) + b^2 \cos^2(\omega t)}
$$

Using the identity $\cos^2(\omega t) = 1 - \sin^2(\omega t)$:

$$
|\vec{v}(t)| = \omega \sqrt{a^2 \sin^2(\omega t) + b^2 (1 - \sin^2(\omega t))} = \omega \sqrt{b^2 + (a^2 - b^2) \sin^2(\omega t)}
$$

The magnitude is **not constant** unless $a = b$ (which would be circular motion). The speed fluctuates as the particle moves along the ellipse.

### 3. Maximum Velocity

To find where the velocity is maximum, we analyze the expression under the square root. Assuming $a > b$:
* The speed is maximized when $\sin^2(\omega t) = 1$.
* This occurs at $\omega t = \pi/2, 3\pi/2, \dots$ (the y-intercepts).
* At these points, $|\vec{v}|_{max} = a\omega$.

If $b > a$, the maximum occurs when $\sin^2(\omega t) = 0$, meaning the velocity is maximum at the x-intercepts ($|\vec{v}|_{max} = b\omega$).

### 4. Trajectory and Kinematic Graphs

* **Trajectory**: A closed ellipse centered at the origin.
* **Velocity Magnitude $|\vec{v}(t)|$**: Periodic function oscillating between $a\omega$ and $b\omega$.
* **Acceleration Magnitude $|\vec{a}(t)|$**:

$$
|\vec{a}(t)| = \omega^2 \sqrt{a^2 \cos^2(\omega t) + b^2 \sin^2(\omega t)}
$$

This is also a periodic function, reaching its maximum at the points where the distance from the origin is greatest (the semi-major axis).

## Final Result

* **Velocity**: $\vec{v}(t) = (-a \omega \sin \omega t, b \omega \cos \omega t)$
* **Acceleration**: $\vec{a}(t) = (-\omega^2 a \cos \omega t, -\omega^2 b \sin \omega t) = -\omega^2 \vec{r}(t)$
* **Velocity Magnitude**: Variable, $|\vec{v}(t)| = \omega \sqrt{a^2 \sin^2 \omega t + b^2 \cos^2 \omega t}$

## Interpretation

Similar to circular motion, the acceleration vector $\vec{a}(t)$ is always directed toward the origin ($\vec{a} = -\omega^2 \vec{r}$). However, because the curvature of the ellipse changes, the speed is not constant. The particle speeds up as it approaches the "flatter" sections and slows down near the "sharper" turns, depending on the ratio of $a$ and $b$.