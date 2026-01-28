# EE 451: Communications Systems
# Final Exam - Comprehensive Study Guide

**Exam Date:** Thursday, May 21, 2026 (12:45-2:45 PM)
**Duration:** 180 minutes (3 hours)
**Coverage:** All course material (Chapters 1-11) with emphasis on Chapters 8-11
**Format:** Closed book, one 8.5" × 11" formula sheet (both sides) allowed

---

## Overview

The final exam is **comprehensive** but with **emphasis on later material** (probability, noise, BER, link budgets). Structure:
- **Part I (30 pts):** Fundamentals review (Fourier, AM, FM/PM)
- **Part II (35 pts):** Digital modulation (BPSK, QPSK, FSK, QAM)
- **Part III (40 pts):** Probability and noise (Gaussian, SNR, BER)
- **Part IV (35 pts):** Link budgets and system performance
- **Part V (10 pts):** Advanced topics (OFDM, spread spectrum)
- **Bonus (10 pts):** Satellite link analysis

**Key insight:** 85 of 150 points (57%) come from material AFTER Midterm 2!

---

## Study Strategy

### Priority Levels

**🔴 HIGHEST PRIORITY** (Study first - 60% of exam)
- Link budget calculations (Problems 10, 11)
- Gaussian distribution and Q-function (Problem 7)
- Thermal noise and SNR calculations (Problem 8)
- BER analysis for BPSK (Problem 9)
- Shannon capacity (Problem 11)

**🟡 MEDIUM PRIORITY** (Important - 25% of exam)
- BPSK vs QPSK comparison (Problem 4)
- 16-QAM and Gray coding (Problem 5)
- FSK system design (Problem 6)
- Adaptive modulation (Problem 12)

**🟢 LOWER PRIORITY** (Review quickly - 15% of exam)
- Fourier transforms (Problem 1)
- AM power calculations (Problem 2)
- FM vs PM (Problem 3)
- OFDM and spread spectrum concepts (Problem 13)

---

## Part I: Fundamentals Review (30 points)

### Quick Review Topics

**Fourier Transforms (10 pts)**
- Sinc ↔ rect transform pair
- Time-frequency duality
- Modulation property (DSB-SC spectrum)

**AM (10 pts)**
- Modulation index $\mu = A_m/A_c$
- Power: $P_{total} = \frac{A_c^2}{2R}(1 + \mu^2/2)$
- Efficiency: $\eta = \frac{\mu^2/2}{1 + \mu^2/2}$

**FM/PM (10 pts)**
- FM: $\Delta f = k_f A_m$ (independent of $f_m$)
- PM: $\Delta f = k_p A_m f_m$ (proportional to $f_m$)
- Carson's rule: $B_{FM} = 2(\Delta f + f_m)$

**Study Tip:** These are REVIEW topics. Don't spend too much time here if you understand Midterms 1 & 2 material. Focus on new material!

---

## Part II: Digital Modulation (35 points)

### BPSK vs QPSK (12 pts - Problem 4)

**Key Comparisons:**

| Feature | BPSK | QPSK |
|---------|------|------|
| Bits/symbol | 1 | 2 |
| Symbol rate | $R_b$ | $R_b/2$ |
| Bandwidth | $2R_b$ | $R_b$ |
| Spectral efficiency | 0.5 bits/s/Hz | 1.0 bits/s/Hz |
| BER (same $E_b/N_0$) | Same! | Same! |

**Critical insight:** QPSK is twice as bandwidth efficient with no BER penalty!

### QAM and Gray Coding (12 pts - Problem 5)

**16-QAM Basics:**
- M = 16 symbols, k = 4 bits/symbol
- Rectangular constellation: 4×4 grid
- Amplitude levels: typically {±1, ±3}

**Gray Coding Rules:**
- Adjacent symbols differ by 1 bit
- Minimizes BER (most errors → adjacent symbols)
- Mandatory in modern systems!

**EVM (Error Vector Magnitude):**
- Measures constellation quality
- EVM% = (Error distance / Reference distance) × 100%
- WiFi/LTE have strict EVM limits (e.g., 256-QAM < 3%)

### FSK System Design (11 pts - Problem 6)

**Orthogonal FSK:**
- Minimum separation: $\Delta f_{min} = \frac{1}{2T_b}$
- Modulation index: $h = \Delta f \times T_b$
- MSK: $h = 0.5$ exactly

