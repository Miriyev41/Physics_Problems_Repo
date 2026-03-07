# Task 07 – Vertical Throw with Drag

## Problem Statement

A body is thrown vertically with an initial velocity $v_0$ from an initial position $x(0) = 0$. The motion is governed by the following equation:

$$
m \frac{dv}{dt} = -mg - kv
$$

* Solve the equation of motion for $v(t)$.
* Determine the maximum height reached by the body.
* Compare the result with the case without air resistance ($k = 0$).
* Perform a numerical simulation comparison (conceptual).

## Theory

Vertical motion with linear drag involves two forces acting in the downward direction during the upward phase: gravity and air resistance. Unlike horizontal motion, the body reaches a terminal velocity if falling, but during an upward throw, both forces work together to decelerate the object faster than gravity alone.

The equation is a first-order linear differential equation:

$$
\frac{dv}{dt} + \frac{k}{m}v = -g
$$



## Step-by-Step Solution

### 1. Solving for Velocity $v(t)$

We use the method of separation of variables:

$$
\frac{dv}{g + \frac{k}{m}v} = -dt
$$

Integrating from $t = 0$ ($v = v_0$) to $t$ ($v = v$):

$$
\int_{v_0}^{v} \frac{dv'}{g + \frac{k}{m}v'} = -\int_{0}^{t} dt'
$$

The integral on the left results in a natural logarithm:

$$
\frac{m}{k} \ln \left( \frac{g + \frac{k}{m}v}{g + \frac{k}{m}v_0} \right) = -t
$$

Solving for $v(t)$:

$$
g + \frac{k}{m}v = \left( g + \frac{k}{m}v_0 \right) e^{-\frac{k}{m}t}
$$

$$
v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}
$$

### 2. Maximum Height

The maximum height $H$ is reached when the velocity becomes zero ($v(t_s) = 0$). First, find the stopping time $t_s$:

$$
0 = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t_s} - \frac{mg}{k} \implies e^{-\frac{k}{m}t_s} = \frac{mg}{mg + kv_0}
$$

To find the position $x(t)$, we integrate $v(t)$:

$$
x(t) = \int_{0}^{t} \left[ \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t'} - \frac{mg}{k} \right] dt'
$$

$$
x(t) = \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{k}{m}t} \right) - \frac{mgt}{k}
$$

Substituting $e^{-\frac{k}{m}t_s}$ into the position equation for $H$:

$$
H = \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - \frac{mg}{mg + kv_0} \right) - \frac{mg t_s}{k}
$$

$$
H = \frac{mv_0}{k} - \frac{m^2g}{k^2} \ln \left( 1 + \frac{kv_0}{mg} \right)
$$

### 3. Comparison with Vacuum Case ($k \to 0$)

In a vacuum, the maximum height is $H_{vac} = \frac{v_0^2}{2g}$. Using the Taylor expansion for $\ln(1+x) \approx x - \frac{x^2}{2}$ for the result in section 2:

$$
H \approx \frac{mv_0}{k} - \frac{m^2g}{k^2} \left[ \frac{kv_0}{mg} - \frac{1}{2} \left( \frac{kv_0}{mg} \right)^2 \right] = \frac{mv_0}{k} - \frac{mv_0}{k} + \frac{v_0^2}{2g} = H_{vac}
$$

This confirms that as drag becomes negligible, the solution converges to the standard kinematic formula.

## Final Result

* **Velocity**: $v(t) = (v_0 + v_{term})e^{-t/\tau} - v_{term}$, where $v_{term} = \frac{mg}{k}$ and $\tau = \frac{m}{k}$.
* **Max Height**: $H = \frac{mv_0}{k} - \frac{m^2g}{k^2} \ln(1 + \frac{kv_0}{mg})$.

## Interpretation

The inclusion of air resistance reduces the maximum height reached compared to a vacuum. Because the drag force always opposes motion, it aids gravity on the way up, leading to a shorter ascent time and a lower peak. The term $\frac{mg}{k}$ represents the terminal velocity the object would reach if it were falling, acting here as a scaling factor for the resistive effects.