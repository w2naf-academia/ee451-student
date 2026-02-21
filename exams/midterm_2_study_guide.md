# EE 451: Communications Systems
# Midterm Exam 2 — Study Guide

**Exam Date:** Tuesday, April 21, 2026 (L21)
**Duration:** 75 minutes
**Coverage:** Chapters 4-7, 9, 11 (Angle Modulation, Digital Modulation, Noise & Link Budgets)

---

## Exam Format

This exam has two parts, both completed during the 75-minute class period:

### Part A — Multiple Choice (20 points, ~15 minutes)

- **20 questions** at 1 point each on **Brightspace**
- Covers conceptual knowledge from the L11, L13, and L17 reading quizzes, plus topics from L15-L16 and L18-L20
- Questions are drawn randomly from the same pool as the **Practice Quiz** (see below)
- You may complete Part A and Part B in any order

### Part B — Open-Ended Problems (80 points, ~55 minutes)

- **5 problems** at 16 points each on **paper**
- **Closed book, closed notes** — a formula sheet is provided
- You may annotate the formula sheet with your own notes (no worked problems)
- Show all work for full credit
- Problems parallel Homework 3 and Homework 4
- You may use a scientific calculator

---

## Practice Quiz (Available on Brightspace)

A **Practice Quiz** is available on Brightspace containing questions from the exam MC pool.

- **Unlimited attempts** — take it as many times as you want
- **Your highest score counts as a homework grade**
- Questions cover FM/PM, FSK, BPSK, baseband digital, noise concepts, and more
- The best way to prepare for Part A is to take the practice quiz until you can consistently score well

---

## What to Study

### For Part A (Multiple Choice)

The MC questions test conceptual understanding and quick recall. Focus on:

**From L11 Reading (Ch 4.1-4.5):**
- FM vs. PM distinction
- Frequency deviation and modulation index $\beta$
- NBFM vs. WBFM classification
- Carson's rule for FM bandwidth
- Bessel functions and FM spectrum

**From L13 Reading (Ch 4.6-4.8, 7.3-7.4):**
- FM generation methods (direct, indirect)
- FM demodulation (discriminator, PLL)
- Binary FSK fundamentals (modulation index $h$, orthogonality)
- BPSK signal expressions and coherent detection

**From L17 Reading (Ch 5-6):**
- Intersymbol interference (ISI) and its causes
- Eye diagram interpretation
- Nyquist criterion for zero ISI
- Raised cosine filter and roll-off factor $\alpha$

**Additional MC topics from L15-L16, L18-L20:**
- Thermal noise ($P_n = kTB$), AWGN, SNR concepts
- Noise figure, Friis cascaded noise figure
- Link budget concepts (EIRP, path loss, link margin)
- OFDM basics (subcarriers, cyclic prefix, advantages)
- Spread spectrum (DSSS, FHSS, processing gain)
- CDMA and Walsh codes
- M-ary modulation (QPSK, QAM), spectral efficiency, EVM

**Preparation strategy:** Take the practice quiz on Brightspace repeatedly. Review any questions you get wrong.

### For Part B (Open-Ended Problems)

The open-ended problems test your ability to set up and solve calculations. Problems are similar in style to your homework assignments. You should be comfortable with the following topics:

**FM and PM Analysis**
- FM frequency deviation $\Delta f = k_f \cdot \max|m(t)|$ and modulation index $\beta = \Delta f / f_m$
- Carson's rule: $B_{\text{FM}} = 2(\Delta f + f_m)$
- PM phase deviation $\Delta\phi = k_p \cdot \max|m(t)|$
- PM frequency deviation: $\Delta f_{\text{PM}} = k_p \cdot A_m \cdot f_m$ (sinusoidal message)
- FM vs. PM: frequency deviation dependence on message frequency

**FSK and MSK**
- FSK modulation index $h = \Delta f \cdot T_b$
- MSK: $h = 0.5$, minimum frequency separation for orthogonality
- FSK bandwidth estimation
- Coherent vs. non-coherent FSK detection
- Advantages of continuous-phase FSK (MSK)

**BPSK, QPSK, and M-ary Modulation**
- BPSK and QPSK signal expressions
- Constellation diagrams and Gray coding
- Symbol rate $R_s = R_b / \log_2(M)$
- Null-to-null bandwidth for PSK
- Spectral efficiency $\eta = R_b / B$ (bits/s/Hz)
- Trade-off between spectral efficiency and power efficiency

