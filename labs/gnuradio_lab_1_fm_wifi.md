# GNU Radio Lab 1: FM Broadcasting & WiFi Signals

**EE 451: Communications Systems**

**Name:** _________________________ **Date:** _____________

---

## Objectives

1. Use RTL-SDR to receive and demodulate FM broadcast signals
2. Understand frequency deviation and audio bandwidth in FM
3. Observe WiFi signals in the 2.4 GHz spectrum
4. Analyze real-world RF spectrum characteristics
5. Build GNU Radio flowgraphs for signal reception

---

## Equipment Required

- Computer with GNU Radio Companion installed
- RTL-SDR USB dongle
- Antenna (included with RTL-SDR)

---

## Part 1: RTL-SDR Setup and Verification (15 points)

### Task 1.1: Verify RTL-SDR Connection

1. Connect the RTL-SDR dongle to your computer
2. Open a terminal and run:
   ```bash
   rtl_test
   ```
3. Verify the dongle is detected

**Screenshot 1.1:** Paste a screenshot of successful `rtl_test` output here.

*[Insert screenshot]*

### Task 1.2: Launch GNU Radio Companion

1. Open GNU Radio Companion:
   ```bash
   gnuradio-companion
   ```
2. Create a new flowgraph
3. Add the following blocks:
   - **RTL-SDR Source** (from `osmocom` category)
   - **QT GUI Frequency Sink**
   - **QT GUI Waterfall Sink**

4. Configure the RTL-SDR Source:
   - Sample Rate: 2.4 MHz (2400000)
   - Center Frequency: 100 MHz (for FM band)
   - RF Gain: 40 dB
   - IF Gain: 20 dB

5. Connect the source to both sinks

**Screenshot 1.2:** Paste a screenshot of your flowgraph here.

*[Insert screenshot]*

### Question 1.1 (5 points)

a) What is the frequency range of the RTL-SDR dongle you're using?

b) What is the maximum sample rate supported?

**Your Answer:**

*[Write your answer here]*

---

## Part 2: FM Broadcast Reception (30 points)

### Task 2.1: Build FM Receiver Flowgraph

Create a flowgraph with the following blocks:

1. **RTL-SDR Source**
   - Sample Rate: 2.4 MHz
   - Center Frequency: [Your local FM station, e.g., 91.5 MHz]
   - Gains: Adjust as needed

2. **Low Pass Filter**
   - Cutoff Frequency: 100 kHz
   - Transition Width: 10 kHz
   - Decimation: 10

3. **WBFM Receive** (Wideband FM demodulator)
   - Quadrature Rate: 240 kHz (after decimation)
   - Audio Decimation: 5

4. **Rational Resampler** (if needed to get 48 kHz audio)

5. **Audio Sink**
   - Sample Rate: 48000

6. Add visualization:
   - QT GUI Frequency Sink (after RTL-SDR)
   - QT GUI Frequency Sink (after audio)

**Screenshot 2.1:** Your complete FM receiver flowgraph.

*[Insert screenshot]*

### Task 2.2: Tune to Different Stations

1. Run the flowgraph
2. Tune to at least 3 different FM stations
3. Record observations in the table below:

| Station Frequency | Call Sign (if known) | Signal Strength | Audio Quality |
|-------------------|----------------------|-----------------|---------------|
|                   |                      |                 |               |
|                   |                      |                 |               |
|                   |                      |                 |               |

### Task 2.3: Observe FM Spectrum Characteristics

1. Zoom in on a single FM station in the frequency sink
2. Observe the occupied bandwidth

**Screenshot 2.3:** Spectrum of a single FM broadcast station showing bandwidth.

*[Insert screenshot]*

### Question 2.1 (15 points)

a) What is the approximate bandwidth occupied by an FM broadcast station (measure from your spectrum display)?

b) The FCC allocates 200 kHz per FM station. Why is this more than the audio bandwidth (15 kHz)?

c) Compare the spectrum of a station playing music vs. speech. What differences do you observe?

**Your Answer:**

*[Write your answer here]*

### Task 2.4: Explore Stereo FM (Optional Bonus)

FM stereo uses a 19 kHz pilot tone and L-R difference signal at 38 kHz.

1. Add an **FFT** block after the FM demodulator
2. Look for the 19 kHz pilot tone and 38 kHz subcarrier

**Screenshot 2.4:** Spectrum showing stereo pilot tone (if visible).

*[Insert screenshot]*

---

## Part 3: Frequency Deviation Measurement (20 points)

### Task 3.1: Measure Frequency Deviation

The FM broadcast standard uses ±75 kHz maximum deviation.