**Quick formulas:**
```
Tb = 1/Rb
Δf = |f₁ - f₀|
h = Δf·Tb
Orthogonal: Δf ≥ 1/(2Tb)
MSK: h = 0.5
```

---

## Part III: Probability and Noise (40 points) 🔴

**THIS IS THE MOST IMPORTANT SECTION!**

### Gaussian Distribution (15 pts - Problem 7)

**PDF of Gaussian:**
$$f_X(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-(x-\mu)^2/(2\sigma^2)}$$

**Standardization:**
$$Z = \frac{X - \mu}{\sigma} \sim N(0, 1)$$

**Q-Function:**
$$Q(x) = P(Z > x) \text{ for } Z \sim N(0,1)$$

**For general Gaussian X ~ N(μ, σ²):**
$$P(X > a) = Q\left(\frac{a - \mu}{\sigma}\right)$$

**Key Q-function values (memorize these!):**
```
Q(1.0) ≈ 0.159    Q(2.0) ≈ 0.023
Q(1.5) ≈ 0.067    Q(3.0) ≈ 0.0013
Q(4.0) ≈ 3e-5     Q(4.75) ≈ 1e-6
```

**Property:** $Q(-x) = 1 - Q(x)$

**Practice:**
1. Identify μ and σ from problem
2. Standardize: $z = (x - \mu)/\sigma$
3. Express using Q-function
4. Look up or calculate

### Thermal Noise and SNR (12 pts - Problem 8)

**Thermal Noise Power:**
$$P_n = kTB$$
where:
- $k = 1.38 \times 10^{-23}$ J/K (Boltzmann constant)
- $T$ = temperature (K)
- $B$ = bandwidth (Hz)

**Noise Figure:**
$$P_{n,total} = P_n \times F = P_n \times 10^{NF_{dB}/10}$$

**In dBm:**
$$P_n(dBm) = 10\log_{10}\left(\frac{kTB}{10^{-3}}\right)$$

**Quick calculation:**
At T = 290 K:
$$P_n(dBm) \approx -174 + 10\log_{10}(B_{Hz})$$

**SNR:**
$$SNR(dB) = P_s(dBm) - P_n(dBm)$$

**Critical conversions:**
```
dBm to W: P_W = 10^((P_dBm - 30)/10)
W to dBm: P_dBm = 10·log₁₀(P_W) + 30
dB addition: Ptotal(dB) = P1(dB) + P2(dB)
Linear addition: Ptotal_W = P1_W + P2_W
```

**Common values to know:**
```
0 dBm = 1 mW
-30 dBm = 1 μW
-60 dBm = 1 nW
-90 dBm = 1 pW

+3 dB = ×2
+10 dB = ×10
+20 dB = ×100
```

### BER Performance (13 pts - Problem 9)

**BPSK BER:**
$$BER_{BPSK} = Q(\sqrt{2E_b/N_0})$$

**Conversions:**
$$\frac{E_b}{N_0}(dB) = 10\log_{10}(E_b/N_0)$$

**To find linear from dB:**
$$\frac{E_b}{N_0} = 10^{(E_b/N_0)_{dB}/10}$$

**Bit errors per second:**
$$N_{errors/s} = BER \times R_b$$

**Common $E_b/N_0$ values for BER targets:**
```
BER = 10⁻³: Eb/N0 ≈ 6.8 dB
BER = 10⁻⁴: Eb/N0 ≈ 8.4 dB
BER = 10⁻⁵: Eb/N0 ≈ 9.6 dB
BER = 10⁻⁶: Eb/N0 ≈ 10.5 dB
```

**Step-by-step for BER problems:**
1. Convert $E_b/N_0$ from dB to linear
2. Calculate $\sqrt{2E_b/N_0}$
3. Find $Q(\sqrt{2E_b/N_0})$ using table
4. This is your BER
5. Errors/sec = BER × bit rate

---

## Part IV: Link Budgets (35 points) 🔴🔴🔴

**CRITICAL SECTION - WORTH 35 POINTS!**

### Free-Space Path Loss (FSPL)

**Two equivalent forms:**

**Form 1 (dB, easier for calculations):**
$$FSPL(dB) = 20\log_{10}(d_{km}) + 20\log_{10}(f_{MHz}) + 32.45$$

**Form 2 (from wavelength):**
$$FSPL(dB) = 20\log_{10}\left(\frac{4\pi d}{\lambda}\right)$$
where $\lambda = c/f$

