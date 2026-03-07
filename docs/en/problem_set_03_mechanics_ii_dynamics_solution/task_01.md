# Task 01 – Newton's Second Law (Constant Force)

## Problem Statement

A constant force acts on a body of mass $m = 2\ \text{kg}$:

$$
\vec{F} = \begin{pmatrix} 6 \\ 2 \end{pmatrix}\ \text{N}
$$

The body starts with an initial velocity $\vec{v}(0) = (1, -1)\ \text{m/s}$ from the point $\vec{r}(0) = (0, 0)\ \text{m}$.

* Determine $\vec{a}(t)$.
* Determine $\vec{v}(t)$.
* Determine $\vec{r}(t)$.
* Draw the trajectory of the motion.
* Calculate the work done by the force at time $t = 3\ \text{s}$.
* Check the consistency with the work-energy theorem.

## Theory

Newton's Second Law states that the acceleration of an object is directly proportional to the net force acting on it and inversely proportional to its mass:

$$
\vec{F} = m\vec{a} \implies \vec{a} = \frac{\vec{F}}{m}
$$

For a constant force, the acceleration is constant. The velocity and position are found by integration:

$$
\vec{v}(t) = \int \vec{a} \, dt = \vec{v}_0 + \vec{a}t
$$

$$
\vec{r}(t) = \int \vec{v}(t) \, dt = \vec{r}_0 + \vec{v}_0 t + \frac{1}{2}\vec{a}t^2
$$

The work done by a constant force is the dot product of force and displacement:

$$
W = \vec{F} \cdot \Delta\vec{r}
$$

The work-energy theorem states that the work done by the net force equals the change in kinetic energy:

$$
W = \Delta K = \frac{1}{2}m v_f^2 - \frac{1}{2}m v_i^2
$$

## Step-by-Step Solution

### 1. Acceleration Vector

Using the given mass $m = 2\ \text{kg}$ and force:

$$
\vec{a} = \frac{1}{2} \begin{pmatrix} 6 \\ 2 \end{pmatrix} = \begin{pmatrix} 3 \\ 1 \end{pmatrix}\ \text{m/s}^2
$$

### 2. Velocity Vector

Integrating with initial velocity $\vec{v}_0 = (1, -1)$:

$$
\vec{v}(t) = \begin{pmatrix} 1 \\ -1 \end{pmatrix} + \begin{pmatrix} 3 \\ 1 \end{pmatrix}t = \begin{pmatrix} 1 + 3t \\ -1 + t \end{pmatrix}
$$

### 3. Position Vector

Integrating with initial position $\vec{r}_0 = (0, 0)$:

$$
\vec{r}(t) = \begin{pmatrix} 1 \\ -1 \end{pmatrix}t + \frac{1}{2} \begin{pmatrix} 3 \\ 1 \end{pmatrix}t^2 = \begin{pmatrix} t + 1.5t^2 \\ -t + 0.5t^2 \end{pmatrix}
$$

### 4. Work Done at $t = 3\ \text{s}$

First, find the displacement $\Delta\vec{r}$ at $t = 3$:

$$
\vec{r}(3) = \begin{pmatrix} 3 + 1.5(3^2) \\ -3 + 0.5(3^2) \end{pmatrix} = \begin{pmatrix} 16.5 \\ 1.5 \end{pmatrix}\ \text{m}
$$

The work done is:

$$
W = \vec{F} \cdot \vec{r}(3) = \begin{pmatrix} 6 \\ 2 \end{pmatrix} \cdot \begin{pmatrix} 16.5 \\ 1.5 \end{pmatrix} = (6 \times 16.5) + (2 \times 1.5) = 99 + 3 = 102\ \text{J}
$$

### 5. Work-Energy Theorem Verification

**Initial Kinetic Energy ($K_i$):**
$v_0^2 = 1^2 + (-1)^2 = 2$

$$
K_i = \frac{1}{2}(2)(2) = 2\ \text{J}
$$

**Final Kinetic Energy at $t = 3$ ($K_f$):**
$\vec{v}(3) = (1 + 3(3), -1 + 3) = (10, 2)$
$v_f^2 = 10^2 + 2^2 = 104$

$$
K_f = \frac{1}{2}(2)(104) = 104\ \text{J}
$$

**Change in Kinetic Energy:**
$\Delta K = 104 - 2 = 102\ \text{J}$

Since $W = \Delta K = 102\ \text{J}$, the theorem is verified.

## Final Result

* **Acceleration**: $\vec{a} = (3, 1)\ \text{m/s}^2$
* **Velocity**: $\vec{v}(t) = (1+3t, -1+t)$
* **Position**: $\vec{r}(t) = (t+1.5t^2, -t+0.5t^2)$
* **Work**: $W = 102\ \text{J}$

## Interpretation

The constant force results in a parabolic trajectory. The initial motion is directed into the fourth quadrant, but the positive acceleration in both axes eventually pulls the body into the first quadrant. The energy analysis confirms that the work performed by the external force is entirely converted into the kinetic energy of the mass.