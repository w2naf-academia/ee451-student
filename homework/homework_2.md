# EE 451: Communications Systems
# Homework 2 - Amplitude Modulation and ASK

**Topics:** DSB-SC, full carrier AM, envelope detection, ASK/OOK
**Textbook Reference:** Haykin & Moher, Chapters 3.1-3.3, 7.1-7.2

**Total Points:** 100

---

## Instructions

- Show all work for full credit
- Include units in all final answers
- Sketch waveforms where requested
- You may use Python/MATLAB for verification, but show analytical work

---

## Problem 1: DSB-SC Fundamentals (12 points)

A message signal $m(t) = 5\cos(2\pi \cdot 1000 \cdot t) \text{ V}$ modulates a carrier $c(t) = 10\cos(2\pi \cdot 100 \times 10^3 \cdot t) \text{ V}$ using DSB-SC modulation.

**(a)** Write the expression for the DSB-SC modulated signal $s(t)$. (3 points)

**(b)** Use trigonometric identities to express $s(t)$ as a sum of two sinusoids and identify the upper and lower sideband frequencies. (5 points)

**(c)** What is the bandwidth of the DSB-SC signal? (2 points)

**(d)** What is the power in each sideband if the system has $50 \, \Omega$ resistance? (2 points)

---

## Problem 2: Full Carrier AM (15 points)

An AM broadcast station transmits with a carrier frequency of $1.2 \text{ MHz}$. The carrier amplitude is $A_c = 100 \text{ V}$ and the message signal is $m(t) = 0.6\cos(2\pi \cdot 5000 \cdot t) \text{ V}$.

**(a)** Write the complete expression for the AM signal $s(t)$. (3 points)

**(b)** What is the modulation index $\mu$? (3 points)

**(c)** Sketch one complete cycle of the modulating signal showing the envelope of the AM waveform. Label key amplitudes. (4 points)

**(d)** Calculate the total transmitted power and the percentage of power in the sidebands vs. the carrier (assume $50 \, \Omega$). (5 points)

---

## Problem 3: Modulation Index and Overmodulation (12 points)

An AM transmitter has carrier amplitude $A_c = 50 \text{ V}$.

**(a)** What is the maximum message amplitude $A_m$ that can be used without overmodulation? (3 points)

**(b)** If $m(t) = 40\cos(2\pi \cdot 3000 \cdot t) \text{ V}$, calculate the modulation index and determine if the signal is overmodulated. (3 points)

**(c)** Sketch the AM envelope for $\mu = 0.5$, $\mu = 1.0$, and $\mu = 1.5$. Explain what happens during overmodulation. (6 points)

---

## Problem 4: Envelope Detection (10 points)

An envelope detector is used to demodulate an AM signal. The AM signal has:
- Carrier frequency: $f_c = 900 \text{ kHz}$
- Message signal: $m(t) = \cos(2\pi \cdot 5000 \cdot t)$
- Modulation index: $\mu = 0.8$

**(a)** Sketch a simple envelope detector circuit (diode, RC components). (3 points)

**(b)** What is the requirement on the RC time constant to avoid distortion? Express in terms of the carrier frequency $f_c$ and the maximum message frequency $f_m$. (4 points)

**(c)** What happens if the RC time constant is too large? Too small? (3 points)

---

## Problem 5: AM Bandwidth and Spectral Efficiency (12 points)

An AM radio station broadcasts audio from $50 \text{ Hz}$ to $5 \text{ kHz}$.

**(a)** What is the RF bandwidth required for DSB-SC? For full carrier AM? (4 points)

**(b)** If the station is assigned a carrier frequency of $1050 \text{ kHz}$, what frequencies appear in the transmitted spectrum? (4 points)

**(c)** Calculate the spectral efficiency (bits/s/Hz) if the audio is digitized at 8 bits per sample with Nyquist rate sampling, then transmitted using AM. (4 points)

---

## Problem 6: On-Off Keying (ASK) (15 points)

A binary data stream "1 0 1 1 0" is transmitted using OOK with:
- Bit rate: $R_b = 1000 \text{ bits/s}$
- Carrier frequency: $f_c = 10 \text{ kHz}$
- Carrier amplitude for "1": $A = 5 \text{ V}$
- Carrier amplitude for "0": $0 \text{ V}$

