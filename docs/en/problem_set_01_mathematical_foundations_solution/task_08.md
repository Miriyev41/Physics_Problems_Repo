# Task 08 – First-Order Differential Equation

## Problem Statement

Given the first-order differential equation:

$$
\frac{dy}{dt} = -k y
$$

1. Solve the equation.
2. Visualize the solution in an HTML/JS application for different values of parameter $k$ and different initial conditions $y(0)$.

## Theory

A differential equation relates an unknown function to its derivatives. The equation $\frac{dy}{dt} = -ky$ is a first-order, linear, and separable ordinary differential equation (ODE). It is one of the most fundamental equations in physics, commonly used to model processes where the rate of change of a quantity is directly proportional to the current amount of that quantity. 

If $k > 0$, the equation describes **exponential decay** (e.g., radioactive decay, discharging a capacitor). If $k < 0$, it describes **exponential growth** (e.g., unconstrained population growth, continuously compounded interest).

The standard method to solve a separable ODE is to move all terms involving the dependent variable ($y$) to one side of the equation and all terms involving the independent variable ($t$) to the other side, and then integrate both sides.

## Step-by-Step Solution

### 1. Separation of variables

Starting with the given differential equation:

$$
\frac{dy}{dt} = -k y
$$

Divide both sides by $y$ and multiply by $dt$ to separate the variables $y$ and $t$:

$$
\frac{1}{y} \, dy = -k \, dt
$$

### 2. Integration of both sides

Integrate both sides of the equation:

$$
\int \frac{1}{y} \, dy = \int -k \, dt
$$

Evaluating the integrals yields:

$$
\ln|y| = -kt + C
$$

where $C$ is an arbitrary constant of integration.

### 3. Solving for y(t)

To isolate $y$, exponentiate both sides of the equation:

$$
\begin{align}
e^{\ln|y|} &= e^{-kt + C} \\
|y| &= e^C \cdot e^{-kt}
\end{align}
$$

Let $A = \pm e^C$. Since $C$ is an arbitrary constant, $A$ can be any non-zero real number. (The case $A=0$ corresponds to the trivial solution $y(t)=0$, which also satisfies the original ODE). We can write the general solution as:

$$
y(t) = A e^{-kt}
$$

### 4. Applying the initial condition

Let the initial condition at time $t = 0$ be $y(0) = y_0$. Substitute $t = 0$ into the general solution:

$$
\begin{align}
y(0) &= A e^{-k(0)} \\
y_0 &= A e^0 \\
y_0 &= A(1) \\
A &= y_0
\end{align}
$$

Substituting $A = y_0$ back into the general solution yields the particular solution.

## Final Result

The solution to the differential equation is:

$$
y(t) = y_0 e^{-kt}
$$

## Interpretation

The solution $y(t) = y_0 e^{-kt}$ demonstrates that the quantity $y$ changes exponentially over time. 

The parameter $y_0$ strictly determines the starting amplitude of the curve. The parameter $k$ determines the rate of the exponential function. A larger positive value of $k$ causes the function to decay more rapidly toward zero. A negative value of $k$ causes the function to grow exponentially toward infinity. The value $k=0$ results in a constant function $y(t) = y_0$, where the rate of change is zero.