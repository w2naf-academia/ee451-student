# GNU Radio Lab 2: Noise, SNR, and Signal Quality

**EE 451: Communications Systems**

**Name:** _________________________ **Date:** _____________

---

## Objectives

1. Understand noise characteristics in communication systems
2. Measure and calculate Signal-to-Noise Ratio (SNR)
3. Observe the effect of noise on signal quality
4. Implement noise addition and filtering in GNU Radio
5. Relate SNR to practical communication performance

---

## Equipment Required

- Computer with GNU Radio Companion installed
- RTL-SDR USB dongle (for Part 4)
- Antenna

---

## Part 1: Gaussian Noise Characteristics (20 points)

### Task 1.1: Generate and Visualize AWGN

Create a flowgraph to generate and analyze Additive White Gaussian Noise (AWGN):

1. Add **Noise Source** block
   - Type: Gaussian
   - Amplitude: 1.0

2. Add visualization blocks:
   - **QT GUI Time Sink**
   - **QT GUI Frequency Sink**
   - **QT GUI Histogram Sink**

3. Set sample rate to 32000 Hz

**Screenshot 1.1:** Your noise generation flowgraph.

*[Insert screenshot]*

**Screenshot 1.2:** Time domain view of Gaussian noise.

*[Insert screenshot]*

**Screenshot 1.3:** Frequency spectrum of white noise (should be flat).

*[Insert screenshot]*

**Screenshot 1.4:** Histogram showing Gaussian distribution.

*[Insert screenshot]*

### Question 1.1 (10 points)

a) Why is the frequency spectrum of "white" noise flat?

b) What is the relationship between the noise amplitude setting and the noise power (variance)?

c) From your histogram, estimate the standard deviation of the noise. How does this compare to the amplitude setting?

**Your Answer:**

*[Write your answer here]*

---

## Part 2: Signal-to-Noise Ratio Measurement (30 points)

### Task 2.1: Create Signal + Noise System

Build a flowgraph with:

1. **Signal Source** (sine wave)
   - Frequency: 1000 Hz
   - Amplitude: 1.0
   - Sample Rate: 32000

2. **Noise Source** (Gaussian)
   - Amplitude: Variable (start at 0.1)

3. **Add** block to combine signal and noise

4. Visualization:
   - QT GUI Time Sink (show both clean and noisy signals)
   - QT GUI Frequency Sink

5. Add **QT GUI Range** slider to control noise amplitude (0.01 to 2.0)

**Screenshot 2.1:** Flowgraph with signal, noise, and variable control.

*[Insert screenshot]*

### Task 2.2: Measure SNR at Different Noise Levels

For each noise amplitude setting, measure:
- Signal power from the spectrum display
- Noise power from the spectrum display (noise floor)
- Calculate SNR in dB

**SNR Measurement Table:**

| Noise Amplitude | Signal Power (dB) | Noise Floor (dB) | SNR (dB) | Signal Quality |
|-----------------|-------------------|------------------|----------|----------------|
| 0.1             |                   |                  |          |                |
| 0.3             |                   |                  |          |                |
| 0.5             |                   |                  |          |                |
| 1.0             |                   |                  |          |                |
| 2.0             |                   |                  |          |                |

### Task 2.3: Visual Comparison

**Screenshot 2.3a:** Time domain at high SNR (noise amplitude = 0.1).

*[Insert screenshot]*

**Screenshot 2.3b:** Time domain at low SNR (noise amplitude = 1.0).

*[Insert screenshot]*

### Question 2.1 (10 points)

a) At what SNR does the sine wave become difficult to identify visually in the time domain?

b) Even when the sine wave is hidden in noise visually, can you still see it in the frequency domain? Why?

c) If signal amplitude is 1.0 and noise amplitude is 0.5, calculate the expected SNR in dB.

**Your Answer:**

*[Write your answer here]*

---

## Part 3: Filtering to Improve SNR (25 points)

### Task 3.1: Add Low-Pass Filter

Modify your flowgraph to include filtering:

1. Add **Low Pass Filter** after the Add block
   - Cutoff Frequency: 1500 Hz
   - Transition Width: 500 Hz

2. Display both filtered and unfiltered signals

**Screenshot 3.1:** Flowgraph with filter added.

*[Insert screenshot]*

### Task 3.2: Measure SNR Improvement

Compare SNR before and after filtering:

| Noise Amplitude | SNR Before Filter (dB) | SNR After Filter (dB) | Improvement (dB) |
|-----------------|------------------------|----------------------|------------------|
| 0.5             |                        |                      |                  |
| 1.0             |                        |                      |                  |

