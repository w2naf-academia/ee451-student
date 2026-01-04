# EE 451: Communications Systems
# Homework 5 - Probability, Noise, and SNR

**Topics:** Probability theory, Gaussian distribution, thermal noise, SNR calculations
**Textbook Reference:** Haykin & Moher, Chapters 8, 9, 11.1-11.3

**Total Points:** 100

---

## Instructions

- Show all work for full credit
- Include units in all final answers
- For probability problems, clearly state assumptions
- Q-function table and standard normal table will be provided on exam

---

## Problem 1: Basic Probability (10 points)

A binary communication system transmits bits "0" and "1" with probabilities:
- P(0) = 0.6
- P(1) = 0.4

**(a)** What is the probability of receiving "1" followed by "0" if bits are independent? (3 points)

**(b)** What is the probability of receiving at least one "1" in three consecutive bits? (4 points)

**(c)** If 1000 bits are transmitted, approximately how many "1" bits are sent? (3 points)

---

## Problem 2: Conditional Probability and Bayes' Theorem (12 points)

A receiver detects bits with the following error probabilities:
- P(detect 1 | sent 0) = 0.01 (false alarm)
- P(detect 0 | sent 1) = 0.02 (miss)
- P(sent 0) = 0.7
- P(sent 1) = 0.3

**(a)** What is P(detect 0 | sent 0)? (2 points)

**(b)** What is the probability of detecting a "1"? (4 points)

**(c)** Given that a "1" was detected, what is the probability that a "1" was actually sent? Use Bayes' theorem. (6 points)

---

## Problem 3: Gaussian Distribution (15 points)

A received signal has amplitude that is Gaussian distributed with mean $\mu$ = 5 V and standard deviation $\sigma$ = 2 V.

**(a)** Write the probability density function (PDF) for this signal. (3 points)

**(b)** What is the probability that the amplitude is between 3 V and 7 V? (4 points)

**(c)** What is the probability that the amplitude exceeds 9 V? Express in terms of the Q-function. (4 points)

**(d)** If the threshold for detection is set at 4 V, what fraction of signals will be below this threshold? (4 points)

**Given:** $Q(x) = \frac{1}{\sqrt{2\pi}} \int_x^{\infty} e^{-t^2/2} \, dt$

---

## Problem 4: Q-Function Calculations (12 points)

Use the Q-function for the following calculations:

**(a)** Calculate Q(1.5). You may use the approximation $Q(x) \approx \frac{1}{\sqrt{2\pi x}} \cdot e^{-x^2/2}$ for $x > 3$, or look up the value. (3 points)

**(b)** A bit error occurs if noise exceeds $3\sigma$. What is the probability of this event? (3 points)

**(c)** The complementary error function is $\text{erfc}(x) = 2 \cdot Q(x\sqrt{2})$. Express Q(x) in terms of erfc. (3 points)

**(d)** For BER = $10^{-6}$, what value of SNR (as a ratio, not dB) is required if $\text{BER} = Q(\sqrt{\text{SNR}})$? (3 points)

---

## Problem 5: Thermal Noise Power (15 points)

**(a)** Calculate the thermal noise power in a 1 MHz bandwidth at room temperature (T = 290 K). Use $k = 1.38 \times 10^{-23}$ J/K. (4 points)

**(b)** Express this noise power in dBm. (Recall: dBm = $10 \cdot \log_{10}(P/1 \text{ mW})$) (3 points)

**(c)** If the bandwidth increases to 20 MHz (WiFi channel), what is the new noise power in dBm? (3 points)

**(d)** A receiver has a noise figure NF = 6 dB. What is the total noise power in 20 MHz? (5 points)

---

## Problem 6: Signal-to-Noise Ratio (15 points)

A communication system has the following parameters:
- Received signal power: $P_s = -80$ dBm
- System bandwidth: B = 10 MHz
- Noise temperature: T = 290 K
- Noise figure: NF = 5 dB

**(a)** Calculate the noise power in dBm. (5 points)

**(b)** Calculate the SNR in dB. (3 points)

**(c)** Convert the SNR to a linear ratio. (2 points)

**(d)** If the signal power increases by 3 dB, what is the new SNR? (3 points)

**(e)** What signal power is required to achieve SNR = 20 dB? (2 points)

---

## Problem 7: Noise in AM Systems (12 points)

An AM receiver has the following specifications:
- Carrier power: $P_c = 10$ W
- Modulation index: $\mu$ = 0.8
- Noise power in the message bandwidth: $P_n = 0.1$ W

