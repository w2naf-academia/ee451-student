# EE 451: Communications Systems
# Midterm Exam 1 — Study Guide

**Exam Date:** Thursday, February 26, 2026 (L9)
**Duration:** 75 minutes
**Coverage:** Chapters 2-3, 7.1-7.2 (Fourier Analysis & Amplitude Modulation)

---

## Exam Format

This exam has two parts, both completed during the 75-minute class period:

### Part A — Multiple Choice (20 points, ~15 minutes)

- **20 questions** at 1 point each on **Brightspace**
- Covers conceptual knowledge from the L02, L04, and L07 reading quizzes
- Questions are drawn randomly from the same pool as the **Practice Quiz** (see below)
- You may complete Part A and Part B in any order

### Part B — Open-Ended Problems (80 points, ~55 minutes)

- **5 problems** at 16 points each on **paper**
- **Closed book, closed notes** — a formula sheet is provided
- You may annotate the formula sheet with your own notes (no worked problems)
- Show all work for full credit
- Problems parallel Homework 1 and Homework 2
- You may use a scientific calculator

---

## Practice Quiz (Available Now on Brightspace)

A **Practice Quiz** is available on Brightspace containing all 102 questions from the exam MC pool. This is the same pool that Part A draws from.

- **Unlimited attempts** — take it as many times as you want
- **Your highest score counts as a homework grade**
- Questions cover Fourier transforms, AM, SSB/VSB, receivers, and ASK/OOK
- The best way to prepare for Part A is to take the practice quiz until you can consistently score well

---

## What to Study

### For Part A (Multiple Choice)

The MC questions test conceptual understanding and quick recall. Focus on:

**From L02 Reading (Ch 2.1-2.5):**
- Fourier transform definitions and properties
- Time-frequency duality
- Dirac delta function properties
- Energy vs. power signals
- Parseval's theorem

**From L04 Reading (Ch 3.1-3.3):**
- DSB-SC modulation: signal expression, spectrum, bandwidth
- Full carrier AM: modulation index, overmodulation
- Envelope detection requirements
- Power distribution in AM signals

**From L07 Reading (Ch 3.6-3.8, 7.1-7.2):**
- SSB motivation and bandwidth savings
- SSB generation methods (filter, phasing)
- VSB as a compromise between DSB and SSB
- Superheterodyne receiver architecture
- Image frequency and its mitigation
- ASK/OOK fundamentals

**Preparation strategy:** Take the practice quiz on Brightspace repeatedly. Review any questions you get wrong.

### For Part B (Open-Ended Problems)

The open-ended problems test your ability to set up and solve calculations. Problems are similar in style to your homework assignments. You should be comfortable with the following topics:

**Fourier Analysis & Signal Energy**
- Computing Fourier transforms (especially rect/sinc pairs)
- Bandwidth calculations (first null, null-to-null)
- Signal energy in the time domain
- Time-frequency duality

**Amplitude Modulation (Full AM)**
- Identifying AM signal parameters ($A_c$, $m(t)$, $f_c$, $\mu$)
- Overmodulation conditions
- Power calculations (carrier, sideband, total)
- Power efficiency

**DSB-SC and SSB**
- DSB-SC signal expressions and trig identity expansion
- Sideband frequencies and RF bandwidth
- Power calculations
- SSB bandwidth and frequency components

**On-Off Keying (OOK)**
- OOK signal parameters (bit duration, expression, bandwidth)
- Bandwidth comparison with analog AM
- Waveform sketching

**Superheterodyne Receivers**
- LO frequency and image frequency calculations
- Image rejection and mitigation strategies
- IF trade-offs (image rejection vs. channel selectivity)

**Preparation strategy:** Redo Homework 1 and Homework 2 problems from scratch. If you can solve the homework without looking at solutions, you are well-prepared for Part B.

---

## Essential Formulas

A formula sheet is provided with the exam and distributed ahead of time via the student GitHub repo. It includes Fourier transform pairs, properties, trig identities, and AM formulas. You do not need to memorize these. However, you should know **how to use** each formula — practice applying them on homework problems.

**You may annotate the formula sheet** with your own notes, definitions, or reminders. However, **worked problems are not allowed** — formula sheets containing worked problems will be replaced with a clean copy at the start of the exam.

### Key formulas to be comfortable with

```
Fourier Transform:
  rect(t/T) ↔ T·sinc(fT)
  sinc(x) = sin(πx)/(πx), first zero at x = ±1

Modulation Property:
  x(t)cos(2πfₑt) ↔ ½[X(f - fₑ) + X(f + fₑ)]

Parseval's Theorem:
  E = ∫|x(t)|² dt = ∫|X(f)|² df

AM Signal & Power:
  s(t) = Aₑ[1 + μ·mₙ(t)]cos(2πfₑt)
  P_total = (Aₑ²/2R)(1 + μ²⟨mₙ²⟩)  [general]
  P_total = (Aₑ²/2R)(1 + μ²/2)      [single tone, since ⟨cos²⟩ = ½]
  η = μ²⟨mₙ²⟩ / (1 + μ²⟨mₙ²⟩)

Bandwidth:
  DSB-SC / AM: 2B
  SSB: B
  ASK: 2Rb

Superheterodyne (high-side injection):
  f_LO = f_RF + f_IF
  f_image = f_RF + 2·f_IF
```

