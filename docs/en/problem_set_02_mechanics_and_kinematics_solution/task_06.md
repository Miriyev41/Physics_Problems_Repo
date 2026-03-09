# Task 06 – Projectile motion with air resistance (linear model)

## Problem Statement

A body is thrown with an initial velocity $\vec v_0 = (v_{0x}, v_{0y})$. In addition to gravity, a linear air resistance force $\vec F_d = -b\vec v$ acts on the body.

The required operations are:
1. Write the differential equations of motion for the $x$ and $y$ components.
2. Solve these equations to find $v_x(t)$ and $v_y(t)$.
3. Determine the terminal velocity $v_{term}$ in the vertical direction.
4. Integrate the velocity to find the position equations $x(t)$ and $y(t)$.
5. Compare the trajectory with the case without air resistance (Problem 2).

## Theory

According to Newton's Second Law, the net force on an object is equal to the mass times its acceleration ($\vec F = m\vec a$). In this model, two forces act on the projectile:
- **Gravity:** $\vec F_g = (0, -mg)$
- **Linear Air Resistance:** $\vec F_d = -b\vec v = (-bv_x, -bv_y)$

The total force is:

$$
m\vec a = \vec F_g + \vec F_d
$$

This leads to a system of coupled first-order linear differential equations for the velocity components. The parameter $k = b/m$ is often used to simplify the equations, representing the resistance coefficient per unit mass.

## Step-by-Step Solution

### 1. Write the differential equations of motion

**Horizontal direction ($x$):**

$$
m \frac{dv_x}{dt} = -bv_x
$$

Divide by $m$ and let $k = b/m$:

$$
\frac{dv_x}{dt} = -kv_x
$$

**Vertical direction ($y$):**

$$
m \frac{dv_y}{dt} = -mg - bv_y
$$

Divide by $m$:

$$
\frac{dv_y}{dt} = -g - kv_y
$$

### 2. Solve for $v_x(t)$ and $v_y(t)$

**Solving for $v_x(t)$:**
This is a separable equation:

$$
\frac{dv_x}{v_x} = -k\, dt
$$

Integrate both sides:

$$
\ln v_x = -kt + C
$$

Apply the initial condition $v_x(0) = v_{0x}$:

$$
v_x(t) = v_{0x} e^{-kt}
$$

**Solving for $v_y(t)$:**
Rearrange the equation:

$$
\frac{dv_y}{dt} + kv_y = -g
$$

This is a first-order linear ODE. Using an integrating factor $e^{kt}$:

$$
\frac{d}{dt}(e^{kt}v_y) = -ge^{kt}
$$

Integrate both sides:

$$
e^{kt}v_y = -\frac{g}{k}e^{kt} + C
$$

$$
v_y(t) = -\frac{g}{k} + Ce^{-kt}
$$

Apply initial condition $v_y(0) = v_{0y}$:

$$
v_{0y} = -\frac{g}{k} + C \implies C = v_{0y} + \frac{g}{k}
$$

The velocity solution is:

$$
v_y(t) = \left(v_{0y} + \frac{g}{k}\right)e^{-kt} - \frac{g}{k}
$$

### 3. Determine terminal velocity $v_{term}$

Terminal velocity occurs when acceleration becomes zero, meaning the drag force perfectly balances gravity. Mathematically, this is the limit as $t \to \infty$:

$$
\begin{align}
v_{term} &= \lim_{t \to \infty} v_y(t) \\
         &= \lim_{t \to \infty} \left[ \left(v_{0y} + \frac{g}{k}\right)e^{-kt} - \frac{g}{k} \right] \\
         &= 0 - \frac{g}{k}
\end{align}
$$

The terminal speed is $g/k = mg/b$.

### 4. Determine position equations $x(t)$ and $y(t)$

Integrate the velocity functions (assuming $x(0)=0$ and $y(0)=0$):

**Horizontal Position:**

$$
\begin{align}
x(t) &= \int_0^t v_{0x} e^{-k\tau} \, d\tau \\
     &= \left[ -\frac{v_{0x}}{k} e^{-k\tau} \right]_0^t \\
     &= \frac{v_{0x}}{k} (1 - e^{-kt})
\end{align}
$$

**Vertical Position:**

$$
\begin{align}
y(t) &= \int_0^t \left[ \left(v_{0y} + \frac{g}{k}\right)e^{-k\tau} - \frac{g}{k} \right] \, d\tau \\
     &= \left[ -\frac{1}{k}\left(v_{0y} + \frac{g}{k}\right)e^{-k\tau} - \frac{g}{k}\tau \right]_0^t \\
     &= \frac{1}{k}\left(v_{0y} + \frac{g}{k}\right)(1 - e^{-kt}) - \frac{g}{k}t
\end{align}
$$

## Final Result

* Velocity $x$: $v_x(t) = v_{0x} e^{-kt}$
* Velocity $y$: $v_y(t) = (v_{0y} + g/k)e^{-kt} - g/k$
* Terminal speed: $v_{term} = g/k$
* Position $x$: $x(t) = \frac{v_{0x}}{k} (1 - e^{-kt})$
* Position $y$: $y(t) = \frac{1}{k}(v_{0y} + g/k)(1 - e^{-kt}) - \frac{gt}{k}$

## Interpretation



The presence of air resistance fundamentally changes the symmetry of the trajectory. 

1. **Horizontal Limit:** In a vacuum, $x$ increases linearly forever. With air resistance, as $t \to \infty$, $x(t)$ approaches a finite value $x_{max} = v_{0x}/k$. This is the "impact wall" beyond which the projectile cannot pass.
2. **Asymmetry:** The trajectory is no longer a parabola. It is steeper on the way down than on the way up.
3. **Terminal Velocity:** Unlike the vacuum case where vertical speed increases indefinitely, the resistance force limits the fall speed to a constant value $v_{term}$. 

This model is more realistic for small, slow-moving objects (like a grain of sand in water) where "Stokes' Law" (linear drag) is applicable.