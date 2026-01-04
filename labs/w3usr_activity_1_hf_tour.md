# W3USR Activity 1: HF Station Tour & Propagation

**EE 451: Communications Systems**

**Name:** _________________________ **Date:** _____________

---

## Objectives

1. Tour the W3USR amateur radio station and identify equipment
2. Understand HF propagation mechanisms
3. Listen to live HF signals and identify communication modes
4. Learn about antenna types and their radiation patterns
5. Connect theoretical concepts to real-world radio communication

---

## Part 1: Station Tour (25 points)

### Task 1.1: Equipment Identification

During the station tour, identify and describe the following equipment:

| Equipment | Manufacturer/Model | Purpose/Function |
|-----------|-------------------|------------------|
| HF Transceiver |  |  |
| VHF/UHF Transceiver |  |  |
| Antenna Tuner |  |  |
| Power Amplifier (if present) |  |  |
| SWR Meter |  |  |
| Power Supply |  |  |

### Task 1.2: Station Block Diagram

Draw a simplified block diagram showing how the station components connect:

```
[Draw your block diagram here - show signal path from microphone to antenna]










```

### Question 1.1 (10 points)

a) What is the purpose of an antenna tuner? Why is it needed?

b) What does SWR (Standing Wave Ratio) measure, and why is low SWR important?

c) What is the maximum power output (in watts) that the station can produce on HF?

**Your Answer:**

*[Write your answer here]*

---

## Part 2: Antenna Systems (25 points)

### Task 2.1: Identify Antennas

List the antennas available at W3USR:

| Antenna Type | Bands Covered | Polarization | Approximate Gain |
|--------------|---------------|--------------|------------------|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

### Task 2.2: Antenna Characteristics

For the main HF antenna, answer:

1. **Type:** _______________________
2. **Height above ground:** _______ meters/feet
3. **Orientation:** (directional/omnidirectional) _______________________
4. **Feed type:** _______________________

### Question 2.1 (15 points)

a) A half-wave dipole for 20 meters (14 MHz) is approximately how long?

   *Hint: λ = c/f, dipole length ≈ λ/2*

b) Why do HF antennas need to be much larger than VHF/UHF antennas?

c) What is the advantage of a beam antenna (like a Yagi) over a dipole?

d) How does antenna height affect radiation pattern and propagation distance?

**Your Answer:**

*[Write your answer here]*

---

## Part 3: HF Propagation (25 points)

### Task 3.1: Current Propagation Conditions

Check current propagation conditions using one of these resources:
- https://www.hamqsl.com/solar.html
- https://www.solarham.net/
- Station propagation prediction software

Record the current conditions:

| Parameter | Value | Meaning |
|-----------|-------|---------|
| Solar Flux Index (SFI) |  |  |
| Sunspot Number (SSN) |  |  |
| K-Index |  |  |
| A-Index |  |  |
| Band Conditions (20m) |  |  |
| Band Conditions (40m) |  |  |

### Task 3.2: Listen for DX Stations

Tune the receiver to the following frequencies and log what you hear:

| Band | Frequency | Mode | Station Heard | Location | Signal Strength |
|------|-----------|------|---------------|----------|-----------------|
| 40m  | 7.200 MHz | SSB  |  |  |  |
| 20m  | 14.200 MHz | SSB |  |  |  |
| 17m  | 18.100 MHz | SSB |  |  |  |
| 15m  | 21.200 MHz | SSB |  |  |  |

### Question 3.1 (10 points)

a) What layer of the ionosphere enables long-distance HF propagation during the day? At night?

b) Why do lower frequencies (40m, 80m) work better at night, while higher frequencies (15m, 10m) work better during the day?

c) What is "skip distance" and why does it exist?

d) How do solar flares affect HF propagation?

**Your Answer:**

*[Write your answer here]*

---

## Part 4: Communication Modes (15 points)

### Task 4.1: Identify Different Modes

Listen to the HF bands and identify examples of different modulation types:

| Mode | Frequency Heard | Description of Sound | Bandwidth |
|------|-----------------|---------------------|-----------|
| SSB (Voice) |  |  |  |
| CW (Morse Code) |  |  |  |
| Digital (if heard) |  |  |  |
| AM (if heard) |  |  |  |

### Task 4.2: SSB Observation

When listening to SSB voice:

1. Tune slightly off frequency. What happens to the voice? _______________________

2. Is upper sideband (USB) or lower sideband (LSB) used on 20 meters? _______________________

3. What is the approximate audio bandwidth you hear? _______ Hz to _______ Hz

### Question 4.1 (10 points)

a) Why is SSB more efficient than AM for voice communication?

b) Why does an SSB signal sound "Donald Duck-like" when off frequency?

c) CW (Morse code) can be copied at much lower signal levels than voice. Why?

**Your Answer:**

*[Write your answer here]*

---

## Part 5: Link Budget Estimation (10 points)

### Task 5.1: Estimate a Real Link

For a contact observed during the session:

- **My Location:** _______________________
- **Other Station Location:** _______________________
- **Distance:** _______ km
- **Frequency:** _______ MHz
- **Transmit Power (estimated):** _______ W
- **Antenna Gain (estimated):** _______ dBi

### Basic Link Budget Calculation

Using the free-space path loss formula (approximate, actual ionospheric propagation varies):

$$FSPL_{dB} = 20\log_{10}(d) + 20\log_{10}(f) + 32.44$$

where d is in km and f is in MHz.

**Calculate:**
1. Free Space Path Loss: _______ dB
2. Transmit Power (dBm): _______ dBm
3. EIRP (with antenna): _______ dBm
4. Received Power (rough estimate): _______ dBm

### Question 5.1 (10 points)

a) Why is the actual received power often much higher than free-space path loss would predict for ionospheric propagation?

b) A station with 100W and a 3-element Yagi (8 dBi gain) has what EIRP?

c) Why might a station with 5W (QRP) still make contacts thousands of miles away?

**Your Answer:**

*[Write your answer here]*

---

## Lab Summary

### Key Concepts Learned

1. **HF Station Components**: Transceiver, tuner, SWR meter, power supply, antennas
2. **Antenna Fundamentals**: Length related to wavelength, gain vs. directionality
3. **Ionospheric Propagation**: Skip, critical frequency, MUF, solar effects
4. **HF Modes**: SSB, CW, digital - each with different bandwidth/efficiency tradeoffs

### Connections to Course Material

| Course Topic | Real-World Observation |
|--------------|------------------------|
| Modulation (AM, SSB) |  |
| Bandwidth |  |
| Link Budget |  |
| Propagation |  |
| Noise/SNR |  |

### Personal Observations

What was most interesting or surprising about the HF station experience?

*[Write your reflection here]*

---

## Submission Checklist

- [ ] All equipment tables completed
- [ ] Block diagram drawn
- [ ] Propagation conditions recorded
- [ ] Stations logged
- [ ] All questions answered
- [ ] Summary and reflections completed

---

*Submit to Brightspace by due date.*
