# EE 451: Communications Systems
# Midterm Exam 2 - Study Guide

**Exam Date:** Week 12 (Tuesday, April 21, 2026)
**Duration:** 90 minutes
**Coverage:** Chapters 4-7 (FM, PM, FSK, PSK, M-ary Modulation, QAM)
**Format:** Closed book, one 8.5" × 11" formula sheet (both sides) allowed

---

## Overview

Midterm 2 focuses on angle modulation (FM/PM) and digital modulation schemes. You should be comfortable with:
- FM and PM fundamentals and relationships
- Carson's rule for FM bandwidth
- Binary digital modulation (FSK, BPSK)
- M-ary modulation (QPSK, QAM)
- Gray coding and constellation diagrams
- Spectral efficiency concepts

---

## Topic 1: Frequency Modulation (FM) Fundamentals

### Key Concepts

**1. FM Signal Characteristics**
- Frequency varies with message signal
- Amplitude remains constant (noise immunity!)
- Frequency deviation: $\Delta f = k_f \max|m(t)|$
- Modulation index: $\beta = \Delta f / f_m$

**2. Narrowband vs. Wideband FM**
- **NBFM:** $\beta \ll 1$ (typically $\beta < 0.3$)
- **WBFM:** $\beta \gg 1$ (broadcast FM: $\beta = 5$)
- Different bandwidth requirements!

**3. FM vs. AM**
- AM: Constant frequency, varying amplitude
- FM: Constant amplitude, varying frequency
- FM: Better noise performance (but more bandwidth)

### Essential Formulas

```
FM Signal:
  s(t) = Aₑcos[2πfₑt + 2πkf∫m(t)dt]

Instantaneous Frequency:
  fi(t) = fc + kf·m(t)
  where kf = frequency sensitivity (Hz/V)

Frequency Deviation:
  Δf = kf·max|m(t)|
  For m(t) = Am·cos(2πfmt):
    Δf = kf·Am

Modulation Index:
  β = Δf/fm

Carson's Rule (FM Bandwidth):
  BFM = 2(Δf + fm) = 2fm(1 + β)

NBFM Criterion:
  β << 1 (typically β < 0.3)
  BFM ≈ 2fm (like AM!)

WBFM:
  β >> 1
  BFM ≈ 2Δf (dominated by deviation)
```

### Common Mistakes to Avoid

❌ Confusing $\Delta f$ (deviation) with $f_m$ (message frequency)
❌ Forgetting that $\Delta f$ depends on $k_f$ AND message amplitude
❌ Using wrong Carson's rule form (two equivalent forms!)
❌ Mixing up NBFM and WBFM criteria

### Practice Problems

From **Homework 3:**
- Problem 1: FM fundamentals
- Problem 2: Carson's rule application
- Problem 3: NBFM vs. WBFM classification

**Strategy:**
1. Identify $k_f$, $A_m$, $f_m$ from problem
2. Calculate $\Delta f = k_f \times A_m$
3. Calculate $\beta = \Delta f / f_m$
4. Check if NBFM ($\beta < 0.3$) or WBFM ($\beta > 1$)
5. Apply Carson's rule: $B = 2(\Delta f + f_m)$

---

## Topic 2: Phase Modulation (PM)

### Key Concepts

**1. PM Signal Characteristics**
- Phase varies directly with message
- $\theta_i(t) = 2\pi f_c t + k_p m(t)$
- Phase sensitivity: $k_p$ (rad/V)

**2. FM vs. PM Relationship**
- **Key insight:** PM = FM with derivative
- FM can be generated from PM by integrating message
- PM can be generated from FM by differentiating message

**3. Frequency Deviation in PM**
- PM has frequency deviation that **increases with $f_m$**!
- FM has frequency deviation **independent of $f_m$**
- This is the KEY difference!

### Essential Formulas