**Example calculation:**
```
f = 5.8 GHz = 5800 MHz
d = 50 m = 0.05 km

FSPL = 20·log₁₀(0.05) + 20·log₁₀(5800) + 32.45
     = 20·(-1.301) + 20·(3.763) + 32.45
     = -26.02 + 75.26 + 32.45
     = 81.69 dB
```

### Complete Link Budget (Problem 10 - 18 pts)

**Link Budget Equation:**
$$P_r(dBm) = P_t(dBm) + G_t(dBi) + G_r(dBi) - FSPL(dB) - L_{misc}(dB)$$

**Step-by-step procedure:**

**1. Calculate FSPL**
- Use formula above
- Make sure units match (km and MHz, OR meters and Hz)

**2. Calculate received power**
$$P_r = P_t + G_t + G_r - FSPL - L_{other}$$

**3. Calculate noise power**
$$P_n = kTB \text{ (in W)}$$
$$P_n(dBm) = 10\log_{10}(P_n/0.001)$$

OR use quick formula:
$$P_n(dBm) \approx -174 + 10\log_{10}(B_{Hz}) + NF(dB)$$

**4. Calculate SNR**
$$SNR(dB) = P_r(dBm) - P_n(dBm) - \text{fade margin}$$

**5. Determine supported modulation**
Compare SNR to thresholds:
```
QPSK:    8 dB
16-QAM:  15 dB
64-QAM:  22 dB
256-QAM: 28 dB
```

**Common mistakes:**
❌ Forgetting to convert distance to km or frequency to MHz
❌ Mixing up + and - signs in link budget
❌ Forgetting fade margin
❌ Not adding noise figure to thermal noise

### Shannon Capacity (Problem 11 - 10 pts)

**Shannon-Hartley Theorem:**
$$C = B \log_2(1 + SNR)$$ bits/s

where:
- $C$ = channel capacity (bits/s)
- $B$ = bandwidth (Hz)
- $SNR$ = linear ratio (NOT dB!)

**Convert SNR from dB:**
$$SNR = 10^{SNR(dB)/10}$$

**Spectral Efficiency:**
$$\eta = \frac{C}{B} = \log_2(1 + SNR)$$ bits/s/Hz

**Example:**
```
B = 10 MHz, SNR = 20 dB

SNR_linear = 10^(20/10) = 100

C = 10×10⁶ × log₂(1 + 100)
  = 10×10⁶ × log₂(101)
  = 10×10⁶ × 6.658
  = 66.58 Mbps

η = 6.658 bits/s/Hz
```

**Common mistake:**
❌ Using SNR in dB directly (must convert to linear!)

### Adaptive Modulation (Problem 12 - 7 pts)

**Concept:**
- Choose modulation based on SNR
- Higher SNR → higher-order modulation → more bits/s
- Lower SNR → lower-order modulation → more reliable

**SNR vs. distance model:**
$$SNR(dB) = SNR_0 - n \times 10\log_{10}(d/d_0)$$

where $n$ is path loss exponent (typical: 2-4)

**Procedure:**
1. Calculate SNR at each distance
2. Compare to modulation thresholds
3. Select highest modulation with SNR ≥ threshold

---

## Part V: Advanced Topics (10 points)

### OFDM (4 pts)

**Why OFDM?**
- Solves frequency-selective fading problem
- Divides wideband channel into many narrowband subchannels
- Each subchannel experiences flat fading
- Simpler equalization than single-carrier

**Applications:**
- WiFi (802.11a/g/n/ac/ax)
- LTE, 5G NR
- DVB-T (digital TV)

**Key concept:** Convert frequency-selective fading → flat fading per subcarrier

### Spread Spectrum (6 pts)

**DSSS (Direct Sequence Spread Spectrum):**
- Data rate: $R_b$
- Chip rate: $R_c$ (much higher)
- Processing gain: $G_p = \frac{R_c}{R_b}$ (ratio)
- In dB: $G_p(dB) = 10\log_{10}(R_c/R_b)$

**Advantages:**
- Jamming resistance (processing gain)
- Multiple access (CDMA)
- Low probability of intercept

**Example:**
```
Rb = 1 Mbps, Rc = 10 Mchips/s
Gp = 10 Mchips/s / 1 Mbps = 10
Gp(dB) = 10·log₁₀(10) = 10 dB
```

---

## Bonus: Satellite Link (10 points)

