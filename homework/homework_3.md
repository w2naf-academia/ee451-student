# EE 451: Communications Systems
# Homework 3 - FM, PM, FSK, and BPSK

**Topics:** Frequency and phase modulation, FSK, BPSK, Carson's rule
**Textbook Reference:** Haykin & Moher, Chapters 4.1-4.8, 7.2-7.4

**Total Points:** 100

---

## Instructions

- Show all work for full credit
- Include units in all final answers
- For bandwidth calculations, clearly state which rule or method you're using
- Sketches should be clearly labeled

---

## Problem 1: FM Fundamentals (10 points)

A message signal $m(t) = 2\cos(2\pi \cdot 1000 \cdot t)$ V modulates an FM carrier with $f_c = 100$ MHz and frequency sensitivity $k_f = 10$ kHz/V.

**(a)** Write the expression for the instantaneous frequency $f_i(t)$. (2 points)

**(b)** What is the maximum frequency deviation $\Delta f$? (2 points)

**(c)** Write the complete FM signal expression $s(t)$. Evaluate the integral to express $s(t)$ in closed form. (3 points)

**(d)** What is the modulation index $\beta$ for FM? (3 points)

---

## Problem 2: Carson's Rule Application (10 points)

An FM broadcast station transmits audio signals with maximum frequency $f_m = 15$ kHz and maximum frequency deviation $\Delta f = 75$ kHz (standard FM broadcasting parameters).

**(a)** Calculate the modulation index $\beta$. (2 points)

**(b)** Use Carson's rule to estimate the FM bandwidth. (2 points)

**(c)** Is this narrowband FM (NBFM) or wideband FM (WBFM)? Justify your answer. (2 points)

**(d)** How does this compare to the bandwidth required for AM broadcasting of the same audio signal? (2 points)

**(e)** What is the advantage of using such a large bandwidth for FM? (2 points)

---

## Problem 3: Narrowband vs. Wideband FM (10 points)

**(a)** For NBFM, the criterion is $\beta \ll 1$. If $f_m = 3$ kHz, what is the maximum $\Delta f$ that qualifies as NBFM? Use $\beta < 0.3$ as the threshold. (2 points)

**(b)** Estimate the bandwidth of NBFM using the small-angle approximation. (3 points)

**(c)** For WBFM with the same $f_m = 3$ kHz but $\Delta f = 30$ kHz, calculate $\beta$ and the bandwidth using Carson's rule. (3 points)

**(d)** Compare the bandwidth efficiency (in terms of $\beta$) between NBFM and WBFM. (2 points)

---

## Problem 4: Phase Modulation (10 points)

A PM signal is given by $s(t) = A_c\cos[2\pi f_c t + k_p m(t)]$ where:

- $A_c = 10$ V
- $f_c = 200$ MHz
- $k_p = 2$ rad/V (phase sensitivity)
- $m(t) = 3\cos(2\pi \cdot 5000 \cdot t)$ V

**(a)** What is the maximum phase deviation $\Delta\phi$? (2 points)

**(b)** Write the expression for the instantaneous phase $\theta_i(t)$. (3 points)

**(c)** Find the instantaneous frequency $f_i(t)$. (3 points)

**(d)** What is the maximum frequency deviation? (2 points)

---

## Problem 5: FM vs. PM Relationship (10 points)

**(a)** Explain the fundamental difference between FM and PM. How are they related? (4 points)

**(b)** If you integrate a message signal before applying it to a phase modulator, what type of modulation do you effectively create? Explain why. (3 points)

**(c)** For the message $m(t) = \cos(2\pi f_m t)$, how does the frequency deviation in FM compare to the frequency deviation in PM as $f_m$ varies? (3 points)

---

## Problem 6: Binary FSK Fundamentals (10 points)

A binary FSK system transmits data at 1200 bits/s using:

- "0" bit: $f_0 = 1200$ Hz
- "1" bit: $f_1 = 2200$ Hz
- Carrier amplitude: $A = 5$ V

**(a)** Write the signal expressions $s_0(t)$ and $s_1(t)$ for the two binary symbols. (2 points)

**(b)** What is the center frequency $f_c$ and the frequency deviation $\Delta f$ (deviation from $f_c$)? (2 points)

**(c)** Calculate the modulation index $h = \frac{2\Delta f}{R_b}$ where $R_b$ is the bit rate. (2 points)

**(d)** For coherent FSK detection, the minimum frequency deviation for orthogonality is $\Delta f = \frac{R_b}{4}$. Is this FSK system using orthogonal tones? (2 points)

**(e)** Estimate the bandwidth using Carson's rule, treating FSK as FM with a rectangular baseband signal. (2 points)

---

