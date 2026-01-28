# EE 451: Communications Systems
# Midterm Exam 1 - Study Guide

**Exam Date:** Week 5 (Thursday, February 26, 2026)
**Duration:** 90 minutes
**Coverage:** Chapters 2-3, 7.1-7.2 (Fourier Analysis & Amplitude Modulation)
**Format:** Closed book, one 8.5" × 11" formula sheet (both sides) allowed

---

## Overview

Midterm 1 focuses on foundational concepts in signal analysis and amplitude modulation. You should be comfortable with:
- Fourier transform analysis and properties
- Time-frequency duality and bandwidth concepts
- AM modulation and demodulation
- Power calculations in communication systems
- Binary ASK as digital extension of AM

---

## Topic 1: Fourier Transform Fundamentals

### Key Concepts

**1. Rectangular Pulse and Sinc Function**
- Rectangular pulse in time → Sinc function in frequency
- Time-frequency duality: Narrow pulse → Wide spectrum
- First zero crossing determines bandwidth

**2. Bandwidth Definition**
- Null-to-null bandwidth: Distance between first zeros
- 3-dB bandwidth: Half-power points
- Relationship: $B_{3dB} \approx 0.88 \times B_{null}$

**3. Signal Energy**
- Time domain: $E = \int_{-\infty}^{\infty} |x(t)|^2 \, dt$
- Use Parseval's theorem to verify in frequency domain

### Essential Formulas

```
Fourier Transform Pair:
  rect(t/T) ↔ T·sinc(fT)

Sinc Function:
  sinc(x) = sin(πx)/(πx)
  First zero at x = ±1

Rectangular Pulse:
  x(t) = A·rect(t/T)
  X(f) = AT·sinc(fT)
  First zero at f = ±1/T

Energy:
  E = ∫|x(t)|² dt = A²T (for rectangular pulse)
```

### Practice Problems

From **Homework 1:**
- Problem 1: Rectangular pulse Fourier transform
- Problem 2: Sinc function properties
- Problem 3: Energy calculations

**Strategy:**
- Draw time and frequency domain sketches
- Identify key parameters: amplitude, duration, bandwidth
- Check units (time ↔ frequency reciprocity)

---

## Topic 2: Fourier Transform Properties

### Key Concepts

**1. Time-Shift Property**
- Delay in time → Phase shift in frequency
- Magnitude spectrum unchanged
- $x(t - t_0) \leftrightarrow X(f)e^{-j2\pi f t_0}$

**2. Modulation Property (Critical for AM!)**
- Multiplication by cosine → Frequency translation
- $x(t)\cos(2\pi f_c t) \leftrightarrow \frac{1}{2}[X(f-f_c) + X(f+f_c)]$
- Creates upper and lower sidebands

**3. Bandwidth in Modulated Signals**
- DSB-SC bandwidth = $2B$ (where B is message bandwidth)
- Spectrum centered at ±$f_c$

### Essential Formulas

```
Time-Shift:
  x(t - t₀) ↔ X(f)e^(-j2πft₀)

Modulation (DSB-SC):
  x(t)cos(2πfₑt) ↔ ½[X(f - fₑ) + X(f + fₑ)]

Bandwidth:
  Message bandwidth: B
  DSB-SC bandwidth: 2B
  AM bandwidth: 2B
  SSB bandwidth: B
```

### Practice Problems

From **Homework 1:**
- Problem 4: Modulation property
- Problem 5: DSB-SC spectrum sketching

**Strategy:**
- Always sketch BOTH time and frequency domains
- Label carrier frequency $f_c$ and sidebands clearly
- Remember: modulation creates TWO copies (at ±$f_c$)

---

## Topic 3: Parseval's Theorem

### Key Concepts

**1. Energy Conservation**
- Energy in time = Energy in frequency
- Useful for verifying calculations
- Different domains, same physical quantity

**2. Application**
- Calculate energy in whichever domain is easier
- Time domain for simple pulses
- Frequency domain for sinc functions

### Essential Formulas

```
Parseval's Theorem:
  ∫|x(t)|² dt = ∫|X(f)|² df

For exponential decay x(t) = Ae^(-at)u(t):
  E = A²/(2a)
```

### Practice Problems

From **Homework 1:**
- Problem 6: Verify energy using both domains

**Strategy:**
- Calculate in time domain first (usually easier)
- Use Parseval to verify in frequency domain
- Check units: energy has units of V²·s or J

---