```
PM Signal:
  s(t) = Aₑcos[2πfₑt + kp·m(t)]
  where kp = phase sensitivity (rad/V)

Instantaneous Phase:
  θi(t) = 2πfₑt + kp·m(t)

Phase Deviation:
  Δφ = kp·max|m(t)|

Instantaneous Frequency:
  fi(t) = (1/2π)·dθi/dt = fc + (kp/2π)·dm/dt

For m(t) = Am·cos(2πfmt):
  Maximum Frequency Deviation:
    Δf_PM = kp·Am·fm
    (Note: proportional to fm!)

Comparison:
  FM: Δf = kf·Am (independent of fm)
  PM: Δf = kp·Am·fm (proportional to fm)
```

### Common Mistakes to Avoid

❌ Thinking PM and FM have the same $\Delta f$ behavior
❌ Forgetting to take derivative when finding $f_i(t)$ from PM
❌ Confusing $\Delta\phi$ (phase deviation) with $\Delta f$ (frequency deviation)

### Practice Problems

From **Homework 3:**
- Problem 4: PM analysis
- Problem 5: FM vs. PM relationship

**Strategy:**
1. For PM: Write $\theta_i(t) = 2\pi f_c t + k_p m(t)$
2. Find $\Delta\phi = k_p \times \max|m(t)|$
3. Find $f_i(t) = \frac{1}{2\pi}\frac{d\theta_i}{dt}$
4. For sinusoidal message: $\Delta f = k_p \times A_m \times f_m$

---

## Topic 3: Binary FSK (Frequency Shift Keying)

### Key Concepts

**1. FSK Basics**
- Bit "0" → Frequency $f_0$
- Bit "1" → Frequency $f_1$
- Frequency separation: $\Delta f = |f_1 - f_0|$

**2. Modulation Index for FSK**
- $h = \Delta f \times T_b$
- Critical parameter for FSK design
- Determines orthogonality and spectral efficiency

**3. Orthogonality for Coherent Detection**
- Minimum separation: $\Delta f_{min} = \frac{1}{2T_b}$
- This gives $h = 0.5$ (MSK!)
- Larger separation OK, but wastes bandwidth

**4. Coherent vs. Non-Coherent Detection**
- **Coherent:** Requires phase lock, better performance
- **Non-coherent:** Simpler, no phase tracking needed
- FSK can use either (unlike PSK which requires coherent)

### Essential Formulas

```
FSK Signal Expressions:
  s₀(t) = A·cos(2πf₀t)    (bit "0")
  s₁(t) = A·cos(2πf₁t)    (bit "1")

Frequency Separation:
  Δf = |f₁ - f₀|

Bit Duration:
  Tb = 1/Rb  (where Rb = bit rate)

Modulation Index:
  h = Δf·Tb

Orthogonality Condition (Coherent FSK):
  Δf_min = 1/(2Tb) = Rb/2
  Gives h = 0.5 (Minimum Shift Keying!)

Bandwidth (Carson's Rule):
  B_FSK ≈ 2(Δf + Rb)
```

### Common Mistakes to Avoid

❌ Forgetting to calculate $T_b = 1/R_b$ first
❌ Confusing $\Delta f$ (separation) with $f_0$ or $f_1$ (individual frequencies)
❌ Using wrong orthogonality condition ($1/T_b$ instead of $1/(2T_b)$)

### Practice Problems

From **Homework 3:**
- Problem 6: Binary FSK fundamentals
- Problem 7: MSK analysis
- Problem 9: Coherent vs. non-coherent detection

**Strategy:**
1. Find $T_b = 1/R_b$
2. Calculate $\Delta f = |f_1 - f_0|$
3. Calculate $h = \Delta f \times T_b$
4. Check orthogonality: Is $\Delta f \geq 1/(2T_b)$?
5. If $h = 0.5$, it's MSK!

---

## Topic 4: Minimum Shift Keying (MSK)

### Key Concepts