**Screenshot 3.2:** Spectrum comparison before/after filtering.

*[Insert screenshot]*

### Task 3.3: Experiment with Filter Bandwidth

Try different filter cutoff frequencies:

| Cutoff Frequency | SNR (dB) | Signal Distortion? |
|------------------|----------|-------------------|
| 5000 Hz          |          |                   |
| 2000 Hz          |          |                   |
| 1500 Hz          |          |                   |
| 1100 Hz          |          |                   |
| 1000 Hz          |          |                   |

### Question 3.1 (15 points)

a) Why does a narrower filter bandwidth improve SNR?

b) What happens to the signal when the filter bandwidth is too narrow (e.g., below the signal frequency)?

c) In practice, why can't we always use the narrowest possible filter?

d) The noise power in a bandwidth B is N = N₀ × B. If you halve the filter bandwidth, how much does the SNR improve (in dB)?

**Your Answer:**

*[Write your answer here]*

---

## Part 4: Real-World SNR with RTL-SDR (25 points)

### Task 4.1: Measure FM Station SNR

1. Build FM receiver flowgraph (from Lab 1)
2. Tune to a strong local FM station
3. Tune to a weak/distant FM station
4. Compare signal quality

**Screenshot 4.1a:** Spectrum of strong FM station.

*[Insert screenshot]*

**Screenshot 4.1b:** Spectrum of weak FM station.

*[Insert screenshot]*

### Task 4.2: Estimate SNR from Spectrum

For each station:

| Station | Freq (MHz) | Peak Power (dB) | Noise Floor (dB) | Est. SNR (dB) | Audio Quality |
|---------|------------|-----------------|------------------|---------------|---------------|
| Strong  |            |                 |                  |               |               |
| Weak    |            |                 |                  |               |               |

### Task 4.3: Effect of Antenna Position

1. Move antenna to different positions
2. Observe SNR changes

**Observations:**

*[Describe how antenna position affects signal quality]*

### Question 4.1 (10 points)

a) What causes the noise floor in the RTL-SDR receiver?

b) Why does the FM signal "capture" effect mean that only the strongest signal is heard when two stations are close in frequency?

c) FM is often described as having a "threshold effect." What happens when SNR drops below about 10-12 dB?

**Your Answer:**

*[Write your answer here]*

---

## Part 5: Noise Figure and System SNR (Bonus - 10 points)

### Background

The noise figure (NF) describes how much noise a component adds:

$$NF = 10 \log_{10}\left(\frac{SNR_{in}}{SNR_{out}}\right)$$

For cascaded stages (Friis formula):
$$NF_{total} = NF_1 + \frac{NF_2 - 1}{G_1} + \frac{NF_3 - 1}{G_1 G_2} + ...$$

### Question 5.1 (Bonus)

A receiver has these stages:
- LNA: Gain = 20 dB, NF = 1.5 dB
- Mixer: Gain = -6 dB (loss), NF = 8 dB
- IF Amp: Gain = 30 dB, NF = 3 dB

a) Calculate the total system noise figure.

b) Why is the first stage (LNA) noise figure most critical?

c) If the RTL-SDR has NF ≈ 4-6 dB, would adding a low-noise amplifier (LNA) with NF = 1 dB and G = 20 dB at the antenna improve performance? By how much?

**Your Answer:**

*[Write your answer here]*

---

## Lab Summary

### Key Concepts

1. **AWGN**: Gaussian amplitude distribution, flat (white) frequency spectrum
2. **SNR**: SNR(dB) = 10·log₁₀(Psignal/Pnoise)
3. **Filtering**: Narrower bandwidth reduces noise power
4. **Trade-off**: Bandwidth vs. SNR vs. data rate
5. **Noise Figure**: Describes noise added by receiver components

### Important Formulas

- SNR (dB) = Signal Power (dB) - Noise Power (dB)
- Noise Power = kTB (thermal noise)
- Filter SNR improvement = 10·log₁₀(BWold/BWnew) dB

### Practical Insights

- First stage gain and NF are most important
- Filtering helps but can't recover information lost to noise
- Real systems have multiple noise sources

---

## Submission Checklist

- [ ] All screenshots inserted
- [ ] All measurement tables completed
- [ ] All questions answered
- [ ] Flowgraph files (.grc) attached

**Files to Submit:**
1. This completed worksheet (PDF)
2. noise_analysis.grc
3. snr_measurement.grc
4. filter_comparison.grc

---

*Submit to Brightspace by due date.*
