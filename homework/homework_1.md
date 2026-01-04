# EE 451: Communications Systems
# Homework 1 - Complex Numbers, Phasors, and Signal Operations

**Topics:** Complex numbers, Euler's formula, phasors, signal energy and power
**Textbook Reference:** Haykin & Moher, Chapter 2.1

**Total Points:** 100

---

## Instructions

- Show all work for full credit
- Include units in all final answers
- Box or clearly indicate your final answers
- You may use Python/MATLAB for verification, but show analytical work

---

## Problem 1: Complex Number Arithmetic (10 points)

Given two complex numbers:
- $z_1 = 3 + 4j$
- $z_2 = 2 - 5j$

Calculate the following:

**(a)** $z_1 + z_2$ (2 points)

**(b)** $z_1 \cdot z_2$ (3 points)

**(c)** $\frac{z_1}{z_2}$ (express in both rectangular and polar form) (5 points)

---

## Problem 2: Polar and Rectangular Conversion (12 points)

Convert the following complex numbers between rectangular and polar forms:

**(a)** Convert $z = -6 + 8j$ to polar form (magnitude and phase in degrees) (4 points)

**(b)** Convert $z = 15\angle -135°$ to rectangular form (4 points)

**(c)** A signal has magnitude 10 V and phase $-60°$. Express this in rectangular form and verify that $|z|^2$ equals the sum of the squares of the real and imaginary parts. (4 points)

---

## Problem 3: Euler's Formula Application (12 points)

Using Euler's formula $e^{j\theta} = \cos(\theta) + j\sin(\theta)$:

**(a)** Express $\cos(\omega t)$ as the real part of a complex exponential. (4 points)

**(b)** Express $\sin(\omega t + \phi)$ as the imaginary part of a complex exponential. (4 points)

**(c)** Prove the trigonometric identity:
$$\cos(A)\cos(B) = \frac{1}{2}[\cos(A+B) + \cos(A-B)]$$
using Euler's formula. (4 points)

---

## Problem 4: Phasor Addition (15 points)

Two sinusoidal voltages are added together:
- $v_1(t) = 10\cos(2\pi \cdot 1000 \cdot t + 30°)$ V
- $v_2(t) = 15\cos(2\pi \cdot 1000 \cdot t - 45°)$ V

**(a)** Convert each voltage to phasor form. (4 points)

**(b)** Add the phasors to find the resultant phasor $V_{\text{total}}$. (5 points)

**(c)** Convert the resultant phasor back to a time-domain sinusoid $v_{\text{total}}(t)$. (4 points)

**(d)** Verify your answer using Python or MATLAB (optional, 2 points extra credit).

---

## Problem 5: I/Q Representation (15 points)

A communication signal is represented as:
$$s(t) = I(t)\cos(2\pi f_c t) - Q(t)\sin(2\pi f_c t)$$

where $I(t) = 5$ V and $Q(t) = 12$ V are constant values, and $f_c = 900$ MHz.

**(a)** Express $s(t)$ as a single sinusoid in the form $A\cos(2\pi f_c t + \phi)$. Find $A$ and $\phi$. (7 points)

**(b)** What is the complex envelope of this signal? (4 points)

**(c)** Sketch the position of this signal in the I/Q plane (complex plane). (4 points)

---

## Problem 6: Signal Energy (12 points)

Consider the rectangular pulse signal:

$$x(t) = \begin{cases}
5 \text{ V}, & 0 \leq t \leq 2 \text{ seconds} \\
0, & \text{otherwise}
\end{cases}$$

**(a)** Calculate the energy of this signal. (6 points)

**(b)** Is this an energy signal or a power signal? Justify your answer. (3 points)

**(c)** What would be the energy if the amplitude doubled to 10 V? (3 points)

---

## Problem 7: Power Signal Analysis (15 points)

A periodic signal is given by:
$$x(t) = 10\cos(2\pi \cdot 60 \cdot t) + 5\sin(2\pi \cdot 120 \cdot t) \text{ V}$$

**(a)** Calculate the average power of each frequency component separately. (6 points)

**(b)** Calculate the total average power of the signal. (4 points)

**(c)** Is this an energy signal or a power signal? Explain. (3 points)

**(d)** What is the period of the composite signal? (2 points)

---

## Problem 8: Convolution Fundamentals (9 points)

The unit step function is defined as:

$$u(t) = \begin{cases}
1, & t \geq 0 \\
0, & t < 0
\end{cases}$$

**(a)** Sketch the signal $x(t) = u(t) - u(t-3)$. (3 points)

**(b)** What is the relationship between the unit step $u(t)$ and the unit impulse $\delta(t)$? (3 points)

**(c)** Evaluate the integral:
$$\int_{-\infty}^{\infty} x(\tau)\delta(\tau-2) \, d\tau$$
where $x(t)$ is defined in part (a). (3 points)

---

## Problem 9: Real-World Application - WiFi Signal (10 points - Challenge)

A WiFi signal at 2.4 GHz has I and Q components:
- $I(t) = 3\cos(2\pi \cdot 100 \cdot t)$ V
- $Q(t) = 4\cos(2\pi \cdot 100 \cdot t)$ V

where the 100 Hz represents a slow modulating signal (in reality, WiFi modulation is much faster, but we're simplifying).

**(a)** Express the complete RF signal $s(t) = I(t)\cos(2\pi f_c t) - Q(t)\sin(2\pi f_c t)$ where $f_c = 2.4$ GHz. (4 points)

**(b)** What is the instantaneous magnitude of the complex envelope at $t = 0$? (3 points)

**(c)** Explain why modern software-defined radios (like the RTL-SDR) output I and Q samples rather than the full RF signal $s(t)$. (3 points)

---

## Problem 10: Conceptual Understanding (10 points)

Answer the following short-answer questions (2-3 sentences each):

**(a)** Why is phasor representation useful in analyzing communication systems? (3 points)

**(b)** What is the physical meaning of the phase angle in a complex number representing a sinusoid? (3 points)

**(c)** Explain the difference between the complex envelope and the actual RF carrier signal in a communication system. (4 points)

---

## Bonus Problem (5 points extra credit)

Prove that for any complex number $z = a + jb$:
$$z \cdot z^* = |z|^2$$

where $z^*$ is the complex conjugate of $z$, and $|z|$ is the magnitude of $z$.

Then explain why this property is useful for calculating signal power in communication systems.

---

**Submission Instructions:**
- Submit a single PDF via Brightspace
- Scanned handwritten work is acceptable if legible
- Include any code used for verification

**Academic Integrity:**
- You may discuss concepts with classmates, but all submitted work must be your own
- Show your work - answers without supporting calculations will receive minimal credit