**1. MSK Definition**
- Special case of CPFSK (Continuous Phase FSK)
- Modulation index $h = 0.5$ exactly
- **Minimum** frequency separation for orthogonal FSK

**2. Advantages of MSK**
- Continuous phase → no discontinuities
- Better spectral efficiency than standard FSK
- Faster sidelobe decay (less interference)
- Constant envelope (power amplifier friendly)

**3. Applications**
- GSM cellular (GMSK variant)
- Satellite communications
- Anywhere spectral efficiency matters

### Essential Formulas

```
MSK Characteristics:
  h = 0.5 (defining property!)
  Δf = Rb/2 = 1/(2Tb)

For MSK with bit rate Rb:
  Δf = Rb/2

If center frequency is fc:
  f₀ = fc - Rb/4
  f₁ = fc + Rb/4

MSK Advantages:
  - Continuous phase
  - Minimum bandwidth for orthogonal FSK
  - Constant envelope
```

### Practice Problems

From **Homework 3:**
- Problem 7: Complete MSK analysis

**Strategy:**
1. If $h = 0.5$, it's MSK
2. From $h = 0.5$ and bit rate, find $\Delta f = 0.5R_b$
3. Frequencies: $f_0 = f_c - \Delta f/2$, $f_1 = f_c + \Delta f/2$

---

## Topic 5: Binary Phase Shift Keying (BPSK)

### Key Concepts

**1. BPSK Basics**
- Bit "0" → Phase 0° (or +A)
- Bit "1" → Phase 180° (or -A)
- Information in PHASE, not amplitude
- Constant envelope (like FM/MSK)

**2. Constellation Diagram**
- Two points on I (real) axis
- 180° apart
- Maximum separation = best noise immunity

**3. Detection**
- **Must use coherent detection!**
- Envelope detector won't work (constant envelope)
- Requires carrier phase synchronization

**4. Bandwidth**
- Null-to-null: $B = 2R_b$
- Similar to ASK (same symbol rate)

### Essential Formulas

```
BPSK Signals:
  s₀(t) = A·cos(2πfₑt)         (bit "0", 0°)
  s₁(t) = -A·cos(2πfₑt)        (bit "1", 180°)
  Or: s₁(t) = A·cos(2πfₑt + π)

Constellation:
  Bit "0": I = +A, Q = 0
  Bit "1": I = -A, Q = 0
  Phase difference: 180°

Bandwidth:
  B_null-null = 2/Tb = 2Rb
  B_3dB ≈ Rb

Cannot use envelope detection!
  (Envelope is constant = A for both symbols)
```

### Common Mistakes to Avoid

❌ Saying BPSK can use envelope detection (NO!)
❌ Confusing BPSK bandwidth with carrier frequency
❌ Drawing constellation in wrong locations

### Practice Problems

From **Homework 3:**
- Problem 8: BPSK fundamentals

**Strategy:**
1. Write two signal expressions (180° apart)
2. Draw constellation: two points on I-axis
3. Calculate bandwidth: $B = 2R_b$
4. Explain why coherent detection is required

---

## Topic 6: QPSK (Quadrature Phase Shift Keying)

### Key Concepts

**1. QPSK Basics**
- 4 phase states (45°, 135°, 225°, 315°)
- Encodes **2 bits per symbol**
- Twice as efficient as BPSK!
- Symbol rate = Bit rate / 2

**2. I/Q Representation**
- QPSK uses both I (In-phase) and Q (Quadrature) channels
- Each symbol: combination of I and Q amplitudes
- 4 constellation points equally spaced

**3. BER Performance**
- QPSK has same BER as BPSK for same $E_b/N_0$
- But uses half the bandwidth!
- Best of both worlds for spectral efficiency

### Essential Formulas