**(a)** Calculate the total transmitted power. (3 points)

**(b)** Calculate the signal power in the sidebands. (3 points)

**(c)** For DSB-SC (suppressed carrier), what is the output SNR? Assume the output SNR equals (sideband power)/(noise power). (3 points)

**(d)** For full carrier AM, the output SNR is reduced by the factor $\frac{\mu^2}{2 + \mu^2}$. Calculate the output SNR for this AM system. (3 points)

---

## Problem 8: FM Noise Performance (12 points)

An FM system has:
- Carrier power: $P_c = 20$ W
- Noise power: $P_n = 0.5$ W
- Modulation index: $\beta$ = 5
- Message bandwidth: $B_m = 15$ kHz

**(a)** Calculate the input SNR (carrier power to noise power ratio). (3 points)

**(b)** The output SNR for FM is given by: $(\text{SNR})_{\text{out}} = 3\beta^2(\beta + 1) \cdot (\text{SNR})_{\text{in}}$ for $\beta \gg 1$. Calculate the output SNR. (4 points)

**(c)** What is the FM improvement factor (output SNR / input SNR)? (3 points)

**(d)** Express the output SNR in dB. (2 points)

---

## Problem 9: Additive White Gaussian Noise (AWGN) (10 points)

**(a)** What does "white" mean in the context of white Gaussian noise? (3 points)

**(b)** What does "Gaussian" refer to? (2 points)

**(c)** The power spectral density of AWGN is $N_0/2$ W/Hz. If $N_0/2 = 10^{-9}$ W/Hz and the bandwidth is 5 MHz, what is the total noise power? (3 points)

**(d)** Why is AWGN a good model for thermal noise in communication systems? (2 points)

---

## Problem 10: Link Budget Basics (12 points - Challenge)

A WiFi system operates at 2.4 GHz with the following parameters:
- Transmit power: $P_t = 20$ dBm
- Transmit antenna gain: $G_t = 2$ dBi
- Receive antenna gain: $G_r = 2$ dBi
- Distance: d = 10 m
- System bandwidth: 20 MHz
- Noise figure: NF = 7 dB
- Temperature: T = 290 K

**(a)** Calculate the free-space path loss at 2.4 GHz and 10 m using: FSPL(dB) = $20 \cdot \log_{10}(d) + 20 \cdot \log_{10}(f) + 32.45$, where d is in km and f is in MHz. (4 points)

**(b)** Calculate the received signal power $P_r$ in dBm. (3 points)

**(c)** Calculate the noise power in dBm. (3 points)

**(d)** Calculate the SNR in dB. (2 points)

---

## Bonus Problem 1: Shannon's Theorem (5 points extra credit)

Shannon's theorem states that the channel capacity is:
$C = B \cdot \log_2(1 + \text{SNR})$

where C is in bits/s, B is bandwidth in Hz, and SNR is a linear ratio.

**(a)** Calculate the channel capacity for a system with B = 20 MHz and SNR = 30 dB. (3 points)

**(b)** If you want to transmit at 100 Mbps with B = 20 MHz, what minimum SNR (in dB) is required? (2 points)

---

## Bonus Problem 2: Noise Temperature (5 points extra credit)

**(a)** A receiver has a noise figure NF = 3 dB. Calculate the equivalent noise temperature $T_e$. Use the relationship: $\text{NF} = 1 + \frac{T_e}{T_0}$ where $T_0 = 290$ K. (3 points)

**(b)** If two amplifiers are cascaded with noise figures $\text{NF}_1$ = 3 dB and $\text{NF}_2$ = 6 dB, and gains $G_1$ = 20 dB and $G_2$ = 10 dB, calculate the overall noise figure using Friis formula:
$F_{\text{total}} = F_1 + \frac{F_2 - 1}{G_1}$
where F is the noise factor (linear, not dB). (2 points)

---

**Submission Instructions:**
- Submit a single PDF via Brightspace
- Show all conversions between dB and linear units
- For probability problems, show the complete calculation
- Q-function values can be looked up or approximated

**Academic Integrity:**
- Individual work required
- Show all work for full credit
- Cite any formula references

**Useful Constants:**
- Boltzmann constant: $k = 1.38 \times 10^{-23}$ J/K
- Room temperature: $T_0 = 290$ K
- Speed of light: $c = 3 \times 10^8$ m/s