**Typical satellite parameters:**
- High transmit power: 40 dBW (10 kW)
- High antenna gains: 30-40 dBi
- Long distance: 36,000 km (GEO)
- Very high FSPL: ~200 dB!
- Low noise temperature: 150 K (LNA)

**$E_b/N_0$ and SNR relationship:**
$$\frac{E_b}{N_0} = SNR \times \frac{B}{R_b}$$

**Use this to find maximum bit rate:**
$$R_b = \frac{SNR \times B}{E_b/N_0}$$

---

## Master Formula Sheet

### Probability & Noise

```
Gaussian PDF:
  f(x) = (1/(σ√(2π))) exp(-(x-μ)²/(2σ²))

Q-function:
  P(X > a) = Q((a-μ)/σ) for X ~ N(μ, σ²)
  Q(-x) = 1 - Q(x)

Thermal Noise:
  Pn = kTB  (k = 1.38×10⁻²³ J/K)
  Pn(dBm) ≈ -174 + 10log₁₀(B_Hz) + NF(dB)  [at T=290K]

SNR:
  SNR(dB) = Ps(dBm) - Pn(dBm)

BER:
  BER_BPSK = Q(√(2Eb/N0))
```

### Link Budget

```
FSPL:
  FSPL(dB) = 20log₁₀(d_km) + 20log₁₀(f_MHz) + 32.45

Link Budget:
  Pr(dBm) = Pt(dBm) + Gt + Gr - FSPL - Losses

Shannon Capacity:
  C = B·log₂(1 + SNR)  [SNR must be linear!]

Eb/N0 vs SNR:
  Eb/N0 = SNR × (B/Rb)
```

### Digital Modulation (Review)

```
BPSK: k=1, Rs=Rb, B=2Rb
QPSK: k=2, Rs=Rb/2, B=Rb
M-ary: k=log₂(M), Rs=Rb/k

FSK: h = Δf·Tb
     Orthogonal: Δf = 1/(2Tb)
     MSK: h = 0.5
```

### Analog Modulation (Review)

```
AM:
  s(t) = Ac[1 + μ·mn(t)]cos(2πfct)
  Ptotal = (Ac²/2R)(1 + μ²/2)
  η = μ²/(2 + μ²)

FM:
  Δf = kf·max|m(t)|
  β = Δf/fm
  BFM = 2(Δf + fm)

PM:
  Δφ = kp·max|m(t)|
  Δf_PM = kp·Am·fm  (depends on fm!)
```

---

## Exam Strategy for 180 Minutes

### Time Allocation

**Part I (30 pts) - 25 minutes**
- Problem 1: 7 min (Fourier - straightforward)
- Problem 2: 10 min (AM power)
- Problem 3: 8 min (FM vs PM)

**Part II (35 pts) - 30 minutes**
- Problem 4: 10 min (BPSK vs QPSK)
- Problem 5: 12 min (16-QAM, Gray coding)
- Problem 6: 8 min (FSK design)

**Part III (40 pts) - 50 minutes** 🔴
- Problem 7: 18 min (Gaussian & Q-function - 5 parts!)
- Problem 8: 15 min (Thermal noise & SNR)
- Problem 9: 17 min (BER analysis)

**Part IV (35 pts) - 45 minutes** 🔴
- Problem 10: 25 min (WiFi link budget - longest problem!)
- Problem 11: 12 min (Shannon capacity)
- Problem 12: 8 min (Adaptive modulation)

**Part V (10 pts) - 10 minutes**
- Problem 13: 10 min (OFDM & spread spectrum concepts)

**Bonus (10 pts) - 10 minutes** (if time!)
- Satellite link analysis

**Review: 10 minutes**

### Priority Order (if running low on time)

1. **Do first:** Problems 7, 8, 9, 10 (new material, high points)
2. **Do second:** Problems 11, 12 (new material)
3. **Do third:** Problems 4, 5, 6 (review, but still good points)
4. **Do last:** Problems 1, 2, 3 (pure review)
5. **If time:** Problems 13 and Bonus

### Calculator Tips

**Pre-calculate common values:**
```
log₁₀(2) ≈ 0.301
log₁₀(10) = 1
ln(2) ≈ 0.693

10⁰·³ ≈ 2
10⁰·⁵ ≈ 3.16
10¹·⁰ = 10

For log₂(x): log₂(x) = log₁₀(x)/log₁₀(2) ≈ 3.32·log₁₀(x)
```

---

## Common Mistakes to AVOID

### Part III (Probability/Noise)

