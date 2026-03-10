# Task 07 – Vertical throw with drag

## Problem Statement

We have the equation of motion for a vertical throw with linear drag:

$$
m\frac{dv}{dt} = -mg - kv
$$

with initial conditions $v(0)=v_0$, $x(0)=0$.

1. Solve the equation.
2. Determine the maximum height.
3. Compare with the case without drag.
4. Perform a numerical simulation.
5. Compare the analytical and numerical solutions.

## Theory

When an object is thrown vertically upwards in a fluid (like air), it experiences two forces: the constant downward force of gravity ($F_g = -mg$) and a drag force that opposes its motion. For relatively low speeds, Stokes' linear drag applies ($F_d = -kv$).

The net force determines the acceleration via Newton's Second Law. To find the velocity $v(t)$ and position $x(t)$, we must solve the resulting first-order ordinary differential equation (ODE). Since the forces depend on velocity, the acceleration is not constant, and we cannot use simple constant-acceleration kinematics.

## Step-by-Step Solution

### 1. Solve the equation of motion

Starting with the given ODE:

$$
m\frac{dv}{dt} = -mg - kv
$$

Rearrange it to isolate terms with $v$:

$$
\frac{dv}{dt} = -g - \frac{k}{m}v = -\frac{k}{m} \left( v + \frac{mg}{k} \right)
$$

This is a separable differential equation. Separate the variables $v$ and $t$:

$$
\frac{dv}{v + \frac{mg}{k}} = -\frac{k}{m} dt
$$

Integrate both sides:

$$
\int \frac{dv}{v + \frac{mg}{k}} = \int -\frac{k}{m} \, dt
$$

$$
\ln\left| v + \frac{mg}{k} \right| = -\frac{k}{m}t + C
$$

Exponentiate both sides to solve for $v$:

$$
v(t) + \frac{mg}{k} = A e^{-\frac{k}{m}t}
$$

where $A = \pm e^C$. Apply the initial condition $v(0) = v_0$:

$$
\begin{align}
v_0 + \frac{mg}{k} &= A e^0 \\
A &= v_0 + \frac{mg}{k}
\end{align}
$$

Substitute $A$ back to find the exact velocity function:

$$
v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}
$$

To find the position $x(t)$, integrate the velocity function:

$$
\begin{align}
x(t) &= \int v(t) \, dt \\
     &= \int \left[ \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k} \right] dt \\
     &= -\frac{m}{k} \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}t + C_2
\end{align}
$$

Apply the initial condition $x(0) = 0$:

$$
\begin{align}
0 &= -\frac{m}{k} \left( v_0 + \frac{mg}{k} \right) e^0 - 0 + C_2 \\
C_2 &= \frac{m}{k} \left( v_0 + \frac{mg}{k} \right)
\end{align}
$$

Substitute $C_2$ back to find the exact position function:

$$
\begin{align}
x(t) &= \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) - \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}t \\
     &= \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{k}{m}t} \right) - \frac{mg}{k}t
\end{align}
$$

### 2. Determine the maximum height

The object reaches its maximum height when its velocity is zero ($v(t_h) = 0$). First, find the time $t_h$:

$$
0 = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t_h} - \frac{mg}{k}
$$

$$
e^{\frac{k}{m}t_h} = \frac{v_0 + \frac{mg}{k}}{\frac{mg}{k}} = 1 + \frac{k v_0}{mg}
$$

$$
t_h = \frac{m}{k} \ln\left( 1 + \frac{k v_0}{mg} \right)
$$

Substitute $t_h$ into the position function $x(t)$ to find $x_{max}$. Note that from the velocity equation at $t_h$, we know $e^{-\frac{k}{m}t_h} = \left(1 + \frac{k v_0}{mg}\right)^{-1}$.

$$
\begin{align}
x_{max} &= \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - \frac{1}{1 + \frac{k v_0}{mg}} \right) - \frac{mg}{k} \left[ \frac{m}{k} \ln\left( 1 + \frac{k v_0}{mg} \right) \right] \\
        &= \frac{m}{k} \left( \frac{k v_0 + mg}{k} \right) \left( \frac{\frac{k v_0}{mg}}{1 + \frac{k v_0}{mg}} \right) - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{mg} \right) \\
        &= \frac{m v_0}{k} - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{mg} \right)
\end{align}
$$

### 3. Compare with the case without drag

Without drag ($k \to 0$), we recover the standard kinematic equations via Taylor series expansion of the logarithm, or by directly solving $m\ddot{x} = -mg$:
- **Velocity without drag:** $v_{nodrag}(t) = v_0 - gt$
- **Position without drag:** $x_{nodrag}(t) = v_0 t - \frac{1}{2}gt^2$
- **Maximum height without drag:** $x_{max, nodrag} = \frac{v_0^2}{2g}$

When drag is present, the net downward force is greater on the way up ($mg + kv$) than it would be without drag ($mg$). This causes the object to decelerate faster, meaning it takes less time to reach the apex and it reaches a strictly **lower maximum height** ($x_{max} < \frac{v_0^2}{2g}$).

### 4. Numerical simulation & 5. Comparison

A numerical simulation can be performed using the Euler method. We define a small time step $\Delta t$ and iteratively update velocity and position:
1. $a_i = -g - \frac{k}{m}v_i$
2. $v_{i+1} = v_i + a_i \Delta t$
3. $x_{i+1} = x_i + v_i \Delta t$

The HTML application accompanying this task executes this numerical integration simultaneously with the analytical evaluation. Because the Euler method uses a first-order approximation, a slight discrepancy (truncation error) emerges between the exact analytical curve and the numerical points, which shrinks as $\Delta t \to 0$.

## Final Result

- **Velocity:** $v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}$
- **Position:** $x(t) = \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{k}{m}t} \right) - \frac{mg}{k}t$
- **Max Height:** $x_{max} = \frac{m v_0}{k} - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{mg} \right)$
- **Comparison:** The drag force causes a strictly lower maximum height and a non-symmetric trajectory (it takes longer to fall down than it does to rise).

## Interpretation

The term $\frac{mg}{k}$ represents the "terminal velocity" $v_t$ of the object. As $t \to \infty$ (assuming the object falls infinitely), the exponential term vanishes, and $v(t) \to -\frac{mg}{k} = -v_t$. This means the object accelerates downward until the upward drag force exactly balances the downward gravitational force, at which point the net acceleration becomes zero and the object falls at a constant speed.