**(a)** Write the expression for the OOK signal during transmission of a "1" bit. (3 points)

**(b)** Sketch the transmitted waveform $s(t)$ for the entire data sequence. Show at least 3 carrier cycles per bit. (5 points)

**(c)** What is the null-to-null bandwidth of the OOK signal? (4 points)

**(d)** How does this compare to the bandwidth of the unmodulated baseband data stream? (3 points)

---

## Problem 7: Binary ASK Spectral Analysis (12 points)

A binary ASK system transmits rectangular pulses at a bit rate of $2400 \text{ bits/s}$ using a carrier frequency of $2.4 \text{ GHz}$ (WiFi band, simplified).

**(a)** What is the bit duration $T_b$? (2 points)

**(b)** The baseband rectangular pulse has a sinc-shaped spectrum. What is the first null bandwidth of the baseband signal? (4 points)

**(c)** After modulation to $f_c = 2.4 \text{ GHz}$, what frequencies define the main lobe of the ASK spectrum? (4 points)

**(d)** Compare the bandwidth efficiency of ASK to DSB-SC AM for the same baseband signal. (2 points)

---

## Problem 8: AM vs. ASK Comparison (10 points)

**(a)** Explain the fundamental difference between analog AM and digital ASK. What do they have in common? (4 points)

**(b)** Both AM and ASK can use envelope detection. Why is this possible? (3 points)

**(c)** Why might ASK be preferred over AM in a digital communication system? (3 points)

---

## Problem 9: Superheterodyne Receiver (12 points - Challenge)

An AM broadcast receiver uses the superheterodyne architecture with an intermediate frequency (IF) of $455 \text{ kHz}$.

**(a)** If you want to receive a station at $1200 \text{ kHz}$, to what frequency should the local oscillator (LO) be tuned? (3 points)

**(b)** What is the image frequency for this receiver? (4 points)

**(c)** If an interfering signal exists at the image frequency, explain what problem this causes. How do receivers mitigate this? (5 points)

---

## Problem 10: Real-World AM System Design (10 points - Challenge)

You are designing an AM transmitter for a campus radio station:
- Carrier frequency: $f_c = 88.5 \text{ MHz}$ (FM band, but using AM for this problem)
- Audio bandwidth: $20 \text{ Hz}$ to $15 \text{ kHz}$
- Maximum transmit power: $100 \text{ W}$
- Carrier amplitude: $A_c = 30 \text{ V}$
- Load resistance: $50 \, \Omega$

**(a)** What is the maximum modulation index you can use to transmit at $100 \text{ W}$ total power? (5 points)

**(b)** What is the RF bandwidth of your transmission? (2 points)

**(c)** If you want to maximize power efficiency (power in sidebands), would you choose DSB-SC or full carrier AM? Justify your answer. (3 points)

---

## Bonus Problem 1: SSB (5 points extra credit)

Single Sideband (SSB) modulation transmits only one sideband, saving bandwidth and power.

**(a)** For a message signal with bandwidth $3 \text{ kHz}$, what is the bandwidth of USB (Upper Sideband) SSB? (2 points)

**(b)** If DSB-SC requires $50 \text{ W}$ to transmit both sidebands, how much power is required for SSB (transmitting one sideband)? (3 points)

---

## Bonus Problem 2: Mathematical Derivation (5 points extra credit)

Starting from $s(t) = A_c[1 + \mu \cdot m_n(t)]\cos(2\pi f_c t)$ where $m_n(t)$ is normalized to $|m_n(t)| \leq 1$:

Show that the carrier power is $P_c = \frac{A_c^2}{2}$ and the total sideband power is $P_{sb} = \frac{\mu^2 A_c^2}{4} \cdot P_m$, where $P_m$ is the normalized message power.

For a single tone $m_n(t) = \cos(2\pi f_m t)$, verify that the efficiency (sideband power / total power) is $\frac{\mu^2}{2 + \mu^2}$.

---

**Submission Instructions:**
- Submit a single PDF via Brightspace
- Include all sketches and waveform drawings
- Label all graphs with frequencies, amplitudes, and time scales
- Show all intermediate steps for calculations

**Academic Integrity:**
- Individual work required
- Cite any external references used
- Discussion of concepts is allowed; copying solutions is not