1. Observe the spectrum during loud audio passages
2. Observe the spectrum during quiet passages
3. Note how the occupied bandwidth changes

### Question 3.1 (10 points)

a) During loud audio, does the FM signal's occupied bandwidth increase or decrease?

b) FM stations use "pre-emphasis" to boost high frequencies before transmission. Why is this done?

c) What is the modulation index (β) for an FM station with 75 kHz deviation and 15 kHz audio bandwidth? Use: β = Δf/fm

**Your Answer:**

*[Write your answer here]*

### Task 3.2: Compare NBFM vs WBFM

Try receiving a narrowband FM signal (if available):
- Public safety or amateur radio: 144-148 MHz or 440-450 MHz
- NBFM uses ±5 kHz deviation

### Question 3.2 (10 points)

a) What is the bandwidth difference between WBFM (broadcast) and NBFM?

b) Why do mobile radios use NBFM instead of WBFM?

**Your Answer:**

*[Write your answer here]*

---

## Part 4: WiFi Spectrum Observation (25 points)

### Task 4.1: View 2.4 GHz WiFi Spectrum

**Note:** RTL-SDR typically covers up to ~1.7 GHz. For 2.4 GHz, you may need to:
- Use a downconverter, or
- Use a different SDR (HackRF, USRP), or
- Observe the spectrum using `hackrf_sweep` or similar tool

If RTL-SDR cannot reach 2.4 GHz, complete this section using:
1. WiFi analyzer app on your phone, or
2. Spectrum screenshots from instructor materials

### WiFi Channel Allocation

| Channel | Center Frequency | Notes |
|---------|------------------|-------|
| 1       | 2.412 GHz        |       |
| 6       | 2.437 GHz        | Common default |
| 11      | 2.462 GHz        |       |

**Screenshot 4.1:** 2.4 GHz WiFi spectrum showing multiple access points.

*[Insert screenshot or describe observations]*

### Task 4.2: Identify WiFi Characteristics

Observe and record:

1. **Channel width:** _________________ MHz
2. **OFDM subcarrier spacing visible?** Yes / No
3. **Approximate power level difference between channels:** _______ dB

### Question 4.1 (15 points)

a) Standard 802.11n WiFi channels are 20 MHz wide. Why don't adjacent channels (e.g., 1 and 2) interfere with each other if they're only 5 MHz apart?

b) How many non-overlapping 20 MHz channels exist in the 2.4 GHz band?

c) Modern 802.11ac/ax uses 80 MHz or 160 MHz channels in the 5 GHz band. What is the trade-off between wider channels and coverage?

**Your Answer:**

*[Write your answer here]*

### Task 4.3: Observe WiFi Traffic Patterns

1. Watch the spectrum while:
   - Streaming video
   - No network activity
   - Downloading a large file

2. Note the difference in spectrum activity

**Observations:**

*[Describe what you observed]*

---

## Part 5: Advanced Exploration (10 points)

### Task 5.1: Explore Other Signals (Choose One)

Using your RTL-SDR, find and observe one of the following:

- [ ] **ADS-B aircraft signals** (1090 MHz)
- [ ] **NOAA weather satellites** (137 MHz)
- [ ] **Amateur radio** (144-148 MHz or 420-450 MHz)
- [ ] **Pager signals** (~929 MHz)
- [ ] **Weather radio** (162.4-162.55 MHz)

**What signal did you find?** _______________________

**Screenshot 5.1:** Spectrum of the signal you discovered.

*[Insert screenshot]*

**Description:** Describe the signal characteristics (bandwidth, modulation type if known, activity pattern).

*[Write your description here]*

---

## Lab Summary

### Key Concepts Learned

1. **FM Broadcasting**: ±75 kHz deviation, 200 kHz channel spacing
2. **SDR Architecture**: RTL-SDR samples RF directly, software does demodulation
3. **WiFi Spectrum**: 20/40/80 MHz channels, OFDM modulation, overlapping channels
4. **Real-world signals**: Impairments, interference, varying signal strengths

### Practical Skills Developed

- [ ] Built working GNU Radio flowgraph
- [ ] Tuned and received FM broadcast signals
- [ ] Analyzed RF spectrum characteristics
- [ ] Identified different signal types in spectrum

---

## Submission Checklist

- [ ] All screenshots inserted
- [ ] All questions answered
- [ ] All tables completed
- [ ] Flowgraph files (.grc) attached
- [ ] Document saved as PDF

**Files to Submit:**
1. This completed worksheet (PDF)
2. fm_receiver.grc (your FM receiver flowgraph)
3. Any additional flowgraphs created

---

*Submit to Brightspace by due date.*