**Noise and Cascaded Receivers**
- Thermal noise power: $P_n = kTB$
- dB/linear conversions for gain and noise figure
- Friis cascaded noise figure formula
- Equivalent noise temperature $T_e = (F - 1) \cdot T_0$
- System noise temperature $T_{\text{sys}} = T_{\text{ant}} + T_e$
- SNR calculation from signal power and noise power

**Link Budgets**
- EIRP = $P_t + G_t$ (dB)
- Free-space path loss: $L_p = 20\log_{10}(d) + 20\log_{10}(f) + 32.45$
- Received power: $P_r = \text{EIRP} - L_p + G_r$
- Noise power: $N = -174 + 10\log_{10}(B)$ (dBm)
- Link margin = SNR $-$ SNR$_{\text{req}}$

**Preparation strategy:** Redo Homework 3 and Homework 4 problems from scratch. If you can solve the homework without looking at solutions, you are well-prepared for Part B.

---

## Essential Formulas

A formula sheet is provided with the exam and distributed ahead of time via the student GitHub repo. It includes FM/PM, digital modulation, noise, and link budget formulas. You do not need to memorize these. However, you should know **how to use** each formula — practice applying them on homework problems.

**You may annotate the formula sheet** with your own notes, definitions, or reminders. However, **worked problems are not allowed** — formula sheets containing worked problems will be replaced with a clean copy at the start of the exam.

### Key formulas to be comfortable with

```
FM/PM:
  f_i(t) = f_c + k_f·m(t)                    [FM instantaneous frequency]
  Δf = k_f·max|m(t)|                          [FM frequency deviation]
  β = Δf / f_m                                [FM modulation index]
  B_FM = 2(Δf + f_m)                          [Carson's rule]
  Δf_PM = k_p · A_m · f_m                     [PM frequency deviation, sinusoidal]

Digital Modulation:
  T_b = 1/R_b                                 [bit duration]
  h = Δf · T_b                                [FSK modulation index]
  Δf_min = 1/(2T_b)                           [coherent FSK orthogonality]
  R_s = R_b / log₂(M)                         [symbol rate]
  B_null = 2R_b (BPSK), R_b (QPSK)            [null-to-null bandwidth]
  η = R_b / B                                 [spectral efficiency]

Noise:
  P_n = kTB                                   [thermal noise]
  F_total = F₁ + (F₂−1)/G₁ + (F₃−1)/(G₁G₂)  [Friis formula]
  T_e = (F − 1)·T₀                            [equivalent noise temp]
  T_sys = T_ant + T_e                          [system noise temp]

Link Budget:
  EIRP = P_t + G_t (dB)
  L_p = 20log(d) + 20log(f) + 32.45           [d in km, f in MHz]
  P_r = EIRP − L_p + G_r (dBm)
  N = −174 + 10log(B) (dBm)                   [B in Hz]
  Margin = SNR − SNR_req
```

---

## Time Management (75 minutes)

You may complete Part A and Part B in any order. Here are suggested time targets:

| Phase | Time | What to Do |
|-------|------|------------|
| Part A: Multiple Choice | ~15 min | Answer 20 MC questions on Brightspace |
| Problem 1: FM/PM | ~10 min | Deviation, modulation index, Carson's, FM vs PM |
| Problem 2: FSK/MSK | ~10 min | Bit duration, orthogonality, bandwidth, MSK advantages |
| Problem 3: BPSK/QPSK/QAM | ~10 min | Constellation, Gray coding, spectral efficiency |
| Problem 4: Noise | ~10 min | Friis formula, noise temperature, SNR |
| Problem 5: Link Budget | ~10 min | EIRP, path loss, received power, margin |
| Review | ~10 min | Check answers, verify units and dB conversions |
| **Total** | **75 min** | |

---

## Common Mistakes to Avoid

**FM/PM:**
- Confusing frequency deviation ($\Delta f$, in Hz) with modulation index ($\beta$, dimensionless)
- Forgetting to multiply Carson's rule by 2: $B_{\text{FM}} = 2(\Delta f + f_m)$
- In PM, forgetting that frequency deviation depends on $f_m$: $\Delta f_{\text{PM}} = k_p \cdot A_m \cdot f_m$