## Problem 7: Minimum Shift Keying (MSK) (10 points)

MSK is a special case of continuous-phase FSK (CPFSK) with modulation index $h = 0.5$.

**(a)** If the bit rate is $R_b = 2400$ bps, what is the bit duration $T_b$? (2 points)

**(b)** Given $h = 0.5 = \frac{2\Delta f}{R_b}$, calculate the required frequency deviation $\Delta f$. (2 points)

**(c)** What are the two frequencies $f_0$ and $f_1$ if the center frequency is 1800 Hz? (3 points)

**(d)** Why is MSK preferred over standard FSK in many applications? (3 points)

---

## Problem 8: Binary Phase Shift Keying (BPSK) (10 points)

A BPSK system transmits at 1 Mbps with carrier frequency $f_c = 2.4$ GHz.

**(a)** Write the two possible signal expressions for BPSK representing bits "0" and "1". (2 points)

**(b)** Sketch the constellation diagram for BPSK in the I/Q plane. Label the two signal points. (2 points)

**(c)** What is the phase difference between the two BPSK symbols? (2 points)

**(d)** Calculate the null-to-null bandwidth of the BPSK signal. (2 points)

**(e)** Can BPSK be demodulated using an envelope detector? Why or why not? (2 points)

---

## Problem 9: Coherent vs. Non-Coherent Detection (10 points)

**(a)** Explain the difference between coherent and non-coherent detection. (3 points)

**(b)** Which modulation schemes can use non-coherent detection: ASK, FSK, BPSK? Explain. (4 points)

**(c)** What is the advantage of coherent detection? What is the disadvantage? (3 points)

---

## Problem 10: Real-World Application - FM Stereo Broadcasting (10 points)

Commercial FM stereo radio in the US transmits a composite baseband signal with maximum frequency deviation $\Delta f = 75$ kHz. The composite baseband contains:

- L+R mono audio: 0-15 kHz
- Pilot tone: 19 kHz
- L-R stereo difference on a 38 kHz subcarrier: 23-53 kHz
- RDS (Radio Data System) on a 57 kHz subcarrier: 55.5-58.5 kHz
- Some stations optionally add an SCA (Subsidiary Communications Authorization) subcarrier at 67 kHz for secondary audio services (e.g., background music, reading services for the blind)

**(a)** What is the highest frequency component in the composite baseband signal (not including SCA)? (2 points)

**(b)** Using Carson's rule with $\Delta f = 75$ kHz and the composite baseband bandwidth from (a), estimate the total RF bandwidth of the stereo FM signal. (3 points)

**(c)** FM stations are allocated 200 kHz of bandwidth. Does your calculated bandwidth fit? What does this imply about Carson's rule as an approximation? (3 points)

**(d)** Some stations add an SCA subcarrier at 67 kHz, extending the composite baseband to ~75 kHz. What is the Carson's rule bandwidth now, and how do stations manage to stay within the 200 kHz allocation? (2 points)

---

## Bonus Problem 1: Bessel Functions in FM (5 points extra credit)

The FM spectrum consists of infinite sidebands with amplitudes given by Bessel functions $J_n(\beta)$.

For single-tone FM with $\beta = 2$:
- $J_0(2) = 0.224$
- $J_1(2) = 0.577$
- $J_2(2) = 0.353$
- $J_3(2) = 0.129$
- $J_4(2) = 0.034$

**(a)** Sketch the frequency spectrum showing the carrier and first four sidebands on each side. Label amplitudes relative to carrier (assume $A_c = 10$ V). (3 points)

**(b)** Notice that $J_0(2)$ is small. What does this mean about the carrier power in FM compared to AM? (2 points)

---

## Bonus Problem 2: Frequency Deviation Calculation (5 points extra credit)

For the FM signal $s(t) = 10\cos[2\pi \cdot 100 \times 10^6 \cdot t + 50\sin(2\pi \cdot 1000 \cdot t)]$:

**(a)** Identify the carrier amplitude $A_c$, carrier frequency $f_c$, message frequency $f_m$, and the modulation index $\beta$. (2 points)

**(b)** Calculate the frequency deviation $\Delta f$. Is this NBFM or WBFM? (1 point)

**(c)** Use Carson's rule to estimate the transmission bandwidth. (2 points)

**Hint:** The general form is $s(t) = A_c\cos[2\pi f_c t + \beta\sin(2\pi f_m t)]$ for single-tone FM.

---

**Submission Instructions:**

- Submit a single PDF via Brightspace
- Show all derivations and calculations
- Include clear sketches with labeled axes
- State all assumptions

**Academic Integrity:**

- Individual work required
- You may use textbook formulas and course notes
- Cite any external references