```
QPSK Parameters:
  M = 4 symbols
  k = 2 bits/symbol
  Symbol rate: Rs = Rb/2

Four Signals (phases 45°, 135°, 225°, 315°):
  s₁(t) = A·cos(2πfₑt + π/4)
  s₂(t) = A·cos(2πfₑt + 3π/4)
  s₃(t) = A·cos(2πfₑt + 5π/4)
  s₄(t) = A·cos(2πfₑt + 7π/4)

Constellation Points:
  All at distance A from origin
  90° apart
  On circle of radius A

Bandwidth:
  B_QPSK = 2Rs = 2(Rb/2) = Rb
  Half the bandwidth of BPSK for same bit rate!

Spectral Efficiency:
  BPSK: 0.5 bits/s/Hz (in null-null BW)
  QPSK: 1.0 bits/s/Hz
```

### Common Mistakes to Avoid

❌ Forgetting symbol rate = bit rate / 2
❌ Drawing constellation points at wrong phases
❌ Not using Gray coding (see next topic!)
❌ Thinking QPSK has worse BER than BPSK

### Practice Problems

From **Homework 4:**
- Problem 1: QPSK fundamentals
- Problem 2: Gray coding for QPSK

**Strategy:**
1. Calculate symbol rate: $R_s = R_b / 2$
2. Write 4 signal expressions (45°, 135°, 225°, 315°)
3. Draw constellation with 4 points
4. Bandwidth: $B = 2R_s = R_b$

---

## Topic 7: Gray Coding

### Key Concepts

**1. Why Gray Coding?**
- Adjacent symbols differ by only **1 bit**
- Most errors go to adjacent symbols (AWGN)
- Symbol error → typically 1 bit error (not 2!)
- Reduces bit error rate (BER)

**2. Gray Code Properties**
- Used in ALL modern systems (WiFi, LTE, 5G)
- Essential for M-ary modulation
- Simple mapping rule: adjacent symbols differ by 1 bit

**3. Example for QPSK**
```
Natural Binary:  00, 01, 10, 11 (can differ by 2 bits!)
Gray Coded:      00, 01, 11, 10 (adjacent differ by 1 bit)
```

### QPSK Gray Coding Example

```
Constellation (typical Gray mapping):
     Q
     |
 01  |  00    (top half)
  ●──┼──●
     |         I
  ●──┼──●
 11  |  10    (bottom half)
     |
```

**Key:** Moving horizontally or vertically changes only 1 bit!

### Common Mistakes to Avoid

❌ Using natural binary instead of Gray code
❌ Assigning codes randomly without checking adjacency

### Practice Problems

From **Homework 4:**
- Problem 2: Gray coding for QPSK
- Problem 3: 8-PSK Gray coding

**Strategy:**
1. Draw constellation
2. Assign codes so adjacent symbols differ by 1 bit
3. Verify: moving one step (any direction) changes 1 bit

---

## Topic 8: M-ary Modulation and QAM

### Key Concepts

**1. M-ary PSK**
- M symbols, $k = \log_2(M)$ bits/symbol
- Better spectral efficiency as M increases
- But requires higher SNR for same BER

**2. QAM (Quadrature Amplitude Modulation)**
- Combines amplitude AND phase modulation
- Uses I and Q channels independently
- Rectangular constellation (e.g., 16-QAM: 4×4 grid)
- Even better spectral efficiency than M-PSK

**3. Spectral Efficiency**
- BPSK: 1 bit/symbol
- QPSK: 2 bits/symbol
- 16-QAM: 4 bits/symbol
- 64-QAM: 6 bits/symbol
- Higher M = more bits/symbol but needs more SNR

### Essential Formulas

```
M-ary Modulation:
  M = number of symbols
  k = log₂(M) = bits per symbol
  Rs = Rb/k = symbol rate

Examples:
  BPSK: M=2, k=1
  QPSK: M=4, k=2
  8-PSK: M=8, k=3
  16-QAM: M=16, k=4
  64-QAM: M=64, k=6

Spectral Efficiency:
  η = Rb/B = k·Rs/B bits/s/Hz
  Higher M → higher η

Trade-off:
  Higher M: Better spectral efficiency
  Higher M: Needs higher SNR (worse BER)
```

