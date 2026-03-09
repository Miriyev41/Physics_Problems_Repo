# Task 07 – Vertical throw with drag

## Problem Statement

A body of mass $m$ is thrown vertically upward with an initial velocity $v(0) = v_0$ from the initial position $y(0) = 0$. The motion is subject to gravity and a linear air resistance force $F_d = -kv$.

The equation of motion is given as:

$$
m\frac{dv}{dt} = -mg - kv
$$

The required operations are:
1. Solve the differential equation to find the velocity $v(t)$.
2. Determine the maximum height $H_{max}$ reached by the body.
3. Compare the result with the case without drag.
4. Perform a numerical simulation (HTML/JS) and compare analytical and numerical solutions.

## Theory

In a vertical throw with air resistance, two forces act on the body during its ascent: the constant force of gravity $mg$ and the velocity-dependent drag force $kv$. Both forces point downward (opposite to the initial upward velocity), leading to a faster deceleration than in a vacuum.

The governing equation is a first-order linear non-homogeneous differential equation:

$$
\frac{dv}{dt} + \frac{k}{m}v = -g
$$

This can be solved using the method of separating variables or by using an integrating factor. The maximum height is reached at the instant $t_s$ when the velocity becomes zero ($v(t_s) = 0$). The height is found by integrating the velocity function:

$$
y(t) = \int_0^t v(\tau) \, d\tau
$$

## Step-by-Step Solution

### 1. Solve for velocity $v(t)$

**Step 1: Separate the variables**

Rearrange the equation of motion:

$$
\frac{dv}{dt} = -\left( g + \frac{k}{m}v \right)
$$

$$
\frac{dv}{g + \frac{k}{m}v} = -dt
$$

**Step 2: Integrate both sides**

Integrate from $v_0$ to $v(t)$ and from $0$ to $t$:

$$
\int_{v_0}^{v} \frac{d\bar{v}}{g + \frac{k}{m}\bar{v}} = -\int_0^t d\tau
$$

Let $u = g + \frac{k}{m}\bar{v}$, then $du = \frac{k}{m}d\bar{v}$:

$$
\frac{m}{k} \ln \left| g + \frac{k}{m}\bar{v} \right|_{v_0}^v = -t
$$

$$
\ln \left( \frac{g + \frac{k}{m}v}{g + \frac{k}{m}v_0} \right) = -\frac{k}{m}t
$$

**Step 3: Isolate $v(t)$**

$$
\frac{g + \frac{k}{m}v}{g + \frac{k}{m}v_0} = e^{-\frac{k}{m}t}
$$

$$
v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}
$$

### 2. Determine the maximum height $H_{max}$

**Step 1: Find the stopping time $t_s$**

Set $v(t_s) = 0$:

$$
0 = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t_s} - \frac{mg}{k}
$$

$$
e^{-\frac{k}{m}t_s} = \frac{\frac{mg}{k}}{v_0 + \frac{mg}{k}} = \frac{mg}{kv_0 + mg}
$$

Taking the natural logarithm:

$$
t_s = \frac{m}{k} \ln \left( 1 + \frac{kv_0}{mg} \right)
$$

**Step 2: Integrate velocity to find $y(t)$**

$$
\begin{align}
y(t) &= \int_0^t \left[ \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}\tau} - \frac{mg}{k} \right] d\tau \\
     &= \left( v_0 + \frac{mg}{k} \right) \left[ -\frac{m}{k} e^{-\frac{k}{m}\tau} \right]_0^t - \frac{mg}{k}t \\
     &= \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{k}{m}t} \right) - \frac{mg}{k}t
\end{align}
$$

**Step 3: Evaluate at $t_s$**

Substitute $e^{-\frac{k}{m}t_s} = \frac{mg}{kv_0 + mg}$ and $t_s$:

$$
\begin{align}
H_{max} &= \frac{m}{k} \left( \frac{kv_0 + mg}{k} \right) \left( 1 - \frac{mg}{kv_0 + mg} \right) - \frac{mg}{k} \left[ \frac{m}{k} \ln \left( 1 + \frac{kv_0}{mg} \right) \right] \\
        &= \frac{mv_0}{k} - \frac{m^2 g}{k^2} \ln \left( 1 + \frac{kv_0}{mg} \right)
\end{align}
$$

### 3. Compare with the case without drag

In a vacuum ($k \to 0$), we use the Taylor expansion $\ln(1+x) \approx x - \frac{x^2}{2} + \frac{x^3}{3}$:

$$
\begin{align}
H_{max} &\approx \frac{mv_0}{k} - \frac{m^2 g}{k^2} \left[ \frac{kv_0}{mg} - \frac{1}{2} \left( \frac{kv_0}{mg} \right)^2 \right] \\
        &= \frac{mv_0}{k} - \left[ \frac{mv_0}{k} - \frac{v_0^2}{2g} \right] \\
        &= \frac{v_0^2}{2g}
\end{align}
$$

This confirms that the result reduces to the standard kinematic formula $H = \frac{v_0^2}{2g}$ when resistance is neglected. With drag ($k > 0$), the logarithmic term ensures $H_{max}$ is always strictly smaller than the vacuum height.

## Final Result

* Velocity: $v(t) = (v_0 + \frac{mg}{k})e^{-\frac{k}{m}t} - \frac{mg}{k}$
* Stopping time: $t_s = \frac{m}{k} \ln(1 + \frac{kv_0}{mg})$
* Max Height: $H_{max} = \frac{mv_0}{k} - \frac{m^2 g}{k^2} \ln(1 + \frac{kv_0}{mg})$
* Comparison: $H_{with\ drag} < H_{vacuum}$

## Interpretation

[Image of velocity-time graph for a vertical throw with linear air resistance]

The presence of air resistance during an upward throw results in a "shorter" and "faster" ascent compared to a vacuum. Because the drag force helps gravity pull the object down during the upward phase, the object loses its initial kinetic energy more rapidly. This leads to a lower peak height and a significantly shorter time to reach that peak. Physically, the term $mg/k$ represents the terminal velocity; in this upward throw model, it acts as a scaling factor for how quickly the atmosphere "saps" the momentum from the projectile.