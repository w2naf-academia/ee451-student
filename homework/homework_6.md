# EE 451: Communications Systems
# Homework 6 - BER, Link Budgets, and System Analysis

**Topics:** Bit error rate, matched filtering, link budgets, WiFi/cellular systems
**Textbook Reference:** Haykin & Moher, Chapters 10, 11.4-11.7

**Total Points:** 100

---

## Instructions

- Show all work for full credit
- Include units in all final answers
- For link budgets, show the complete calculation chain
- State all assumptions clearly

---

## Problem 1: BER for BPSK (12 points)

A BPSK system operates with $E_b/N_0 = 10$ dB.

**(a)** Convert $E_b/N_0$ to a linear ratio. (2 points)

**(b)** The BER for BPSK is given by: BER = $Q(\sqrt{2E_b/N_0})$. Calculate the BER. (4 points)

**(c)** If the bit rate is 1 Mbps, approximately how many bit errors occur per second? (3 points)

**(d)** What $E_b/N_0$ is required to achieve BER = $10^{-6}$? (3 points)

---

## Problem 2: BER Comparison (15 points)

Compare the BER performance of BPSK, QPSK, and 8-PSK.

**(a)** For BPSK: BER = $Q(\sqrt{2E_b/N_0})$
    For QPSK: BER $\approx Q(\sqrt{2E_b/N_0})$ (approximately same as BPSK)
    For 8-PSK: BER $\approx \frac{2}{3} \cdot Q(\sqrt{6E_b/N_0} \cdot \sin(\pi/8))$

    Calculate the BER for each modulation at $E_b/N_0 = 12$ dB. (6 points)

**(b)** Which modulation has the best BER performance? Why? (3 points)

**(c)** Which modulation has the highest spectral efficiency? (3 points)

**(d)** If you need to transmit 10 Mbps in 5 MHz bandwidth, which modulation should you choose? Consider both BER and spectral efficiency. (3 points)

---

## Problem 3: Matched Filtering (12 points)

**(a)** Explain what a matched filter is and why it's optimal for detecting signals in AWGN. (4 points)

**(b)** For a rectangular pulse of duration T and amplitude A, what is the output SNR of a matched filter? Express in terms of signal energy $E_s$ and noise power spectral density $N_0$. (4 points)

**(c)** A BPSK system uses matched filtering. If the bit energy is $E_b = 10^{-13}$ J and $N_0 = 10^{-20}$ W/Hz, calculate the output SNR. (4 points)

---

## Problem 4: QAM Bit Error Rate (12 points)

For M-QAM, the symbol error rate (SER) is approximately:
SER $\approx 4 \cdot \left(1 - \frac{1}{\sqrt{M}}\right) \cdot Q\left(\sqrt{\frac{3E_s}{N_0(M-1)}}\right)$

For 16-QAM at $E_s/N_0 = 18$ dB:

**(a)** Convert $E_s/N_0$ to linear ratio. (2 points)

**(b)** Calculate the symbol error rate (SER). (4 points)

**(c)** For Gray coding, approximate BER $\approx$ SER/$\log_2(M)$. Calculate the BER. (3 points)

**(d)** If the symbol rate is 10 Msymbols/s, what is the bit rate and how many bit errors per second occur? (3 points)

---

## Problem 5: Complete Link Budget - WiFi (18 points)

A WiFi 6 system operates at 5 GHz with the following parameters:
- Transmit power: $P_t = 23$ dBm (200 mW, FCC limit for 5 GHz)
- Transmit antenna gain: $G_t = 3$ dBi
- Receive antenna gain: $G_r = 0$ dBi (laptop internal antenna)
- Frequency: 5.0 GHz
- Distance: 30 m
- System bandwidth: 80 MHz
- Noise figure: NF = 6 dB
- Temperature: T = 290 K
- Implementation loss: 3 dB
- Fade margin: 10 dB

**(a)** Calculate free-space path loss using: FSPL(dB) = $20 \cdot \log_{10}(4\pi d/\lambda)$, where $\lambda = c/f$. (4 points)

**(b)** Calculate received signal power $P_r$ including all gains and losses. (4 points)

**(c)** Calculate noise power $P_n$ in the 80 MHz bandwidth. (3 points)

**(d)** Calculate the SNR. (2 points)

**(e)** Based on the SNR, what is the highest modulation that can be used? Use these thresholds:
- BPSK/QPSK: 5 dB
- 16-QAM: 12 dB
- 64-QAM: 20 dB
- 256-QAM: 28 dB
- 1024-QAM: 35 dB
(3 points)

**(f)** Calculate the maximum data rate (assuming ideal spectral efficiency and no overhead). (2 points)

---

## Problem 6: Link Budget - Cellular 5G (15 points)

A 5G base station communicates with a smartphone at 3.5 GHz:
- Base station transmit power: $P_t = 43$ dBm (20 W)
- Base station antenna gain: $G_t = 15$ dBi (directional)
- Smartphone antenna gain: $G_r = -2$ dBi
- Distance: 500 m
- Path loss exponent: n = 3.5 (urban environment)
- Shadow fading margin: 8 dB
- Bandwidth: 100 MHz
- Noise figure: NF = 7 dB

