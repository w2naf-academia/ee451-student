# W3USR Activity 3: Satellite Communication

**EE 451: Communications Systems**

**⭐ OPTIONAL EXTRA CREDIT ACTIVITY ⭐**

**Name:** _________________________ **Date:** _____________

---

## Objectives

1. Understand satellite orbit types and their communication characteristics
2. Calculate Doppler shift for LEO satellite passes
3. Observe or participate in amateur satellite communication
4. Analyze satellite link budgets
5. Connect satellite communication to course concepts

---

## Part 1: Satellite Fundamentals (20 points)

### Task 1.1: Orbit Type Comparison

Complete the comparison table:

| Orbit Type | Altitude (km) | Period | Latency | Coverage | Example Satellites |
|------------|---------------|--------|---------|----------|-------------------|
| LEO | 200-2000 |  |  |  |  |
| MEO | 2000-35786 |  |  |  |  |
| GEO | 35786 |  |  |  |  |
| HEO |  |  |  |  |  |

### Task 1.2: Amateur Satellite Resources

Visit https://amsat.org/status and identify active amateur satellites:

| Satellite | Uplink Freq | Downlink Freq | Mode | Status |
|-----------|-------------|---------------|------|--------|
| ISS |  |  |  |  |
| SO-50 |  |  |  |  |
| AO-91 |  |  |  |  |
| RS-44 |  |  |  |  |
|  |  |  |  |  |

### Question 1.1 (10 points)

a) Why do LEO satellites require tracking antennas while GEO satellites use fixed dishes?

b) What is the maximum line-of-sight distance for a LEO satellite at 400 km altitude when directly overhead? When at 10° elevation?

c) Why is the ISS orbit inclined at 51.6° rather than being equatorial?

**Your Answer:**

*[Write your answer here]*

---

## Part 2: Doppler Shift Calculation (25 points)

### Background

For a satellite moving at velocity v, the Doppler shift is:

$$\Delta f = f_0 \cdot \frac{v_r}{c}$$

where $v_r$ is the radial velocity component toward the observer.

Maximum Doppler occurs when satellite is at horizon, minimum (zero) at closest approach.

### Task 2.1: Calculate Doppler for ISS

The ISS orbits at approximately:
- Altitude: 420 km
- Orbital velocity: 7.66 km/s
- Downlink frequency: 145.80 MHz

**Calculate:**

1. Maximum radial velocity (at horizon): _______ km/s

2. Maximum Doppler shift: _______ Hz

3. Total Doppler swing (AOS to LOS): _______ Hz

### Task 2.2: Doppler Compensation

During a pass, the receiver must compensate for Doppler. Plot the expected Doppler curve:

| Time from AOS | Elevation | Doppler Shift (Hz) |
|---------------|-----------|-------------------|
| 0 min (AOS) | ~0° |  |
| 2 min | ~20° |  |
| 4 min (TCA) | ~60° |  |
| 6 min | ~20° |  |
| 8 min (LOS) | ~0° |  |

**Sketch the Doppler curve:**

```
        +3000 |
              |
Doppler  0 Hz |--------------------
(Hz)          |
        -3000 |
              +------------------------
               AOS    TCA    LOS
                  Time →
```

### Question 2.1 (15 points)

a) If you don't correct for Doppler on a 145 MHz FM satellite, what happens to the received audio?

b) Why is Doppler correction more critical for higher frequencies?

c) A satellite downlink is at 2.4 GHz. What is the maximum Doppler shift for a LEO satellite? Why is this problematic for data communications?

d) How do digital modes like FT8 handle Doppler shift on satellite passes?

**Your Answer:**

*[Write your answer here]*

---

## Part 3: Satellite Pass Observation (25 points)

### Task 3.1: Predict Satellite Pass

Use a tracking tool (N2YO.com, Heavens-Above, GPREDICT, or phone app) to find upcoming passes:

**Satellite:** _______________________

**Pass Details:**

| Parameter | Value |
|-----------|-------|
| Date/Time (Local) |  |
| AOS Time |  |
| AOS Azimuth |  |
| Maximum Elevation |  |
| TCA Time |  |
| LOS Time |  |
| LOS Azimuth |  |
| Pass Duration |  |

**Screenshot 3.1:** Pass prediction from tracking software.

*[Insert screenshot]*

### Task 3.2: Observe/Listen to Pass

If live observation is possible, record your observations:

| Time | Azimuth | Elevation | Signal Strength | Notes |
|------|---------|-----------|-----------------|-------|
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

