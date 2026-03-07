# Task 06 – Motion with Linear Drag

## Problem Statement

The drag force is given by the formula:

$$
F = -kv
$$

Initial conditions: $v(0) = v_0$, $x(0) = 0$.

* Write down the equation of motion and solve it.
* Investigate the limit $\lim_{t\to\infty} v(t)$.
* Compare with motion without drag.

## Theory

When an object moves through a fluid, it experiences a resistive force known as drag. At low speeds, this force is often proportional to the velocity ($F \propto v$), which is known as linear drag or Stokes' drag.

According to Newton's Second Law:

$$
m \frac{dv}{dt} = \sum F
$$

In this horizontal case, the only force acting on the body is the drag force. The negative sign indicates that the force always acts in the direction opposite to the velocity vector, leading to deceleration.

## Step-by-Step Solution

### 1. Solving the Equation of Motion

Starting with Newton's Second Law:

$$
m \frac{dv}{dt} = -kv
$$

This is a first-order separable differential equation. We rearrange the terms to isolate $v$ and $t$:

$$
\frac{dv}{v} = -\frac{k}{m} dt
$$

Integrating both sides from the initial state ($t=0, v=v_0$) to an arbitrary state $(t, v)$:

$$
\int_{v_0}^{v} \frac{1}{v'} dv' = -\frac{k}{m} \int_{0}^{t} dt'
$$

$$
\ln(v) - \ln(v_0) = -\frac{k}{m}t
$$

$$
\ln\left( \frac{v}{v_0} \right) = -\frac{k}{m}t
$$

Exponentiating both sides:

$$
v(t) = v_0 e^{-\frac{k}{m}t}
$$

### 2. Velocity Limit

To find the long-term behavior of the velocity, we take the limit as time approaches infinity:

$$
\lim_{t\to\infty} v(t) = \lim_{t\to\infty} v_0 e^{-\frac{k}{m}t}
$$

Since the exponent is negative, the term $e^{-\infty}$ approaches zero:

$$
\lim_{t\to\infty} v(t) = 0
$$

### 3. Comparison with Motion Without Drag

* **Acceleration**: Without drag ($k=0$), the acceleration is zero and velocity remains constant ($v(t) = v_0$). With drag, the acceleration is $a(t) = -\frac{k}{m}v(t)$, which is non-zero and decreases as the object slows down.
* **Velocity Decay**: Without drag, the velocity graph is a horizontal line. With drag, it is an exponential decay curve.
* **Stopping Distance**: Without drag, the object moves infinitely. With drag, we can find the position by integrating velocity:

$$
x(t) = \int_{0}^{t} v_0 e^{-\frac{k}{m}t'} dt' = \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right)
$$

As $t \to \infty$, the object approaches a finite total distance $x_{max} = \frac{mv_0}{k}$.

## Final Result

* **Velocity Equation**: $v(t) = v_0 e^{-\frac{k}{m}t}$
* **Asymptotic Behavior**: The velocity asymptotically approaches zero.
* **Comparison**: Unlike Newton's First Law for vacuum motion (where $v$ is constant), linear drag causes a continuous loss of kinetic energy until the body comes to a rest.

## Interpretation

The parameter $\tau = \frac{m}{k}$ is known as the relaxation time or characteristic time constant. It represents the time required for the velocity to drop to approximately $37\%$ ($1/e$) of its initial value. A larger mass or a smaller drag coefficient increases this time, allowing the object to retain its velocity for longer.