**(a)** Calculate path loss using: PL(dB) = FSPL($d_0$) + $10n \cdot \log_{10}(d/d_0)$, where $d_0 = 1$ m. (5 points)

**(b)** Calculate received power. (3 points)

**(c)** Calculate noise power. (2 points)

**(d)** Calculate SNR. (2 points)

**(e)** Using Shannon's theorem $C = B \cdot \log_2(1 + \text{SNR})$, calculate the theoretical channel capacity. (3 points)

---

## Problem 7: WiFi vs. Cellular Comparison (10 points)

**(a)** Compare the link budgets from Problems 5 and 6. Which system can communicate over longer distances? Why? (4 points)

**(b)** Which system provides higher data rates? Explain the trade-offs. (3 points)

**(c)** Explain why cellular systems use higher transmit power and higher antenna gain compared to WiFi. (3 points)

---

## Problem 8: Adaptive Modulation System (12 points)

A wireless link uses adaptive modulation with the following SNR thresholds:
- QPSK: 8 dB, data rate = 20 Mbps
- 16-QAM: 15 dB, data rate = 40 Mbps
- 64-QAM: 22 dB, data rate = 60 Mbps
- 256-QAM: 30 dB, data rate = 80 Mbps

The received SNR varies with distance as: SNR(dB) = $45 - 30 \cdot \log_{10}(d/10)$, where d is in meters.

**(a)** Calculate the SNR at distances of 10 m, 20 m, 50 m, and 100 m. (4 points)

**(b)** For each distance, determine which modulation scheme is used. (4 points)

**(c)** Calculate the average data rate if the user spends equal time at each of these four distances. (2 points)

**(d)** What is the maximum distance at which communication is possible (SNR $\geq$ 8 dB)? (2 points)

---

## Problem 9: Multipath and Fading (10 points)

**(a)** Explain how multipath propagation affects wireless communication systems. (3 points)

**(b)** What is frequency-selective fading and why does it occur? (3 points)

**(c)** How do OFDM-based systems (WiFi, LTE, 5G) mitigate frequency-selective fading? (4 points)

---

## Problem 10: Real-World System Design (14 points - Challenge)

You are designing a long-range WiFi link for a rural area:
- Frequency: 2.4 GHz (better propagation than 5 GHz)
- Required distance: 1 km
- Required data rate: 50 Mbps
- Available transmit power: 30 dBm (1 W)
- Available antennas: $G_t = G_r = 10$ dBi (directional)
- Bandwidth: 20 MHz
- Temperature: T = 290 K
- Noise figure: NF = 5 dB
- Required SNR for 64-QAM: 22 dB
- Fade margin: 15 dB (for reliability)

**(a)** Calculate the free-space path loss at 1 km and 2.4 GHz. (3 points)

**(b)** Calculate the link budget and determine the received SNR. (5 points)

**(c)** Can the system achieve the required SNR of 22 dB with 15 dB fade margin? (2 points)

**(d)** If not, suggest three modifications to improve the link budget and calculate the improvement from each. (4 points)

---

## Bonus Problem 1: Friis Transmission Equation (5 points extra credit)

The Friis transmission equation relates received power to transmitted power:
$P_r = P_t \cdot G_t \cdot G_r \cdot \left(\frac{\lambda}{4\pi d}\right)^2$

**(a)** Derive the free-space path loss formula FSPL(dB) = $20 \cdot \log_{10}(d) + 20 \cdot \log_{10}(f) + 32.45$ (with d in km and f in MHz) from the Friis equation. (3 points)

**(b)** Verify your derivation by calculating FSPL at d = 1 km and f = 1 GHz. (2 points)

---

## Bonus Problem 2: Eb/N0 vs. SNR Relationship (5 points extra credit)

For a digital communication system:
- Bit rate: $R_b$
- Bandwidth: B
- SNR = signal power / noise power
- $E_b/N_0$ = bit energy / noise power spectral density

**(a)** Show that $E_b/N_0 = \text{SNR} \cdot (B/R_b)$. (3 points)

**(b)** For QPSK with $R_b = 10$ Mbps in B = 5 MHz, if SNR = 12 dB, calculate $E_b/N_0$. (2 points)

---

**Submission Instructions:**
- Submit a single PDF via Brightspace
- Show complete link budget calculations
- Include all unit conversions (dB $\leftrightarrow$ linear)
- Clearly label each step

**Academic Integrity:**
- Individual work required
- Show all work for partial credit
- Cite any references to standards or specifications

**Useful Formulas:**
- FSPL(dB) = $20 \cdot \log_{10}(d) + 20 \cdot \log_{10}(f) + 32.45$ (d in km, f in MHz)
- FSPL(dB) = $20 \cdot \log_{10}(4\pi d/\lambda)$ (d and $\lambda$ in same units)
- $P_n = k \cdot T \cdot B$ (thermal noise)
- $k = 1.38 \times 10^{-23}$ J/K
- $c = 3 \times 10^8$ m/s
- Shannon: $C = B \cdot \log_2(1 + \text{SNR})$