**FSK/MSK:**
- Confusing frequency separation $\Delta f = |f_1 - f_0|$ with the distance from center ($\Delta f/2$)
- Forgetting the orthogonality condition: $\Delta f_{\min} = 1/(2T_b)$, not $1/T_b$

**BPSK/QPSK/QAM:**
- BPSK null-to-null bandwidth is $2R_b$, but QPSK is $2R_s = R_b$ (half the bandwidth for the same bit rate)
- Forgetting that QPSK carries 2 bits/symbol, so $R_s = R_b / 2$
- Gray coding: adjacent symbols differ by **one** bit, not two

**Noise:**
- Mixing up linear and dB values in the Friis formula — the formula uses **linear** gains and noise figures
- Forgetting to convert noise figure from dB to linear before applying Friis
- Using $T_0 = 290$ K (the reference temperature), not $T_{\text{ant}}$, in the $T_e = (F-1) \cdot T_0$ formula

**Link Budget:**
- Path loss formula units: $d$ in **km**, $f$ in **MHz** — wrong units give wrong answers
- Forgetting that path loss is **subtracted** in dB: $P_r = \text{EIRP} - L_p + G_r$
- Doubling distance adds $20\log_{10}(2) = 6.02$ dB of path loss (not 3 dB)

---

## Self-Assessment Checklist

Before the exam, make sure you can:

**FM and PM:**
- [ ] Calculate $\Delta f$, $\beta$, and classify as NBFM or WBFM
- [ ] Apply Carson's rule and compare FM bandwidth to AM bandwidth
- [ ] Calculate PM phase and frequency deviation
- [ ] Explain the FM vs. PM difference in frequency deviation behavior

**FSK and MSK:**
- [ ] Calculate FSK modulation index $h$ and verify orthogonality
- [ ] Write FSK signal expressions for both bit values
- [ ] Estimate FSK/MSK bandwidth
- [ ] Explain MSK advantages (continuous phase, constant envelope)

**BPSK, QPSK, and QAM:**
- [ ] Write BPSK and QPSK signal expressions
- [ ] Draw constellation diagrams with Gray coding
- [ ] Calculate symbol rate for any M-ary scheme
- [ ] Compute and compare spectral efficiencies

**Noise and Cascaded Systems:**
- [ ] Convert between dB and linear for gain and noise figure
- [ ] Apply the Friis cascaded noise figure formula
- [ ] Calculate equivalent and system noise temperatures
- [ ] Calculate noise power and SNR in dB

**Link Budgets:**
- [ ] Calculate EIRP
- [ ] Calculate free-space path loss from distance and frequency
- [ ] Complete a full link budget (EIRP → path loss → received power → SNR → margin)
- [ ] Explain the effect of doubling distance on path loss

---

## Study Resources

### Homework (Most Important!)

- **Homework 3:** FM/PM analysis, Carson's rule, FSK modulation index, BPSK expressions
- **Homework 4:** M-ary PSK/QAM, spectral efficiency, EVM calculations, WiFi/cellular examples
- Redo these problems from scratch — don't just re-read solutions

### Practice Quiz

- Available on Brightspace — take it multiple times
- Covers all MC topics; highest score counts as homework

### Lecture Notebooks

- **L10:** Angle modulation introduction (FM/PM)
- **L11:** FM spectrum, Bessel functions, Carson's rule, FSK
- **L12:** FSK demodulation, PLL, discriminator
- **L13:** BPSK modulation, constellation diagrams
- **L15:** Noise fundamentals, AWGN, SNR, noise figure
- **L17:** ISI, eye diagrams, raised cosine filter
- **L19:** Spread spectrum, CDMA
- **L20:** M-ary modulation, QAM, EVM, FT8

### Textbook

- Chapter 4.1-4.5: FM/PM theory and modulation
- Chapter 4.6-4.8: FM generation and demodulation
- Chapter 5-6: Baseband digital transmission
- Chapter 7.3-7.4: FSK, BPSK
- Chapter 7.5-7.7: QPSK, QAM, spectral efficiency
- Chapter 9: Noise fundamentals
- Chapter 11.4-11.7: Link budgets

---

**Good luck!**