❌ Forgetting to standardize Gaussian: $z = (x-\mu)/\sigma$
❌ Using SNR in dB directly in Shannon formula (must convert to linear!)
❌ Forgetting to add noise figure to thermal noise
❌ Confusing Q(x) with 1-Q(x)
❌ Using wrong Boltzmann constant or temperature

### Part IV (Link Budgets)

❌ Wrong units in FSPL: using meters instead of km, or Hz instead of MHz
❌ Wrong signs in link budget (it's Pt + Gt + Gr - FSPL, not all positive!)
❌ Forgetting fade margin when calculating SNR
❌ Comparing to wrong modulation thresholds
❌ Not converting $E_b/N_0$ from dB when using formulas

### General

❌ Not showing units in answers
❌ Not checking if answer makes physical sense
❌ Spending too long on early problems (save time for Parts III & IV!)
❌ Forgetting to box/circle final answers

---

## Self-Assessment Checklist

**Can you:**

**Probability & Noise:**
- [ ] Write Gaussian PDF
- [ ] Standardize and use Q-function
- [ ] Calculate thermal noise power (kTB)
- [ ] Convert between dBm and Watts
- [ ] Add noise figure correctly
- [ ] Calculate SNR in dB
- [ ] Convert $E_b/N_0$ between dB and linear
- [ ] Calculate BER for BPSK
- [ ] Find bit errors per second

**Link Budgets:**
- [ ] Calculate FSPL with correct units
- [ ] Perform complete link budget (Pr = Pt + gains - losses)
- [ ] Calculate noise power in dBm
- [ ] Calculate SNR accounting for fade margin
- [ ] Select modulation based on SNR
- [ ] Calculate Shannon capacity (with SNR in linear!)
- [ ] Apply adaptive modulation rules

**Digital Modulation:**
- [ ] Compare BPSK vs QPSK (bandwidth, spectral efficiency)
- [ ] Draw 16-QAM constellation
- [ ] Apply Gray coding
- [ ] Calculate EVM
- [ ] Design orthogonal FSK system
- [ ] Identify MSK

**Review Topics:**
- [ ] Fourier transform of rect/sinc
- [ ] AM power and efficiency
- [ ] FM vs PM frequency deviation

---

## Final Study Plan (1 Week Before Exam)

### Days 7-6: New Material (Priority 🔴)

- **Study:** Homework 5 (all problems) - Probability, noise, SNR
- **Practice:** BER and link budget problems from lecture notebooks
- **Practice:** Midterm 1 solutions (Problems 7-9)
- **Focus:** Link budget procedure, Q-function, thermal noise

### Days 5-4: Integration

- **Practice:** Complete a full link budget from scratch
- **Practice:** Gaussian/Q-function problems
- **Practice:** BER calculations
- **Review:** Shannon capacity problems
- **Make:** Your formula sheet!

### Days 3-2: Review Material

- **Quick review:** Homework 3 & 4 (digital modulation)
- **Quick review:** Homework 1 & 2 (Fourier, AM)
- **Practice:** Midterm 2 (all problems quickly)
- **Refine:** Formula sheet

### Day 1: Final Prep

- **Take:** Practice final (under time pressure!)
- **Review:** Common mistakes list
- **Check:** Formula sheet is complete
- **Sleep:** Well!

---

## What to Bring

✅ Calculator (scientific, not graphing)
✅ Formula sheet (both sides, handwritten recommended)
✅ Pencils/pens
✅ Student ID

---

## During the Exam

1. **Read all problems first** (5 min)
2. **Mark easy problems** with a star
3. **Do high-value problems first** (Parts III & IV)
4. **Show ALL work** - partial credit is generous!
5. **Box final answers**
6. **Check units** on every answer
7. **Sanity check:** Does the answer make sense?
8. **If stuck:** Move on, come back later
9. **Last 10 min:** Review, check signs, check units

---

## Final Thoughts

**The exam rewards:**
- Systematic problem-solving (link budgets!)
- Careful unit management (km vs m, dB vs linear)
- Understanding relationships (Shannon, BER, SNR)

**Focus your final study on:**
1. Link budget procedure (practice 3-5 complete examples)
2. Q-function and BER calculations
3. SNR and noise calculations
4. Digital modulation comparisons

**You've got this! The comprehensive nature means you can show your understanding across the whole course. Focus on the new material (Parts III-IV) and you'll do great! 📡**

**Good luck on your final exam!**