---

## Time Management (75 minutes)

You may complete Part A and Part B in any order. Here are suggested time targets:

| Phase | Time | What to Do |
|-------|------|------------|
| Part A: Multiple Choice | ~15 min | Answer 20 MC questions on Brightspace |
| Problem 1: Fourier | ~10 min | FT, bandwidth, energy, duality |
| Problem 2: AM Power | ~10 min | Parameters, overmodulation, power, efficiency |
| Problem 3: DSB-SC/SSB | ~10 min | Trig expansion, sidebands, power, SSB |
| Problem 4: OOK | ~10 min | Bit duration, bandwidth, waveform sketch |
| Problem 5: Superheterodyne | ~10 min | LO/image frequencies, mitigation, IF trade-off |
| Review | ~10 min | Check answers, verify units |
| **Total** | **75 min** | |

---

## Common Mistakes to Avoid

**Fourier Transform:**
- Forgetting the amplitude scaling: $X(f) = AT \cdot \text{sinc}(fT)$, not just $\text{sinc}(fT)$
- Confusing first null ($1/T$) with null-to-null bandwidth ($2/T$)
- Misreading $|t| \leq \tau/2$ as meaning $T = \tau/2$ instead of $T = \tau$

**AM Power:**
- Forgetting the factor of $1/2$ in power: $P = A^2/(2R)$ for a sinusoid
- Not checking for overmodulation before calculating power
- Confusing $\mu$ (modulation index) with $m(t)$ (message signal)
- Forgetting to include resistance $R$ in power calculations

**DSB-SC / SSB:**
- Forgetting the $1/2$ factor from the trig identity $\cos A \cos B = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$
- SSB bandwidth is $B$, not $2B$

**OOK:**
- Confusing baseband bandwidth ($R_b$) with null-to-null RF bandwidth ($2R_b$)

**Superheterodyne:**
- Sign errors in image frequency calculation
- Confusing the RF preselector filter (rejects image) with the IF filter (selects channel)

---

## Self-Assessment Checklist

Before the exam, make sure you can:

**Fourier Analysis:**
- [ ] Compute FT of rectangular pulse and identify sinc parameters
- [ ] Find first null and null-to-null bandwidth
- [ ] Calculate signal energy in time domain
- [ ] Explain time-frequency duality

**Amplitude Modulation:**
- [ ] Extract $A_c$, $A_m$, $f_c$, $f_m$, $\mu$ from an AM equation
- [ ] Check for overmodulation ($\mu > 1$?)
- [ ] Calculate carrier, sideband, and total power
- [ ] Calculate efficiency $\eta$

**DSB-SC and SSB:**
- [ ] Write DSB-SC expression and expand with trig identity
- [ ] Identify USB and LSB frequency components
- [ ] Calculate DSB-SC power (sum of component powers)
- [ ] Determine SSB-USB components and bandwidth

**On-Off Keying:**
- [ ] Calculate bit duration and null-to-null bandwidth for OOK
- [ ] Compare OOK bandwidth with analog AM bandwidth
- [ ] Sketch OOK waveform from a bit sequence

**Superheterodyne Receiver:**
- [ ] Calculate LO frequency and image frequency
- [ ] Explain the image problem and preselector mitigation
- [ ] Explain why higher IF helps image rejection but hurts channel selectivity

---

## Study Resources

### Homework (Most Important!)

- **Homework 1:** Problems 3, 6, 7 (Euler's formula, signal energy, power signals)
- **Homework 2:** Problems 1-3, 5-7, 9-10 (DSB-SC, AM power, bandwidth, OOK, superheterodyne, AM system design)
- **Homework 2 Bonus 1:** SSB bandwidth and power (extra credit on HW, but good exam practice)
- Redo these problems from scratch — don't just re-read solutions

### Practice Quiz

- Available on Brightspace — take it multiple times
- Covers all MC topics; highest score counts as homework

### Lecture Notebooks

- **L01:** Complex numbers and phasors
- **L02:** Signal analysis, energy/power, I/Q representation
- **L03:** Fourier analysis, rect/sinc, bandwidth
- **L04:** Parseval's theorem, spectral density
- **L05:** AM modulation, DSB-SC, envelope detection
- **L06:** ASK/OOK, spectral analysis, superheterodyne
- **L07:** SSB, Hilbert transform, VSB

### Textbook

- Chapter 2.1-2.5: Fourier Transform and properties
- Chapter 3.1-3.3: AM, DSB-SC
- Chapter 3.6-3.8: SSB, VSB
- Chapter 7.1-7.2: ASK, OOK

---

**Good luck!**
