# W3USR Activity 2: Digital Modes & Data Communication

**EE 451: Communications Systems**

**Name:** _________________________ **Date:** _____________

---

## Objectives

1. Observe and decode digital communication modes on HF
2. Understand the modulation techniques used in amateur digital modes
3. Compare bandwidth, speed, and performance of different modes
4. Relate digital modes to course concepts (FSK, PSK, OFDM)
5. Decode real signals using software

---

## Equipment & Software

- W3USR station equipment
- Computer with audio interface to radio
- Software: Fldigi, WSJT-X, or JS8Call
- Headphones for monitoring

---

## Part 1: Digital Mode Overview (15 points)

### Task 1.1: Digital Mode Comparison

Research and complete this comparison table:

| Mode | Modulation Type | Bandwidth | Data Rate | Typical Use |
|------|----------------|-----------|-----------|-------------|
| RTTY | FSK | ~300 Hz | 45 baud | Contest, DX |
| PSK31 |  |  |  |  |
| FT8 |  |  |  |  |
| FT4 |  |  |  |  |
| JS8Call |  |  |  |  |
| Winlink |  |  |  |  |
| SSTV |  |  |  |  |

### Question 1.1 (10 points)

a) Why do weak-signal modes like FT8 use such narrow bandwidths?

b) What is the relationship between bandwidth and data rate (Shannon's theorem)?

c) FT8 achieves successful decodes at -20 dB SNR. How is this possible when voice requires positive SNR?

**Your Answer:**

*[Write your answer here]*

---

## Part 2: Receiving and Decoding FT8/FT4 (30 points)

### Task 2.1: Configure WSJT-X

1. Launch WSJT-X software
2. Configure audio input from radio
3. Set correct time synchronization (critical for FT8!)
4. Select mode: FT8
5. Choose frequency (e.g., 14.074 MHz for 20m)

**Screenshot 2.1:** WSJT-X main window showing decoded signals.

*[Insert screenshot]*

### Task 2.2: Log Decoded Stations

Monitor FT8 for 10-15 minutes and log decoded stations:

| Time (UTC) | Callsign | Grid Square | Distance (km) | SNR (dB) | Message Type |
|------------|----------|-------------|---------------|----------|--------------|
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

### Task 2.3: Analyze FT8 Waterfall

Observe the waterfall display:

**Screenshot 2.3:** Waterfall showing multiple FT8 signals.

*[Insert screenshot]*

**Observations:**
1. How many simultaneous signals can you see in one time slot? _______
2. What is the bandwidth of a single FT8 signal? _______ Hz
3. How long is each transmission? _______ seconds
4. What is the time between transmission periods? _______ seconds

### Question 2.1 (15 points)

a) FT8 uses GFSK with 8 tones (8-FSK). How many bits does each tone represent?

b) Why is accurate time synchronization (within ±1 second) critical for FT8?

c) FT8 messages are exactly 77 bits. Why is there such a strict limit on message content?

d) What error correction coding does FT8 use, and why is strong FEC essential for weak-signal work?

**Your Answer:**

*[Write your answer here]*

---

## Part 3: PSK31 - Keyboard-to-Keyboard Communication (25 points)

### Task 3.1: Configure Fldigi for PSK31

1. Launch Fldigi
2. Configure audio interface
3. Set mode to PSK31
4. Tune to PSK frequencies:
   - 20m: 14.070 MHz
   - 40m: 7.070 MHz

**Screenshot 3.1:** Fldigi waterfall showing PSK31 signals.

*[Insert screenshot]*

### Task 3.2: Decode PSK31 Transmissions

Click on a PSK31 signal in the waterfall and read the decoded text:

**Decoded Text Sample:**

```
[Copy decoded text here - several lines of a QSO]








```

### Task 3.3: Analyze PSK31 Characteristics

1. **Bandwidth of PSK31 signal:** _______ Hz
2. **Characters per minute (approximate):** _______
3. **Compare to RTTY bandwidth:** _______

**Screenshot 3.3:** Close-up of a single PSK31 signal in the waterfall.

*[Insert screenshot]*

### Question 3.1 (10 points)

a) PSK31 uses BPSK at 31.25 baud. Why was this specific baud rate chosen?

b) Compare the bandwidth efficiency of PSK31 vs. SSB voice. Which is more efficient?

c) PSK31 uses Varicode - a variable-length character encoding. Why is this more efficient than fixed-length codes?

**Your Answer:**

*[Write your answer here]*

---

## Part 4: Comparing Mode Performance (20 points)

### Task 4.1: Signal Quality Comparison

If possible, observe the same station on different modes or compare similar signals:

| Mode | Observed SNR | Decode Success | Bandwidth | Info Rate |
|------|--------------|----------------|-----------|-----------|
| FT8  |  | Yes/No |  |  |
| PSK31 |  | Yes/No |  |  |
| SSB Voice |  | Readable? |  |  |

### Task 4.2: Spectral Efficiency Calculation

Calculate bits per second per Hz for each mode:

| Mode | Data Rate (bps) | Bandwidth (Hz) | Spectral Efficiency (bps/Hz) |
|------|-----------------|----------------|------------------------------|
| FT8  |  |  |  |
| PSK31 |  |  |  |
| RTTY |  |  |  |

### Question 4.1 (10 points)

a) FT8 has very low data rate but works at extremely low SNR. PSK31 has higher data rate but needs stronger signals. Explain this trade-off using Shannon's capacity formula: C = B·log₂(1 + SNR)

b) Why might an operator choose PSK31 over FT8 for an actual conversation?

c) For emergency communication, which mode would you recommend and why?

**Your Answer:**

*[Write your answer here]*

---

## Part 5: Digital Mode Technology (10 points)

### Task 5.1: Modulation Analysis

For each mode, identify the modulation technique used:

| Mode | Base Modulation | Symbol Rate | Coding/Encoding |
|------|-----------------|-------------|-----------------|
| FT8  |  |  |  |
| PSK31 |  |  |  |
| RTTY |  |  |  |
| Winlink (ARDOP) |  |  |  |

### Question 5.1 (10 points)

a) Modern modes like FT8 use forward error correction (FEC). Explain how FEC improves performance at low SNR.

b) OFDM is used in many digital modes (Winlink, some HF data systems). Why is OFDM advantageous for HF channels with multipath?

c) What is the role of interleaving in digital mode error correction?

**Your Answer:**

*[Write your answer here]*

---

## Lab Summary

### Mode Comparison Summary

| Mode | Best For | SNR Required | Bandwidth | Interactive? |
|------|----------|--------------|-----------|--------------|
| FT8  |  |  |  |  |
| PSK31 |  |  |  |  |
| RTTY |  |  |  |  |
| JS8Call |  |  |  |  |

### Connections to Course Material

| Course Topic | Digital Mode Application |
|--------------|-------------------------|
| FSK Modulation | RTTY, FT8 tones |
| PSK Modulation |  |
| Shannon Capacity |  |
| Forward Error Correction |  |
| Bandwidth Efficiency |  |

### Personal Observations

What did you find most interesting about digital modes? How do they compare to your expectations?

*[Write your reflection here]*

---

## Submission Checklist

- [ ] All tables completed
- [ ] Screenshots inserted
- [ ] Decoded text samples included
- [ ] Station logs completed
- [ ] All questions answered
- [ ] Reflections completed

---

*Submit to Brightspace by due date.*
