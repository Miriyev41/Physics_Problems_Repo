# Task 07 – Projectile motion with quadratic air resistance

## Problem Statement

Consider the motion of a projectile where the air resistance is proportional to the square of the velocity:

$$
\vec F_d = -c |\vec v| \vec v
$$

The required operations are:
1. Write the differential equations of motion for the $x$ and $y$ components.
2. Explain why this system of equations cannot be solved analytically like the linear case.
3. Implement a numerical solution using the Euler method in an HTML/JS application.
4. Compare the results with the linear model (Problem 6).

## Theory

For high-speed projectiles (like a baseball or a cannonball), the air resistance is better modeled by a quadratic dependence on speed. Newton's Second Law ($\vec F = m\vec a$) for this system is:

$$
m \vec a = m \vec g - c |\vec v| \vec v
$$

Where $|\vec v| = \sqrt{v_x^2 + v_y^2}$. The drag force components are:

$$
F_{dx} = -c \sqrt{v_x^2 + v_y^2} v_x, \qquad F_{dy} = -c \sqrt{v_x^2 + v_y^2} v_y
$$

Unlike the linear model, the $x$ and $y$ components are **coupled**. This means the change in horizontal velocity depends on the vertical velocity, and vice versa. Because of this coupling and the non-linearity ($v^2$ terms), no general analytical solution exists in terms of elementary functions.

The **Euler Method** is a first-order numerical procedure for solving ODEs. It approximates the next state by taking a small step $\Delta t$ in the direction of the current derivative:

$$
v_{n+1} = v_n + a_n \Delta t, \qquad r_{n+1} = r_n + v_n \Delta t
$$

## Step-by-Step Solution

### 1. Write the differential equations of motion

Define $k = c/m$ as the drag coefficient per unit mass.

**Horizontal Component ($x$):**

$$
\frac{dv_x}{dt} = -k \sqrt{v_x^2 + v_y^2} v_x
$$

**Vertical Component ($y$):**

$$
\frac{dv_y}{dt} = -g - k \sqrt{v_x^2 + v_y^2} v_y
$$

### 2. Explanation of Non-solvability

In Task 06 (linear drag), the equation for $v_x$ was $\dot{v}_x = -kv_x$, which is independent of $v_y$. In the quadratic model:
- The equations are **non-linear** due to the $v^2$ terms (inside the square root and multiplied by the component).
- The equations are **coupled**. You cannot solve for $x(t)$ without simultaneously knowing $y(t)$.
- Standard integration techniques fail because the variables cannot be separated.

### 3. Numerical Algorithm (Euler Method)

To solve this numerically, we iterate through time steps $i$:

1. Calculate current speed: $v_i = \sqrt{v_{x,i}^2 + v_{y,i}^2}$
2. Calculate accelerations:
   - $a_{x,i} = -k \cdot v_i \cdot v_{x,i}$
   - $a_{y,i} = -g - k \cdot v_i \cdot v_{y,i}$
3. Update velocities:
   - $v_{x,i+1} = v_{x,i} + a_{x,i} \Delta t$
   - $v_{y,i+1} = v_{y,i} + a_{y,i} \Delta t$
4. Update positions:
   - $x_{i+1} = x_i + v_{x,i} \Delta t$
   - $y_{i+1} = y_i + v_{y,i} \Delta t$

## Final Result

* ODEs: $\dot{v}_x = -k v v_x$ and $\dot{v}_y = -g - k v v_y$.
* System is non-linear and coupled, requiring numerical solvers.
* Terminal velocity for pure vertical fall ($v_x = 0$) occurs when $mg = c v^2 \implies v_{term} = \sqrt{mg/c}$.

## Interpretation

[Image of trajectory comparison: vacuum vs linear drag vs quadratic drag]

Quadratic drag is much more "aggressive" at high speeds than linear drag. At the beginning of a launch, the drag force is at its maximum because $v$ is highest. This causes a significant "flattening" of the initial climb. As the projectile slows down near the peak, the drag force decreases quadratically, allowing gravity to dominate. The descent is characterized by a rapid approach to a terminal velocity, resulting in a nearly vertical drop at the end of the flight path.