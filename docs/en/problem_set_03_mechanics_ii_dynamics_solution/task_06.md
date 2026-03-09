# Task 06 – Motion with air resistance (Drag force)

## Problem Statement

A body of mass $m$ is moving horizontally with an initial velocity $v(0) = v_0$ at position $x(0) = 0$. The only horizontal force acting on the body is a linear drag force:

$$
F_d = -kv
$$

The required operations are:
1. Write down the equation of motion and solve it to find $v(t)$.
2. Solve the equation to find the position $x(t)$.
3. Investigate the limit $\lim_{t \to \infty} v(t)$.
4. Determine the maximum distance the body can travel.
5. Compare the results with motion without drag.

## Theory

Newton's Second Law states that the net force equals the mass times acceleration:

$$
F = m \frac{dv}{dt}
$$

In this problem, the net force is the drag force $F_d = -kv$. The negative sign indicates that the force acts in the opposite direction of the velocity, causing the body to slow down.

This leads to a first-order linear differential equation. To solve it, we use the method of **separation of variables**. Once the velocity $v(t)$ is known, the position $x(t)$ is found by integrating the velocity with respect to time:

$$
x(t) = x(0) + \int_{0}^{t} v(\tau) \, d\tau
$$

## Step-by-Step Solution

### 1. Solve for velocity $v(t)$

**Step 1: Set up the differential equation**

$$
m \frac{dv}{dt} = -kv
$$

**Step 2: Separate the variables**

Divide by $v$ and multiply by $dt/m$:

$$
\frac{1}{v} \, dv = -\frac{k}{m} \, dt
$$

**Step 3: Integrate both sides**

Integrate from the initial state $(v_0, 0)$ to an arbitrary state $(v, t)$:

$$
\int_{v_0}^{v} \frac{1}{\bar{v}} \, d\bar{v} = -\frac{k}{m} \int_{0}^{t} \, d\tau
$$

$$
\ln|v| - \ln|v_0| = -\frac{k}{m} t
$$

Using logarithm properties:

$$
\ln\left( \frac{v}{v_0} \right) = -\frac{k}{m} t
$$

**Step 4: Solve for $v(t)$**

Exponentiate both sides:

$$
\frac{v(t)}{v_0} = e^{-\frac{k}{m} t}
$$

$$
v(t) = v_0 e^{-\frac{k}{m} t}
$$

### 2. Solve for position $x(t)$

**Step 1: Set up the integral**

$$
x(t) = \int_{0}^{t} v(\tau) \, d\tau = \int_{0}^{t} v_0 e^{-\frac{k}{m} \tau} \, d\tau
$$

**Step 2: Perform the integration**

$$
\begin{align}
x(t) &= v_0 \left[ -\frac{m}{k} e^{-\frac{k}{m} \tau} \right]_0^t \\
     &= -\frac{mv_0}{k} \left( e^{-\frac{k}{m} t} - e^0 \right) \\
     &= -\frac{mv_0}{k} \left( e^{-\frac{k}{m} t} - 1 \right)
\end{align}
$$

Rearranging the terms:

$$
x(t) = \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m} t} \right)
$$

### 3. Investigate the limit $\lim_{t \to \infty} v(t)$

Analyze the behavior of the velocity as time approaches infinity:

$$
\lim_{t \to \infty} v(t) = \lim_{t \to \infty} v_0 e^{-\frac{k}{m} t}
$$

Since the exponent is negative, the term $e^{-\infty}$ approaches zero:

$$
\lim_{t \to \infty} v(t) = 0
$$

The body eventually comes to a complete stop.

### 4. Determine maximum distance

The maximum distance $x_{max}$ is the limit of the position as $t \to \infty$:

$$
\begin{align}
x_{max} &= \lim_{t \to \infty} \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m} t} \right) \\
        &= \frac{mv_0}{k} (1 - 0) \\
        &= \frac{mv_0}{k}
\end{align}
$$

Even though the body theoretically takes an infinite amount of time to stop, it covers a finite distance.

### 5. Compare with motion without drag

In the case without drag ($k = 0$):
- **Velocity:** $v(t) = v_0$ (Constant).
- **Position:** $x(t) = v_0 t$ (Increases linearly without bound).
- **Stopping:** The body never stops.



## Final Result

* Velocity: $v(t) = v_0 e^{-\frac{k}{m} t}$
* Position: $x(t) = \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m} t} \right)$
* Terminal velocity: $0$
* Maximum distance: $x_{max} = \frac{mv_0}{k}$

## Interpretation

The linear drag force creates an exponential decay in velocity. This is physically intuitive: as the body slows down, the drag force decreases, which in turn reduces the rate of deceleration. This "weakening" of the stopping force allows the body to creep forward for an infinite time, yet the rapidly diminishing speed ensures the total displacement is limited to $mv_0/k$. This model is applicable to objects moving at low speeds through viscous fluids (Stokes' drag).