### 16-QAM Constellation

```
4×4 rectangular grid:
Amplitude levels: {±1, ±3} for I and Q

     Q
   3 ● ● ● ●
   1 ● ● ● ●
     ─────── I
  -1 ● ● ● ●
  -3 ● ● ● ●
   -3-1 1 3
```

### Common Mistakes to Avoid

❌ Confusing M (symbols) with k (bits/symbol)
❌ Forgetting symbol rate: $R_s = R_b/k$
❌ Not using Gray coding for QAM
❌ Thinking more bits/symbol is always better (ignores SNR!)

### Practice Problems

From **Homework 4:**
- Problem 3: M-ary PSK
- Problem 4: QAM constellation design
- Problem 5: Spectral efficiency comparison

**Strategy:**
1. Find k: $k = \log_2(M)$
2. Find symbol rate: $R_s = R_b / k$
3. For QAM: Draw rectangular constellation
4. Assign Gray codes to minimize bit errors

---

## Topic 9: EVM (Error Vector Magnitude)

### Key Concepts

**1. EVM Definition**
- Measures constellation quality
- EVM = error distance / reference distance
- Expressed as percentage

**2. Why EVM Matters**
- WiFi/LTE specs have strict EVM limits
- Higher-order modulation needs lower EVM
- Indicates transmitter/receiver impairments

**3. EVM Requirements**
- 256-QAM: EVM < 3% (very tight!)
- 64-QAM: EVM < 8%
- 16-QAM: EVM < 12%
- QPSK: EVM < 17%

### Essential Formulas

```
EVM Calculation:
  Error vector = Received - Ideal
  |Error| = √[(ΔI)² + (ΔQ)²]

EVM (%) = (|Error| / |Reference|) × 100%

Example:
  Ideal: (I, Q) = (1.0, 0.0)
  Received: (I, Q) = (0.92, 0.15)
  Error = √[(1-0.92)² + (0-0.15)²]
        = √[0.08² + 0.15²]
        = √[0.0064 + 0.0225]
        = √0.0289 ≈ 0.17
  EVM = (0.17/1.0) × 100% = 17%
```

### Practice Problems

From **Homework 4:**
- Problem 6: EVM calculation
- Bonus 2: EVM limits in standards

**Strategy:**
1. Plot ideal and received points
2. Calculate error vector
3. Find magnitude of error
4. Divide by reference (usually distance to ideal point)
5. Convert to percentage

---

## Formula Sheet Recommendations

### FM/PM Essentials

```
FM:
  fi(t) = fc + kf·m(t)
  Δf = kf·max|m(t)|
  β = Δf/fm
  BFM = 2(Δf + fm) = 2fm(1 + β)
  NBFM: β << 1
  WBFM: β >> 1

PM:
  θi(t) = 2πfct + kp·m(t)
  Δφ = kp·max|m(t)|
  fi(t) = fc + (kp/2π)·dm/dt
  For sinusoidal m(t):
    Δf_PM = kp·Am·fm
```

### Digital Modulation

```
FSK:
  h = Δf·Tb
  Orthogonal: Δf = 1/(2Tb)
  MSK: h = 0.5

BPSK:
  2 symbols, k=1 bit/symbol
  B = 2Rb
  Coherent detection required

QPSK:
  M=4, k=2 bits/symbol
  Rs = Rb/2
  B = Rb (half of BPSK!)

M-ary:
  k = log₂(M)
  Rs = Rb/k
```

### Spectral Efficiency

```
Bit rate: Rb
Symbol rate: Rs = Rb/k
Spectral efficiency: η = Rb/B bits/s/Hz

Examples:
  BPSK: η ≈ 0.5 bits/s/Hz
  QPSK: η ≈ 1.0 bits/s/Hz
  16-QAM: η ≈ 2.0 bits/s/Hz
  64-QAM: η ≈ 3.0 bits/s/Hz
```