**Audio recording made?** Yes / No

**Stations heard (if FM repeater):**

*[List callsigns/activity heard]*

### Task 3.3: Compare to Prediction

How did the actual pass compare to the prediction?

| Parameter | Predicted | Observed | Difference |
|-----------|-----------|----------|------------|
| AOS Time |  |  |  |
| Max Elevation |  |  |  |
| Signal Strength |  | N/A |  |

### Question 3.1 (10 points)

a) Why do low-elevation passes have weaker signals than high-elevation passes?

b) What causes QSB (signal fading) during a satellite pass?

c) Why is FM commonly used for LEO amateur satellites rather than SSB?

**Your Answer:**

*[Write your answer here]*

---

## Part 4: Link Budget Analysis (20 points)

### Task 4.1: Satellite Link Budget

Calculate the link budget for a LEO satellite downlink:

**Given parameters:**
- Frequency: 435 MHz
- Satellite altitude: 800 km (slant range at 30° elevation ≈ 1500 km)
- Satellite transmit power: 1 W (30 dBm)
- Satellite antenna gain: 0 dBi (omnidirectional)
- Ground station antenna gain: 10 dBi
- Receiver noise figure: 2 dB
- Receiver bandwidth: 15 kHz

**Calculate:**

1. **Free Space Path Loss:**
   $$FSPL = 20\log_{10}(d) + 20\log_{10}(f) + 32.44$$

   FSPL = _______ dB

2. **EIRP (Satellite):**
   EIRP = P_tx + G_tx = _______ dBm

3. **Received Power:**
   P_rx = EIRP - FSPL + G_rx = _______ dBm

4. **Noise Power:**
   N = kTB = -174 + 10·log₁₀(B) + NF = _______ dBm

5. **SNR:**
   SNR = P_rx - N = _______ dB

6. **Is link viable?** (Need >10 dB SNR for FM) Yes / No

### Task 4.2: Link Budget Sensitivity

What happens if:

| Change | Effect on SNR |
|--------|---------------|
| Double the slant range |  |
| Double the frequency |  |
| Use 20 dBi antenna |  |
| Satellite at 3 W power |  |

### Question 4.1 (10 points)

a) Why do GEO satellites require much higher transmit power than LEO satellites?

b) Calculate the one-way latency for GEO (35,786 km) vs. LEO (400 km) satellites.

c) Starlink operates at 12 GHz. How does this affect the link budget compared to 435 MHz amateur satellites?

**Your Answer:**

*[Write your answer here]*

---

## Part 5: Advanced Topics (10 points)

### Question 5.1 (10 points)

a) What is "linear transponder" mode vs. "FM repeater" mode on amateur satellites? What are the advantages of each?

b) Explain the concept of "full duplex" satellite operation. Why do you need separate receive and transmit antennas?

c) Some amateur satellites use "store and forward" for digital messages. How does this work, and why is it useful for limited pass times?

d) The ISS uses packet radio (APRS) on 145.825 MHz. What modulation does APRS use, and how does the digipeater function?

**Your Answer:**

*[Write your answer here]*

---

## Lab Summary

### Key Concepts

1. **Orbit Characteristics**: LEO (low latency, Doppler), GEO (high latency, fixed pointing)
2. **Doppler Effect**: Δf/f = v_r/c, critical for tracking and communication
3. **Link Budget**: EIRP - Path Loss + Rx Gain - Noise = SNR
4. **Pass Geometry**: Elevation affects path loss, duration, and Doppler rate

### Numerical Results Summary

| Parameter | Calculated Value |
|-----------|------------------|
| Max Doppler (145 MHz) |  |
| Path Loss (435 MHz, 1500 km) |  |
| Received Power |  |
| Required SNR for FM |  |

### Connections to Course Material

| Course Topic | Satellite Application |
|--------------|----------------------|
| Doppler Effect |  |
| Link Budget |  |
| Path Loss |  |
| FM Modulation |  |
| Digital Modes |  |

### Personal Reflection

Describe your experience observing or thinking about satellite communication. How does this connect to commercial satellite systems (Starlink, GPS, etc.)?

*[Write your reflection here]*

---

## Submission Checklist

- [ ] All calculation tables completed
- [ ] Doppler shift calculations shown
- [ ] Pass prediction screenshot included
- [ ] Link budget calculated
- [ ] All questions answered
- [ ] Reflection completed

---

*Submit to Brightspace by due date.*
