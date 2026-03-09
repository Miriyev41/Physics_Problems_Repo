# Task 08 – First-order differential equation

## Problem Statement

The following first-order ordinary differential equation is given:

$$
\frac{dy}{dt} = -k y
$$

The required analytical operation is to solve the equation.

The required computational operation is to visualize the solution in an HTML/JS application for different values of the parameter $k$ and different initial conditions $y(0)$.

## Theory

A first-order ordinary differential equation (ODE) relates a function to its first derivative. When the equation can be algebraically manipulated such that all terms involving the dependent variable ($y$) are on one side and all terms involving the independent variable ($t$) are on the other, it is known as a separable differential equation.

The method of separation of variables involves rearranging the equation into the form:

$$
f(y) \, dy = g(t) \, dt
$$

Once separated, we integrate both sides with respect to their respective variables. The resulting constant of integration is determined using an initial condition, typically the value of the function at time zero, $y(0)$.

## Step-by-Step Solution

### 1. Separate the variables

Start with the given differential equation:

$$
\frac{dy}{dt} = -k y
$$

Divide both sides by $y$ (assuming $y \neq 0$) and multiply by the differential $dt$:

$$
\frac{1}{y} \, dy = -k \, dt
$$

### 2. Integrate both sides

Apply the indefinite integral to both sides of the separated equation:

$$
\int \frac{1}{y} \, dy = \int -k \, dt
$$

Evaluate the standard integrals. The integral of $1/y$ is the natural logarithm of the absolute value of $y$, and the integral of a constant is the constant multiplied by the variable of integration:

$$
\ln|y| = -kt + C
$$

Here, $C$ represents an arbitrary constant of integration. (Although each integral produces a constant, they are combined into a single constant $C$ on the right side).

### 3. Solve for $y(t)$

To isolate $y$, exponentiate both sides using base $e$:

$$
e^{\ln|y|} = e^{-kt + C}
$$

Simplify the left side using the inverse property of logarithms and exponentials, and expand the right side using exponent rules:

$$
|y| = e^C e^{-kt}
$$

Let $C_1 = \pm e^C$. Since $e^C$ is a positive constant, allowing for the $\pm$ sign covers both positive and negative values of $y$. If $y=0$, it is a trivial solution that satisfies the original differential equation, meaning $C_1$ can be any real number:

$$
y(t) = C_1 e^{-kt}
$$

### 4. Apply the initial condition

To find the specific value of $C_1$, use the initial condition at $t = 0$, defined as $y(0)$:

$$
\begin{align}
y(0) &= C_1 e^{-k(0)} \\
     &= C_1 e^0 \\
     &= C_1 (1) \\
     &= C_1
\end{align}
$$

Therefore, the constant $C_1$ is exactly equal to the initial value $y(0)$.

Substitute $C_1$ back into the general solution to obtain the particular solution:

$$
y(t) = y(0) e^{-kt}
$$

## Final Result

The general solution to the differential equation is:

$$
y(t) = y(0) e^{-kt}
$$

## Interpretation



This differential equation is the fundamental model for exponential processes. 

When $k > 0$, the solution $y(t)$ represents **exponential decay**. The rate of change of the quantity is directly proportional to its current value, meaning as the quantity decreases, its rate of decrease slows down. This mathematically describes ubiquitous physical phenomena such as radioactive decay, the cooling of a hot object (Newton's law of cooling), or the discharging of a capacitor through a resistor. The parameter $k$ is the decay constant, determining how rapidly the system approaches zero.

When $k < 0$, the exponent becomes positive, representing **exponential growth**, which models unconstrained population growth or continuous compound interest.