---

## Exam Strategy

### Time Management (90 minutes)

- **5 min:** Read entire exam
- **15 min:** Problem 1 (FM fundamentals with Carson's rule)
- **12 min:** Problem 2 (PM analysis)
- **10 min:** Problem 3 (FM vs PM comparison)
- **15 min:** Problem 4 (FSK system design)
- **12 min:** Problem 5 (BPSK fundamentals)
- **15 min:** Problem 6 (QPSK and Gray coding)
- **6 min:** Problem 7 (MSK bonus if time)
- **5 min:** Review

### Problem-Solving Approach

**For FM Problems:**
1. Find $\Delta f = k_f \times A_m$
2. Find $\beta = \Delta f / f_m$
3. Classify: NBFM ($\beta < 0.3$) or WBFM ($\beta > 1$)?
4. Apply Carson's rule: $B = 2(\Delta f + f_m)$

**For PM Problems:**
1. Find $\Delta\phi = k_p \times A_m$
2. Find $f_i(t)$ by taking derivative
3. For sinusoidal: $\Delta f = k_p \times A_m \times f_m$
4. Compare to FM (key difference: $\Delta f$ depends on $f_m$ in PM!)

**For FSK Problems:**
1. Calculate $T_b = 1/R_b$
2. Calculate $\Delta f = |f_1 - f_0|$
3. Calculate $h = \Delta f \times T_b$
4. Check orthogonality: $\Delta f \geq 1/(2T_b)$?
5. If $h = 0.5$: MSK!

**For QPSK Problems:**
1. Symbol rate: $R_s = R_b / 2$
2. Write 4 signal expressions
3. Draw constellation (4 points equally spaced)
4. Apply Gray coding
5. Bandwidth: $B = 2R_s = R_b$

### Common Mistakes

❌ **FM:** Confusing $\Delta f$ with $f_m$, forgetting Carson's rule has TWO forms
❌ **PM:** Thinking $\Delta f$ is independent of $f_m$ (it's not!)
❌ **FSK:** Using $1/T_b$ for orthogonality instead of $1/(2T_b)$
❌ **BPSK:** Saying envelope detection works (it doesn't!)
❌ **QPSK:** Forgetting symbol rate = bit rate / 2
❌ **Gray coding:** Not checking that adjacent symbols differ by 1 bit

---

## Self-Assessment Checklist

Before the exam, can you:

**FM/PM:**
- [ ] Calculate frequency deviation $\Delta f$ for FM
- [ ] Calculate modulation index $\beta$
- [ ] Apply Carson's rule correctly
- [ ] Classify NBFM vs. WBFM
- [ ] Find instantaneous frequency for PM
- [ ] Explain why PM has $\Delta f$ proportional to $f_m$

**FSK:**
- [ ] Calculate bit duration from bit rate
- [ ] Find frequency separation $\Delta f$
- [ ] Calculate modulation index $h$
- [ ] Check orthogonality condition
- [ ] Identify MSK ($h = 0.5$)

**BPSK/QPSK:**
- [ ] Write signal expressions
- [ ] Draw constellation diagrams
- [ ] Calculate bandwidth
- [ ] Explain why BPSK needs coherent detection
- [ ] Find symbol rate for QPSK
- [ ] Apply Gray coding

**M-ary/QAM:**
- [ ] Calculate bits per symbol ($k = \log_2 M$)
- [ ] Find symbol rate from bit rate
- [ ] Draw QAM constellation
- [ ] Compare spectral efficiencies
- [ ] Calculate EVM

---

## Practice Resources

**Homework 3 (FM/PM/FSK/BPSK):** All problems 1-10
**Homework 4 (M-ary/QAM/EVM):** All problems 1-10

**Focus especially on:**
- HW3: Problems 1, 2, 5, 6, 7, 8
- HW4: Problems 1, 2, 4, 6

**Good luck! 📡**
