# Task 05 – Superposition of waves, beats, and group velocity

## Problem Statement

Two harmonic waves are given:

$$
y_1(x,t)=A\sin(kx-\omega t)
$$

$$
y_2(x,t)=A\sin(kx-(\omega+\Delta\omega)t)
$$

1. Determine the resultant wave $y=y_1+y_2$ and reduce it to a product form (carrier × envelope).
2. Identify the beat frequency and the beat period at the point $x=0$.
3. Interpret physically: what does the envelope describe, and what does the carrier wave describe?
4. Use Python/HTML/JS to generate the two waves and their superposition, showing the phenomenon of beats and the motion of the envelope.

## Theory

[Image of wave superposition and beat frequency envelope]

When two linear waves occupy the same space, they satisfy the superposition principle, meaning their resultant displacement is the algebraic sum of their individual displacements. If the two waves have the same amplitude and wave number but slightly different angular frequencies ($\omega$ and $\omega + \Delta\omega$), their superposition creates an interference pattern that varies in time, known as **beats**.

The sum can be simplified using the trigonometric identity for the sum of two sines:

$$
\sin \alpha + \sin \beta = 2 \cos\left(\frac{\alpha - \beta}{2}\right) \sin\left(\frac{\alpha + \beta}{2}\right)
$$

This product separates the resultant wave into a slowly varying amplitude (the envelope) and a rapidly oscillating function (the carrier wave).

## Step-by-Step Solution

### 1. Determine the resultant wave in product form

The resultant wave $y(x,t)$ is the sum of $y_1$ and $y_2$:

$$
y(x,t) = A\sin(kx-\omega t) + A\sin(kx-(\omega+\Delta\omega)t)
$$

Let us define the arguments:
* $\alpha = kx - \omega t$
* $\beta = kx - (\omega + \Delta\omega)t$

Calculate the sum and difference of these arguments:

$$
\frac{\alpha + \beta}{2} = \frac{2kx - 2\omega t - \Delta\omega t}{2} = kx - \left(\omega + \frac{\Delta\omega}{2}\right)t
$$

$$
\frac{\alpha - \beta}{2} = \frac{(kx - \omega t) - (kx - \omega t - \Delta\omega t)}{2} = \frac{\Delta\omega t}{2}
$$

Substitute these into the trigonometric identity:

$$
\begin{align}
y(x,t) &= 2A \cos\left(\frac{\alpha - \beta}{2}\right) \sin\left(\frac{\alpha + \beta}{2}\right) \\
       &= 2A \cos\left(\frac{\Delta\omega}{2} t\right) \sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)
\end{align}
$$

This expression is in the form of a product:
* **Envelope (Amplitude modulation):** $2A \cos\left(\frac{\Delta\omega}{2} t\right)$
* **Carrier wave:** $\sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)$

### 2. Identify the beat frequency and the beat period at $x=0$

At $x=0$, the resultant wave simplifies to:

$$
y(0,t) = -2A \cos\left(\frac{\Delta\omega}{2} t\right) \sin\left(\left(\omega + \frac{\Delta\omega}{2}\right)t\right)
$$

The intensity of the wave (what we perceive as "loudness" in acoustics) depends on the square of the amplitude envelope. The envelope $E(t) = 2A \cos\left(\frac{\Delta\omega}{2} t\right)$ goes through zero whenever the cosine function is zero. 

Since $|\cos(\theta)|$ repeats twice as fast as $\cos(\theta)$, the angular frequency of the envelope's magnitude (the beat angular frequency) is twice the argument's frequency:

$$
\omega_{\text{beat}} = 2 \left(\frac{\Delta\omega}{2}\right) = \Delta\omega
$$

The beat frequency $f_{\text{beat}}$ (in Hertz) is:

$$
f_{\text{beat}} = \frac{\omega_{\text{beat}}}{2\pi} = \frac{\Delta\omega}{2\pi}
$$

The beat period $T_{\text{beat}}$, which is the time between successive amplitude maxima, is the reciprocal of the beat frequency:

$$
T_{\text{beat}} = \frac{1}{f_{\text{beat}}} = \frac{2\pi}{\Delta\omega}
$$

### 3. Physical interpretation

* **The Carrier Wave:** The term $\sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)$ describes the underlying high-frequency oscillation. Physically, it represents the average perceived pitch or tone of the combined waves, oscillating at the mean angular frequency $\bar{\omega} = \omega + \frac{\Delta\omega}{2}$.
* **The Envelope:** The term $2A \cos\left(\frac{\Delta\omega}{2} t\right)$ acts as a slow, macroscopic modulation of the carrier wave's amplitude. Physically, it describes the "beats"—the periodic swelling and fading of the overall wave intensity. If the two waves have slightly different wave numbers $k$ as well, this envelope travels at the **group velocity**, which governs the speed at which energy or information propagates through a dispersive medium.

## Final Result

- **Resultant wave:** $y(x,t) = \left[ 2A \cos\left(\frac{\Delta\omega}{2} t\right) \right] \sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)$
- **Beat frequency:** $f_{\text{beat}} = \frac{\Delta\omega}{2\pi}$
- **Beat period:** $T_{\text{beat}} = \frac{2\pi}{\Delta\omega}$
- **Interpretation:** The carrier wave dictates the rapid, average-frequency oscillations, while the envelope dictates the slow, macroscopic modulation of amplitude (the beats).

## Interpretation

The phenomenon of beats perfectly illustrates the superposition principle. When the two waves are momentarily in phase, constructive interference doubles the amplitude ($2A$). Half a beat period later, they are $180^\circ$ out of phase, and destructive interference completely cancels the amplitude ($0$). This is utilized practically when tuning musical instruments: a musician plays two notes simultaneously and adjusts one until the beat frequency approaches zero, meaning $\Delta\omega = 0$ and the notes are perfectly in tune.