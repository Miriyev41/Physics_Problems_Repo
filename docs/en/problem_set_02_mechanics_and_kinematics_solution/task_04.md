# Task 04 – Circular Motion

## Problem Statement

A body moves in a circle of radius $R$ with angular velocity $\omega$: 

* Determine the position vector $\vec{r}(t)$, velocity vector $\vec{v}(t)$, and acceleration vector $\vec{a}(t)$.
* Determine the magnitudes $|\vec{r}(t)|$, $|\vec{v}(t)|$, and $|\vec{a}(t)|$.
* Show that the acceleration is centripetal.
* Visualize the vectors $\vec{r}$, $\vec{v}$, and $\vec{a}$.

## Theory

Circular motion in a plane can be described using polar coordinates $(R, \theta)$ or Cartesian coordinates $(x, y)$. For a constant radius $R$ and constant angular velocity $\omega$, the angle $\theta$ changes linearly with time:

$$
\theta(t) = \omega t
$$

The relationship between Cartesian and polar coordinates is:

$$
x = R \cos(\theta), \qquad y = R \sin(\theta)
$$

The velocity and acceleration are found by successive differentiation of the position vector with respect to time.



## Step-by-Step Solution

### 1. Vector Components

Using the parametric relations for a circle:

**Position vector:**

$$
\vec{r}(t) = \begin{pmatrix} R \cos(\omega t) \\ R \sin(\omega t) \end{pmatrix}
$$

**Velocity vector:**
Differentiating $\vec{r}(t)$ once with respect to $t$:

$$
\vec{v}(t) = \frac{d\vec{r}}{dt} = \begin{pmatrix} -R \omega \sin(\omega t) \\ R \omega \cos(\omega t) \end{pmatrix}
$$

**Acceleration vector:**
Differentiating $\vec{v}(t)$ once with respect to $t$:

$$
\vec{a}(t) = \frac{d\vec{v}}{dt} = \begin{pmatrix} -R \omega^2 \cos(\omega t) \\ -R \omega^2 \sin(\omega t) \end{pmatrix}
$$

### 2. Magnitudes

**Magnitude of Position:**

$$
|\vec{r}(t)| = \sqrt{(R \cos(\omega t))^2 + (R \sin(\omega t))^2} = \sqrt{R^2 (\cos^2(\omega t) + \sin^2(\omega t))} = R
$$

**Magnitude of Velocity (Speed):**

$$
|\vec{v}(t)| = \sqrt{(-R \omega \sin(\omega t))^2 + (R \omega \cos(\omega t))^2} = \sqrt{R^2 \omega^2 (1)} = R\omega
$$

**Magnitude of Acceleration:**

$$
|\vec{a}(t)| = \sqrt{(-R \omega^2 \cos(\omega t))^2 + (-R \omega^2 \sin(\omega t))^2} = \sqrt{R^2 \omega^4 (1)} = R\omega^2
$$

### 3. Centripetal Nature of Acceleration

To show the acceleration is centripetal (pointing toward the center), we compare $\vec{a}(t)$ and $\vec{r}(t)$:

$$
\vec{a}(t) = \begin{pmatrix} -R \omega^2 \cos(\omega t) \\ -R \omega^2 \sin(\omega t) \end{pmatrix} = -\omega^2 \begin{pmatrix} R \cos(\omega t) \\ R \sin(\omega t) \end{pmatrix}
$$

$$
\vec{a}(t) = -\omega^2 \vec{r}(t)
$$

Since $\omega^2$ is always positive, the vector $\vec{a}$ is in the exact opposite direction of the position vector $\vec{r}$. Because $\vec{r}$ points from the origin to the particle, $\vec{a}$ must point from the particle back to the origin (the center of the circle).

## Final Result

* **Position**: $\vec{r}(t) = (R \cos \omega t, R \sin \omega t)$
* **Velocity**: $\vec{v}(t) = (-R\omega \sin \omega t, R\omega \cos \omega t)$
* **Acceleration**: $\vec{a}(t) = -\omega^2 \vec{r}(t)$
* **Magnitudes**: $|\vec{r}|=R, |\vec{v}|=R\omega, |\vec{a}|=R\omega^2$

## Interpretation

In uniform circular motion, while the speed $|\vec{v}|$ is constant, the velocity vector is not constant because its direction changes continuously. This change in direction is caused by the centripetal acceleration, which is always perpendicular to the velocity and directed toward the center of rotation.