## Topic 4: Amplitude Modulation (AM)

### Key Concepts

**1. AM Signal Structure**
- $s(t) = A_c[1 + \mu m_n(t)]\cos(2\pi f_c t)$
- Carrier amplitude: $A_c$
- Modulation index: $\mu = A_m/A_c$
- Normalized message: $|m_n(t)| \leq 1$

**2. Modulation Index**
- $\mu < 1$: Normal modulation
- $\mu = 1$: 100% modulation
- $\mu > 1$: Overmodulation (envelope distortion!)

**3. Power Distribution**
- Carrier power: Constant, carries NO information
- Sideband power: Varies with $\mu$, contains information
- Efficiency: Low for small $\mu$

### Essential Formulas

```
AM Signal:
  s(t) = Aₑ[1 + μ·cos(2πfₘt)]cos(2πfₑt)
  Aₑ = carrier amplitude
  μ = modulation index = Aₘ/Aₑ

Total Power:
  P_total = (Aₑ²/2R)(1 + μ²/2)

Carrier Power:
  P_carrier = Aₑ²/(2R)

Sideband Power:
  P_sideband = (Aₑ²/2R)(μ²/2)

Efficiency:
  η = P_sideband/P_total = μ²/(2 + μ²)

Bandwidth:
  B_AM = 2fₘ (same as DSB-SC)
```

### Common Mistakes to Avoid

❌ Using $A_c + A_m$ instead of $A_c(1 + \mu)$
❌ Forgetting factor of 1/2 in power formulas (RMS!)
❌ Confusing $\mu$ with $m(t)$
❌ Not checking for overmodulation ($\mu > 1$)

### Practice Problems

From **Homework 2:**
- Problem 1: Basic AM analysis
- Problem 2: Power calculations
- Problem 3: Modulation index and efficiency
- Problem 4: Overmodulation detection

