# EE 451: Communications Systems
# Homework 4 - M-ary Modulation, QAM, and EVM

**Topics:** QPSK, M-ary PSK, QAM, spectral efficiency, EVM, WiFi/cellular modulation
**Textbook Reference:** Haykin & Moher, Chapter 7.5-7.7

**Total Points:** 100

---

## Instructions

- Show all work for full credit
- Include units in all final answers
- Constellation diagrams should be clearly labeled with I/Q axes
- For system design problems, state all assumptions

---

## Problem 1: QPSK Fundamentals (15 points)

A QPSK system transmits at 10 Mbps with carrier frequency $f_c = 1.8$ GHz.

**(a)** How many bits does each symbol represent? What is the symbol rate? (4 points)

**(b)** Write the four possible signal expressions for QPSK. Use phases 45°, 135°, 225°, and 315°. (6 points)

**(c)** Draw the constellation diagram showing all four symbols in the I/Q plane. Label each point with its corresponding bit pattern using Gray coding. (5 points)

---

## Problem 2: QPSK Gray Coding (12 points)

**(a)** Explain what Gray coding is and why it's used in digital modulation. (4 points)

**(b)** For the QPSK constellation in Problem 1, assign 2-bit patterns to each symbol using Gray coding such that adjacent symbols differ by only one bit. (4 points)

**(c)** If a symbol error causes the receiver to select an adjacent symbol, how many bit errors occur with Gray coding? Without Gray coding? (4 points)

---

## Problem 3: M-ary PSK Performance (12 points)

Consider 8-PSK modulation with symbol rate $R_s = 5$ Msymbols/s.

**(a)** What is the bit rate $R_b$? (3 points)

**(b)** What is the phase separation between adjacent symbols? (3 points)

**(c)** Draw the 8-PSK constellation diagram with Gray coding. (4 points)

**(d)** What is the null-to-null RF bandwidth? (2 points)

---

## Problem 4: QAM Constellation Design (15 points)

A 16-QAM system uses a rectangular constellation.

**(a)** How many bits per symbol does 16-QAM transmit? (2 points)

**(b)** Sketch a 16-QAM constellation diagram. Use amplitude levels $\{\pm 1, \pm 3\}$ for both I and Q. Label all 16 points with 4-bit Gray-coded patterns. (6 points)

**(c)** If the symbol rate is 10 Msymbols/s, what is the bit rate? (3 points)

**(d)** What is the average symbol energy if the unit amplitude is 1 V and the system resistance is $50 \, \Omega$? (4 points)

---

## Problem 5: Spectral Efficiency Comparison (15 points)

Compare the spectral efficiency (bits/s/Hz) of the following modulation schemes, all operating at 20 MHz RF bandwidth:

**(a)** BPSK (3 points)

**(b)** QPSK (3 points)

**(c)** 16-QAM (3 points)

**(d)** 64-QAM (3 points)

**(e)** Which modulation scheme provides the highest data rate in 20 MHz? What is that data rate? (3 points)

---

## Problem 6: Error Vector Magnitude (EVM) (12 points)

An ideal QPSK symbol is located at $I = 1.0$ V, $Q = 0$ V. A received symbol is measured at $I = 0.92$ V, $Q = 0.15$ V.

**(a)** Plot both the ideal and received symbol positions on an I/Q diagram. Draw the error vector. (4 points)

**(b)** Calculate the error vector magnitude (EVM) in volts. (4 points)

**(c)** Calculate the EVM as a percentage: EVM% = $\frac{\text{EVM}}{\text{Reference}} \times 100\%$, where the reference is the distance from the origin to the ideal symbol. (2 points)

**(d)** What does EVM measure in a communication system? (2 points)

---

## Problem 7: WiFi Modulation Schemes (12 points)

WiFi 6 (802.11ax) can use BPSK, QPSK, 16-QAM, 64-QAM, 256-QAM, and 1024-QAM depending on channel conditions.

**(a)** Fill in the table below:

| Modulation | Bits/Symbol | Symbol Rate (Msym/s) for 40 MHz channel | Data Rate (Mbps) |
|------------|-------------|------------------------------------------|------------------|
| BPSK       |             | 40                                       |                  |
| QPSK       |             | 40                                       |                  |
| 16-QAM     |             | 40                                       |                  |
| 64-QAM     |             | 40                                       |                  |
| 256-QAM    |             | 40                                       |                  |
| 1024-QAM   |             | 40                                       |                  |

(6 points)

**(b)** Why doesn't WiFi always use 1024-QAM for maximum throughput? (3 points)

**(c)** What is adaptive modulation and coding (AMC)? How does WiFi decide which modulation to use? (3 points)

---

## Problem 8: LTE and 5G Modulation (10 points)

LTE and 5G NR use QPSK, 16-QAM, 64-QAM, and 256-QAM.

**(a)** An LTE system has 20 MHz bandwidth and uses 64-QAM. Assuming ideal spectral efficiency (bits/s/Hz equals bits/symbol), what is the theoretical maximum data rate? (4 points)

**(b)** In practice, LTE achieves about 75% of the theoretical maximum due to overhead (control channels, guard bands, cyclic prefix). What is the practical data rate? (2 points)

**(c)** 5G NR can use 100 MHz bandwidth with 256-QAM. What is the theoretical data rate? (2 points)

**(d)** Why can 5G use wider bandwidths than LTE? (2 points)

---

## Problem 9: Power Efficiency vs. Spectral Efficiency (15 points - Challenge)

**(a)** Explain the trade-off between power efficiency and spectral efficiency in M-ary modulation schemes. (5 points)

**(b)** For a fixed bit rate of 100 Mbps, compare the symbol rate required for QPSK vs. 16-QAM. Which requires higher bandwidth? (5 points)

**(c)** In a power-limited system (e.g., satellite communication), would you prefer QPSK or 16-QAM? In a bandwidth-limited system (e.g., urban cellular), which would you prefer? Justify your answers. (5 points)

---

## Problem 10: Real-World System Design - 5G NR (12 points - Challenge)

You are designing a 5G NR downlink with the following specifications:
- Carrier frequency: 3.5 GHz
- Channel bandwidth: 100 MHz
- Target data rate: 500 Mbps
- Available modulation schemes: QPSK, 16-QAM, 64-QAM, 256-QAM

**(a)** Assuming ideal spectral efficiency (no overhead), which modulation scheme(s) can achieve the 500 Mbps target? (4 points)

**(b)** If overhead reduces efficiency to 70% of theoretical, which modulation schemes can still meet the target? (4 points)

**(c)** The link budget analysis shows SNR = 25 dB. Based on typical SNR requirements below, which modulation should you choose?

- QPSK: 5-10 dB
- 16-QAM: 10-15 dB
- 64-QAM: 18-23 dB
- 256-QAM: 25-30 dB

(4 points)

---

## Bonus Problem 1: OFDM and Spectral Efficiency (5 points extra credit)

WiFi and LTE use OFDM (Orthogonal Frequency Division Multiplexing) with QAM on each subcarrier.

**(a)** If WiFi uses 52 subcarriers (802.11a/g) in a 20 MHz channel, and each subcarrier uses 64-QAM, what is the total data rate assuming ideal conditions? (3 points)

**(b)** How does OFDM improve spectral efficiency compared to single-carrier modulation? (2 points)

---

## Bonus Problem 2: EVM Limits in Standards (5 points extra credit)

WiFi 6 specifies maximum EVM requirements for different modulations:
- BPSK/QPSK: -5 dB (56%)
- 16-QAM: -13 dB (22%)
- 64-QAM: -19 dB (11%)
- 256-QAM: -25 dB (5.6%)
- 1024-QAM: -30 dB (3.2%)

**(a)** Why do higher-order modulations have stricter EVM requirements? (3 points)

**(b)** Convert the EVM requirement for 64-QAM from dB to percentage. Verify: EVM(dB) = $20\log_{10}(\text{EVM}\%)$. Does it match the given 11%? (2 points)

---

**Submission Instructions:**
- Submit a single PDF via Brightspace
- Constellation diagrams should be neat and clearly labeled
- Include all calculations with units
- Tables should be complete and readable

**Academic Integrity:**
- Individual work required
- Show all intermediate steps
- Cite any references to WiFi/LTE specifications
