# Task 05 – Superposition of Waves, Beats, and Group Velocity

## Problem Statement

Two harmonic waves are given:

$$
y_1(x,t) = A \sin(kx - \omega t)
$$

$$
y_2(x,t) = A \sin(kx - (\omega + \Delta\omega)t)
$$

1. Determine the resultant wave $y = y_1 + y_2$ and reduce it to a product form (carrier × envelope).
2. Identify the beat frequency and the beat period at the point $x = 0$.
3. Interpret physically: what does the envelope describe, and what does the carrier wave describe?
4. Use Python/HTML/JS to generate the two waves and their superposition, showing the phenomenon of beats and the motion of the envelope.

## Theory

The principle of superposition states that when two or more waves overlap in a medium, the resultant displacement is the algebraic sum of the individual displacements. When two waves of slightly different frequencies interfere, they produce a pattern of varying amplitude known as **beats**.

This phenomenon is mathematically described using trigonometric identities to separate the fast-oscillating component (the carrier) from the slow-oscillating variation in amplitude (the envelope).



## Step-by-Step Solution

### 1. Resultant Wave in Product Form

The resultant wave is:

$$
y(x,t) = A \left[ \sin(kx - \omega t) + \sin(kx - (\omega + \Delta\omega)t) \right]
$$

Using the trigonometric identity $\sin \alpha + \sin \beta = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right)$, we define:
* $\alpha = kx - \omega t$
* $\beta = kx - \omega t - \Delta\omega t$

**Sum component ($\frac{\alpha + \beta}{2}$):**

$$
\frac{(kx - \omega t) + (kx - \omega t - \Delta\omega t)}{2} = kx - \left(\omega + \frac{\Delta\omega}{2}\right)t
$$

**Difference component ($\frac{\alpha - \beta}{2}$):**

$$
\frac{(kx - \omega t) - (kx - \omega t - \Delta\omega t)}{2} = \frac{\Delta\omega t}{2}
$$

Substituting back into the product form:

$$
y(x,t) = \left[ 2A \cos\left(\frac{\Delta\omega}{2}t\right) \right] \sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)
$$

### 2. Beat Frequency and Period at $x = 0$

At $x = 0$, the expression simplifies to:

$$
y(0,t) = \left[ 2A \cos\left(\frac{\Delta\omega}{2}t\right) \right] \sin\left(-\left(\omega + \frac{\Delta\omega}{2}\right)t\right)
$$

The amplitude term is $|2A \cos(\frac{\Delta\omega}{2}t)|$. A "beat" (maximum loudness or amplitude) occurs twice per cycle of the cosine function (at both the positive and negative peaks).

The angular frequency of the envelope is $\omega_{env} = \frac{\Delta\omega}{2}$. The beat angular frequency $\omega_{beat}$ is twice that of the envelope:

$$
\omega_{beat} = 2 \times \frac{\Delta\omega}{2} = \Delta\omega
$$

The beat frequency $f_{beat}$ is:

$$
f_{beat} = \frac{\Delta\omega}{2\pi} = |f_2 - f_1|
$$

The beat period $T_{beat}$ is:

$$
T_{beat} = \frac{1}{f_{beat}} = \frac{2\pi}{\Delta\omega}
$$

### 3. Physical Interpretation

* **The Carrier Wave**: Represented by the $\sin$ term. It describes the rapid oscillations at the average frequency of the two constituent waves. It represents the "tone" or "pitch" heard in acoustics.
* **The Envelope**: Represented by the $\cos$ term (the amplitude modulator). It describes the slow variation in the total amplitude. In acoustics, this corresponds to the "throbbing" or periodic change in volume.

### 4. Visualization Concept

In a simulation, the two individual waves $y_1$ and $y_2$ would be plotted as thin lines. The resultant wave $y$ would show a high-frequency wave trapped inside a slowly varying "shape." The envelope moves at the **group velocity**, while the carrier waves move through it at the **phase velocity**.

## Final Result

* **Resultant Wave**: $y(x,t) = 2A \cos\left(\frac{\Delta\omega}{2}t\right) \sin\left(kx - (\omega + \frac{\Delta\omega}{2})t\right)$
* **Beat Frequency**: $f_{beat} = \frac{\Delta\omega}{2\pi}$
* **Beat Period**: $T_{beat} = \frac{2\pi}{\Delta\omega}$

## Interpretation

The phenomenon of beats is a direct consequence of the phase relationship between two waves changing over time. Because one wave has a slightly different frequency, it periodically shifts from constructive interference (in-phase) to destructive interference (out-of-phase) and back again. This is a fundamental concept in signal processing and music theory.