**Strategy:**
1. Identify $A_c$, $A_m$, $f_c$, $f_m$ from equation
2. Calculate $\mu = A_m/A_c$
3. Check if $\mu \leq 1$ (overmodulated?)
4. Use power formulas (don't forget the R!)
5. Calculate efficiency as percentage

---

## Topic 5: DSB-SC vs. Full AM

### Key Concepts

**1. DSB-SC (Double Sideband Suppressed Carrier)**
- $s(t) = A_c m(t)\cos(2\pi f_c t)$
- No carrier component → more efficient
- Requires coherent detection (complex receiver)

**2. Comparison Table**

| Feature | DSB-SC | Full AM |
|---------|---------|---------|
| Carrier | Suppressed | Transmitted |
| Power efficiency | 100% in sidebands | $\mu^2/(2+\mu^2)$ |
| Detection | Coherent required | Envelope detector |
| Bandwidth | 2B | 2B |
| Complexity | High (receiver) | Low (receiver) |

**3. When to Use**
- DSB-SC: Power-limited systems, don't mind receiver complexity
- AM: Simple receivers (AM radio), power not critical

### Essential Formulas

```
DSB-SC Signal:
  s(t) = Aₑ·m(t)·cos(2πfₑt)

DSB-SC Power:
  P_DSB = (Aₑ²/2R)·P_m
  where P_m = mean square of m(t)

For sinusoidal m(t) = Aₘcos(2πfₘt):
  P_DSB = Aₑ²Aₘ²/(4R)

Comparison:
  P_DSB_sideband = P_AM_sideband (same sidebands)
  But P_AM_total = P_AM_sideband + P_carrier
```

### Practice Problems

From **Homework 2:**
- Problem 5: DSB-SC power calculation
- Problem 6: Efficiency comparison

**Strategy:**
- For DSB-SC: All power is in sidebands
- For AM: Must calculate carrier + sideband power
- Compare efficiencies as percentages

---

## Topic 6: Single Sideband (SSB)

### Key Concepts

**1. Motivation**
- DSB-SC wastes bandwidth (redundant sidebands)
- SSB transmits only one sideband
- Half the bandwidth of DSB-SC or AM!

**2. Bandwidth Efficiency**
- Message bandwidth: B
- AM/DSB-SC bandwidth: 2B
- SSB bandwidth: B (50% savings!)

**3. Generation Methods**
- **Filter method:** Generate DSB-SC, then filter
- **Phasing method:** Use Hilbert transform (90° phase shift)

**4. Applications**
- Amateur radio (voice communications)
- Telephone systems (frequency division multiplexing)
- Anywhere bandwidth is precious

### Essential Formulas

```
Bandwidth Comparison:
  Message: B (e.g., 3 kHz for voice)
  DSB-SC: 2B = 6 kHz
  SSB: B = 3 kHz
  AM: 2B = 6 kHz

Power:
  P_SSB = ½ P_DSB (only one sideband)
```

### Practice Problems

From **Homework 2:**
- Problem 7: Bandwidth calculations
- Problem 8: SSB generation methods

**Strategy:**
- Identify message bandwidth B
- SSB always uses exactly B (one sideband)
- AM and DSB-SC use 2B (two sidebands)

---

## Topic 7: Binary ASK (Amplitude Shift Keying)

### Key Concepts

**1. ASK as Digital AM**
- Bit "0" → Low amplitude (often 0)
- Bit "1" → High amplitude
- On-Off Keying (OOK): Special case where "0" = 0V

**2. Bit Duration and Bandwidth**
- Bit rate: $R_b$ bits/s
- Bit duration: $T_b = 1/R_b$
- Null-to-null bandwidth: $B \approx 2R_b$

**3. Relationship to AM**
- ASK is AM with digital message signal
- Rectangular pulses → sinc spectrum
- Bandwidth determined by bit rate, not carrier frequency

### Essential Formulas

```
ASK Parameters:
  Bit rate: Rᵦ (bits/s)
  Bit duration: Tᵦ = 1/Rᵦ
  Null-to-null BW: B ≈ 2/Tᵦ = 2Rᵦ

On-Off Keying (OOK):
  s₀(t) = 0              (bit "0")
  s₁(t) = A·cos(2πfₑt)   (bit "1")

Carson's Rule (estimate):
  B_ASK ≈ 2Rᵦ
```

### Practice Problems

From **Homework 2:**
- Problem 9: ASK bandwidth calculations
- Problem 10: Bit rate vs. bandwidth

**Strategy:**
1. Find bit duration $T_b = 1/R_b$
2. Null-to-null BW = $2/T_b = 2R_b$
3. Compare to carrier frequency ($B \ll f_c$ for RF)

---

## Formula Sheet Recommendations

### Must-Have Formulas

**Fourier Transform:**
```
rect(t/T) ↔ T·sinc(fT)
x(t - t₀) ↔ X(f)e^(-j2πft₀)
x(t)cos(2πfₑt) ↔ ½[X(f-fₑ) + X(f+fₑ)]
```

**AM:**
```
s(t) = Aₑ[1 + μmₙ(t)]cos(2πfₑt)
μ = Aₘ/Aₑ
P_total = (Aₑ²/2R)(1 + μ²/2)
η = μ²/(2 + μ²)
```

**DSB-SC:**
```
s(t) = Aₑm(t)cos(2πfₑt)
P_DSB = (Aₑ²/2R)·P_m
```

**Bandwidth:**
```
B_AM = B_DSB = 2B
B_SSB = B
B_ASK ≈ 2Rᵦ
```

**Energy/Power:**
```
Parseval: ∫|x(t)|² dt = ∫|X(f)|² df
P_avg = V²_rms/R = V²_peak/(2R) for sinusoid
```

### Useful Constants

```
Room temperature: T = 290 K
Boltzmann constant: k = 1.38 × 10⁻²³ J/K (probably not needed for Midterm 1)
```

---

## Exam Strategy

### Time Management (90 minutes total)

- **5 min:** Read entire exam, mark easy problems
- **10 min:** Problem 1 (Fourier fundamentals - typically straightforward)
- **10 min:** Problem 2 (Fourier properties)
- **10 min:** Problem 3 (Parseval's theorem)
- **20 min:** Problem 4 (AM analysis - usually longest)
- **10 min:** Problem 5 (DSB-SC comparison)
- **12 min:** Problem 6 (SSB and bandwidth)
- **8 min:** Problem 7 (ASK bonus - if time permits)
- **5 min:** Review and check answers

### Problem-Solving Approach

**For Fourier Transform Problems:**
1. Identify signal type (rect, sinc, exponential)
2. Draw time domain
3. Apply transform pair or properties
4. Draw frequency domain with labels
5. Calculate bandwidth from first zero crossing

**For AM Power Problems:**
1. Write out given signal equation
2. Identify $A_c$, $A_m$, $f_c$, $f_m$
3. Calculate $\mu = A_m/A_c$
4. **Check for overmodulation** ($\mu > 1$?)
5. Calculate carrier power: $P_c = A_c^2/(2R)$
6. Calculate total power: $P_{tot} = P_c(1 + \mu^2/2)$
7. Calculate sideband power: $P_{sb} = P_c(\mu^2/2)$
8. Efficiency: $\eta = P_{sb}/P_{tot}$

**For Bandwidth Problems:**
1. Identify message bandwidth B or frequency $f_m$
2. Choose correct formula:
   - AM/DSB-SC: 2B
   - SSB: B
   - ASK: $2R_b$
3. Label spectrum sketch clearly

### Common Mistakes to Avoid

❌ **Forgetting the factor of 1/2** in power formulas (sinusoid RMS = peak/√2)
❌ **Mixing up time and frequency domains** (check units!)
❌ **Not checking for overmodulation** before calculating AM power
❌ **Confusing bandwidth with carrier frequency**
❌ **Using wrong sideband formula** for SSB (B, not 2B)
❌ **Forgetting to include resistance R** in power calculations
❌ **Not showing units** in final answers

### Tips for Success

✅ **Draw diagrams!** Time and frequency sketches help visualize
✅ **Write out formulas** before substituting numbers
✅ **Check dimensions** (frequency in Hz, power in W, etc.)
✅ **Show all work** - partial credit is generous
✅ **Box final answers** - makes grading easier
✅ **Use your formula sheet** - don't waste time memorizing
✅ **Sanity check** - Does $\mu > 1$? Is power positive? Is BW < $f_c$?

---

## Practice Resources

### Homework Problems (Strongly Recommended)

**Homework 1 (Fourier Analysis):**
- All problems 1-10
- Focus on: Problems 1, 4, 5, 6 (most exam-relevant)

**Homework 2 (AM):**
- All problems 1-10
- Focus on: Problems 1, 2, 3, 4, 8 (core AM concepts)

### Lecture Notebooks

- **Lecture 2:** Fourier Transform fundamentals
- **Lecture 3:** Fourier properties and bandwidth
- **Lecture 5:** AM modulation and demodulation

### Textbook Sections

- **Chapter 2.1:** Fourier Transform
- **Chapter 2.2-2.3:** Filtering and bandwidth
- **Chapter 3:** Amplitude Modulation
- **Chapter 7.1-7.2:** ASK (digital AM)

---

## Self-Assessment Checklist

Before the exam, make sure you can:

**Fourier Transform:**
- [ ] Calculate Fourier transform of rectangular pulse
- [ ] Identify first zero crossing and bandwidth
- [ ] Apply time-shift property
- [ ] Apply modulation property (create sidebands)
- [ ] Sketch magnitude spectrum with labeled axes
- [ ] Calculate signal energy in time domain
- [ ] Verify energy using Parseval's theorem

**Amplitude Modulation:**
- [ ] Identify $A_c$, $A_m$, $f_c$, $f_m$ from AM equation
- [ ] Calculate modulation index $\mu$
- [ ] Detect overmodulation ($\mu > 1$)
- [ ] Calculate carrier power
- [ ] Calculate total transmitted power
- [ ] Calculate sideband power
- [ ] Calculate power efficiency
- [ ] Determine bandwidth (always 2B for AM)

**DSB-SC:**
- [ ] Write DSB-SC signal equation
- [ ] Calculate transmitted power
- [ ] Compare efficiency to full AM
- [ ] Explain advantage (power) vs. disadvantage (receiver complexity)

**SSB:**
- [ ] Calculate bandwidth (always B, not 2B!)
- [ ] Explain bandwidth advantage
- [ ] Describe filter method or phasing method
- [ ] List applications (amateur radio, telephony)

**ASK:**
- [ ] Relate bit rate to bandwidth
- [ ] Calculate null-to-null bandwidth ($2R_b$)
- [ ] Explain relationship to AM

---

## Final Thoughts

**This exam tests fundamentals!** If you understand:
1. Fourier transforms create sidebands when you multiply by a carrier
2. AM puts information in sidebands while wasting power in carrier
3. Bandwidth = 2 × (message bandwidth) for AM/DSB-SC
4. Power = $V^2/(2R)$ for sinusoids

...you'll do well!

**Focus your study time on:**
- Homework 1 & 2 problems (they mirror exam problems)
- Drawing accurate spectrum diagrams
- AM power calculations (most common exam mistakes here)
- Checking for overmodulation

**Good luck! 📡**
