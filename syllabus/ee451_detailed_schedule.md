# EE 451: Communications Systems
## Detailed Lesson-by-Lesson Schedule - Spring 2026

**Class Meeting Times:** Tuesday & Thursday, 2:30 PM - 3:45 PM, Loyola Science Center Room 142<br>
**Textbook:** An Introduction to Analog and Digital Communications (2nd Ed.), Haykin & Moher

---

## Reading Quiz Schedule

10 reading quizzes administered through Brightspace (10 questions randomly selected from 50-question banks):

| Lesson | Date | Topic | Reading |
|--------|------|-------|---------|
| 2 | Thu, Jan 29 | Fourier Transform and Signals | Chapter 2.1 |
| 3 | Tue, Feb 3 | Filtering and Distortion, Bandpass Signals, Hilbert Transform | Chapter 2.2-2.5 |
| 5 | Tue, Feb 10 | Amplitude Modulation Techniques | Chapter 3.1-3.3 |
| 7 | Tue, Feb 17 | SSB, VSB, and Receiver Architectures | Chapter 3.6-3.8 |
| 11 | Tue, Mar 3 | FM/PM Theory and Modulation | Chapter 4.1-4.5 |
| 13 | Tue, Mar 10 | FM Generation and Demodulation | Chapter 4.6-4.8 |
| 17 | Tue, Mar 31 | Pulse Modulation and Digital Transmission | Chapter 6 |
| 23 | Tue, Apr 21 | Probability and Random Variables | Chapter 8.1-8.4 |
| 25 | Tue, Apr 28 | Noise in Communication Systems | Chapter 9 |
| 27 | Tue, May 5 | Digital Performance and BER | Chapter 10 |

**Total Points:** 100 (10 quizzes × 10 points each)

---

## Homework Schedule

| Assignment | Assigned | Due | Topics |
|------------|----------|-----|--------|
| Homework 1 | Thu, Jan 29 | Thu, Feb 5 | Complex numbers, phasors, signals |
| Homework 2 | Thu, Feb 12 | Thu, Feb 19 | AM and ASK |
| Homework 3 | Thu, Mar 5 | Thu, Mar 12 | FM, PM, FSK, BPSK |
| Homework 4 | Thu, Apr 9 | Thu, Apr 16 | M-ary modulation, QAM, EVM |
| Homework 5 | Thu, Apr 30 | Thu, May 7 | Probability, noise, SNR |
| Homework 6 | Thu, May 7 | Thu, May 14 | BER, link budgets, modern systems |

---

## Exam Schedule

| Exam | Date | Coverage |
|------|------|----------|
| Exam 1 | Tue, Feb 24 | Chapters 2-3, 7.1-7.2 (Fourier Analysis & AM) |
| Exam 2 | Tue, Apr 14 | Chapters 4-7 (Modulation & Digital Systems) |
| Final Exam | Week of May 18 | Comprehensive (emphasis on Chapters 8-11) |

---

## Lab Schedule

### Python/Jupyter Labs

| Lab | Week | Date | Topic |
|-----|------|------|-------|
| Python Lab 1 | 2 | Tue, Feb 3 | Fourier Analysis and Spectral Visualization |
| Python Lab 2 | 3 | Thu, Feb 12 | AM/ASK Modulation and Envelope Detection |
| Python Lab 3 | 10 | Tue, Apr 7 | CDMA & Spread Spectrum Simulation |
| Python Lab 4 | 10 | Thu, Apr 9 | QPSK/QAM Simulation with EVM Analysis |
| Python Lab 5 | 14 | Thu, May 7 | BER Performance Simulation |

### GNU Radio Labs

| Lab | Week | Date | Topic |
|-----|------|------|-------|
| GNU Radio Lab 1 | 9 | Thu, Apr 2 | FM Broadcast Reception & WiFi Spectrum Analysis |
| GNU Radio Lab 2 | 13 | Thu, Apr 30 | Noise Analysis and SNR Measurement |

### Baba Yaga's Hut Phasor Labs

| Session | Week | Date | Topic |
|---------|------|------|-------|
| Part 1 | 7 | Thu, Mar 12 | AM Phasor Analysis with I/Q Demodulation |
| Part 2 | 8 | Thu, Mar 26 | DSB-SC, FM, and PM Phasor Analysis |

### W3USR Amateur Radio Station Activities

| Activity | Week | Date | Topic |
|----------|------|------|-------|
| W3USR Activity 1 | 4 | Thu, Feb 19 | HF Station Tour and SSB/AM Reception |
| W3USR Activity 2 | 10 | Thu, Apr 9 | Digital Modes (FT8, APRS, PSK31) |
| W3USR Activity 3 | 15 | Tue, May 12 | Satellite Communications and Tracking |

---

## Phase 1: Foundation (Weeks 1-2)

### Week 1

#### Lesson 1 - Tuesday, January 27
**Course Introduction & Complex Signal Review**
- Course overview, syllabus, grading policy, amateur radio extra credit opportunities
- Introduction to W3USR amateur radio station capabilities
- Cross-disciplinary applications: radar, sonar, audio processing, biomedical
- Complex numbers and Euler's formula review
- Sinusoids: amplitude, frequency, phase
- I/Q (In-phase/Quadrature) representation - industry-critical terminology
- Reading: Chapter 1, Chapter 2.1

**Lab/Activity:** Python/Jupyter setup and environment check
- Install course software (Python, Jupyter, GNU Radio)
- Introduction to NumPy and Matplotlib for signal visualization

#### Lesson 2 - Thursday, January 29
**Signal Analysis Fundamentals**
- Convolution, unit step and impulse functions
- Energy and power signals
- Phasor representation of sinusoids
- Introduction to analytic signals
- Reading: Chapter 2.1

**📝 READING QUIZ 1** (10 points)
- Topic: Fourier Transform and Signals
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

**Note:** Correlation, a related operation to convolution, will be introduced in Lesson 4 after we study Fourier transforms. Correlation is essential for matched filtering and signal detection in communication systems.

**Homework 1 Assigned:** Complex numbers, phasors, basic signal operations

---

### Week 2

#### Lesson 3 - Tuesday, February 3
**Fourier Analysis Essentials**
- Fourier series and Fourier transforms
- Properties of Fourier transforms
- Time-frequency duality
- Bandwidth concepts
- Reading: Chapter 2.2-2.5

**📝 READING QUIZ 2** (10 points)
- Topic: Filtering and Distortion, Bandpass Signals, Hilbert Transform
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

**Lab:** Python Lab 1 - Fourier Analysis
- Generate and plot sinusoids
- Compute and visualize Fourier transforms
- Explore time-frequency duality
- Bandwidth calculations

#### Lesson 4 - Thursday, February 5
**Fourier Analysis Applications**
- Spectral analysis of common signals
- Parseval's theorem and energy spectral density
- Introduction to correlation
- Reading: Chapter 2.2-2.5

**Homework 1 Due**

---

## Phase 2: Modulation Techniques - Integrated Analog & Digital (Weeks 3-8)

### Week 3

#### Lesson 5 - Tuesday, February 10
**Amplitude Modulation Theory**
- Need for modulation
- DSB-SC (Double Sideband Suppressed Carrier) theory
- Full carrier AM
- Envelope detection
- Modulation index and overmodulation
- Reading: Chapter 3.1-3.3

**📝 READING QUIZ 3** (10 points)
- Topic: Amplitude Modulation Techniques
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 6 - Thursday, February 12
**Binary Amplitude Shift Keying (ASK)**
- On-Off Keying (OOK)
- Binary ASK as discrete version of AM
- Spectral characteristics of ASK
- Comparison of analog AM and digital ASK
- Reading: Chapter 7.1-7.2

**Lab:** Python Lab 2 - AM/ASK Modulation
- Simulate AM signals with varying modulation depths
- Implement envelope detection
- Generate and analyze ASK signals
- Compare AM and ASK spectra

**Homework 2 Assigned:** AM and ASK problems

---

### Week 4

#### Lesson 7 - Tuesday, February 17
**AM Systems & SSB**
- Single Sideband (SSB) modulation
- Hilbert transform
- SSB generation (filter method, phasing method)
- Vestigial Sideband (VSB) - brief overview
- Reading: Chapter 3.6-3.8

**📝 READING QUIZ 4** (10 points)
- Topic: SSB, VSB, and Receiver Architectures
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 8 - Thursday, February 19
**Receiver Architectures**
- Superheterodyne receiver design
- Mixer theory and image frequencies
- Direct conversion receivers (produce I/Q baseband)
- Direct sampling receivers (modern high-speed ADC approach)
- Comparison: superheterodyne vs direct conversion vs direct sampling
- Automatic Gain Control (AGC)
- Reading: Chapter 3.6-3.8

**Lab Activity:** W3USR Station Tour & HF Listening
- Tour of W3USR amateur radio station
- Listen to SSB voice communications on HF bands (20m, 40m)
- Identify AM broadcast signals on 80m band
- Demonstrate different receiver modes (AM, SSB, CW)

**Homework 2 Due**

---

### Week 5

#### Lesson 9 - Tuesday, February 24
**EXAM 1: Fourier Analysis & Amplitude Modulation**
- Coverage: Chapters 2-3, 7.1-7.2
- Format: Closed book, equation sheet provided

#### Lesson 10 - Thursday, February 26
**Exam Review & Angle Modulation Introduction**
- Exam 1 review and discussion
- Introduction to frequency and phase modulation
- Narrowband vs. wideband FM
- Reading: Chapter 4.1-4.2

---

### Week 6

#### Lesson 11 - Tuesday, March 3
**FM/PM Theory & Binary FSK**
- FM/PM mathematical representation
- Frequency deviation and modulation index
- Narrowband FM approximation
- Wideband FM characteristics
- Reading: Chapter 4.1-4.5

**📝 READING QUIZ 5** (10 points)
- Topic: FM/PM Theory and Modulation
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 12 - Thursday, March 5
**Binary FSK & MSK**
- Binary Frequency Shift Keying (FSK)
- Continuous Phase FSK (CPFSK)
- Minimum Shift Keying (MSK)
- FSK as digital counterpart to FM
- Comparison of FSK bandwidth to FM (Carson's rule application)
- Reading: Chapter 7.3-7.4

**Homework 3 Assigned:** FM, PM, FSK, BPSK problems

---

### Week 7

#### Lesson 13 - Tuesday, March 10
**FM Generation & Demodulation**
- Direct FM generation (VCO)
- Indirect FM generation (Armstrong method)
- Frequency discriminators
- PLL-based FM demodulation (operates on IQ baseband)
- Reading: Chapter 4.6-4.8

**📝 READING QUIZ 6** (10 points)
- Topic: FM Generation and Demodulation
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 14 - Thursday, March 12
**Binary PSK & Carson's Rule**
- Binary Phase Shift Keying (BPSK) fundamentals
- BPSK as phase modulation of IQ carrier
- Coherent detection of BPSK (requires IQ demodulation)
- Carson's rule for FM bandwidth
- Pre-emphasis and de-emphasis in FM
- Reading: Chapter 4.6-4.8, Chapter 7.2

**Lab Activity:** **"Baba Yaga's Hut" - Phasor Analysis Lab (Part 1 of 2)**
- Build I/Q demodulator using function generators and oscilloscopes
- Examine AM signals in time, frequency, and phasor domains simultaneously
- Vary modulation depth and observe effects in all three representations
- Couple to AM radio for audio demodulation
- Students work in pairs on the one shared setup
- Reference: w8edu_cwru/the-hut-on-phasors-legs.pdf

**Homework 3 Due**

---

**SPRING BREAK: March 14-22 (No Classes)**

---

### Week 8

#### Lesson 15 - Tuesday, March 24
**Pulse Modulation & Sampling Theorem**
- Sampling theorem and Nyquist rate
  - **Real sampling:** 2× bandwidth (traditional approach)
  - **IQ (complex) sampling:** 1× bandwidth (what SDRs like RTL-SDR use)
  - Why the difference: IQ sampling separates positive and negative frequencies
- Aliasing and anti-aliasing filters
- Pulse Amplitude Modulation (PAM)
- Natural and flat-top sampling
- Reading: Chapter 5

#### Lesson 16 - Thursday, March 26
**PCM & Delta Modulation**
- Quantization and quantization noise
- Pulse Code Modulation (PCM)
- Companding (μ-law and A-law)
- Delta modulation and adaptive delta modulation
- Line codes (NRZ, RZ, Manchester, etc.)
- Reading: Chapter 5

**Lab:** **"Baba Yaga's Hut" - Phasor Analysis Lab (Part 2 of 2)**
- Examine DSB-SC (suppressed carrier) signals
- Explore FM and PM in phasor representation
- Vary carrier phase and observe rotation in phasor domain
- Complete lab worksheets and analysis
- Students work in pairs on the one shared setup

---

## Phase 3: Advanced Digital Communications (Weeks 9-11)

### Week 9

#### Lesson 17 - Tuesday, March 31
**Baseband Digital Transmission & Synchronization**
- Intersymbol Interference (ISI) concepts
- Eye diagrams (separate I and Q channel displays)
- Nyquist criterion for zero ISI
- Raised cosine filtering
- Multipath propagation in WiFi and cellular systems
- Carrier and symbol timing synchronization concepts
- Phase-locked loops (PLL) and Costas loops for IQ carrier recovery
- Why synchronization is critical in practice
- Reading: Chapter 6

**📝 READING QUIZ 7** (10 points)
- Topic: Pulse Modulation and Digital Transmission
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 18 - Thursday, April 2
**ISI Mitigation, OFDM & Spread Spectrum Introduction**
- Causes of ISI in practical channels
- Equalization concepts: why equalizers are needed
- Introduction to OFDM as modern solution to frequency-selective fading
- OFDM basics: subcarriers, cyclic prefix, guard intervals
- Why WiFi and LTE use OFDM instead of complex equalizers
- Introduction to spread spectrum concepts
- Direct Sequence Spread Spectrum (DSSS) fundamentals
- Frequency Hopping Spread Spectrum (FHSS) overview
- Reading: Chapter 6

**Lab:** GNU Radio Lab 1 - RTL-SDR FM Reception & WiFi Spectrum Analysis

**Part 1: FM Broadcast Reception (30 min)**
- Introduction to GNU Radio Companion
- Connect and configure RTL-SDR (outputs IQ samples)
- Build FM broadcast receiver flowgraph:
  - RTL-SDR source block
  - Frequency xlating filter to select station
  - **Limiter block** (remove amplitude variations - Armstrong's contribution!)
  - WBFM Receive block for demodulation (mono FM, not full stereo/RDS)
  - Audio sink for output
- Visualize waterfall and spectrum displays
- Listen to demodulated audio

**Part 2: Understanding FM Demodulation (15 min)**
- Examine WBFM block internals (discriminator + de-emphasis)
- Discuss pre-emphasis/de-emphasis (75 μs time constant in US)
- Why limiter is critical: removes amplitude noise before FM demod
- Note: This is mono FM - stereo requires additional 19 kHz pilot tone processing

**Part 3: WiFi Spectrum Analysis (15 min)**
- Retune RTL-SDR to 2.4 GHz WiFi band
- Capture WiFi signals
- Identify 802.11g/n preambles and OFDM spectrum shape
- Compare OFDM spectrum (flat-topped, rectangular) to single-carrier FM (narrow, peaked)

---

**EASTER BREAK: April 3-6 (No Classes)**

---

### Week 10

#### Lesson 19 - Tuesday, April 7
**Spread Spectrum & CDMA**
- DSSS processing gain and bandwidth expansion
- PN sequences and autocorrelation properties
- CDMA (Code Division Multiple Access) fundamentals
- Walsh codes and orthogonality
- IQ spreading: separate codes for I and Q channels
- Applications: 3G cellular (CDMA2000, WCDMA), GPS
- WiFi 802.11b DSSS
- Jamming resistance and security benefits
- Reading: Supplemental materials

**Lab:** Python Lab 3 - CDMA & Spread Spectrum Simulation
- Generate and analyze PN sequences
- Simulate DSSS spreading and despreading
- Demonstrate processing gain against interference
- Multi-user CDMA with Walsh codes
- Compare CDMA to TDMA/FDMA

#### Lesson 20 - Thursday, April 9
**M-ary PSK, QAM & LTE/5G Modulation**
- Extension from binary to M-ary signaling
- QPSK (Quadrature Phase Shift Keying) - encoding 2 bits using IQ
- Offset QPSK (OQPSK)
- M-ary PSK constellations in IQ plane
- QAM (Quadrature Amplitude Modulation) - independent I and Q amplitude control
- Spectral efficiency vs. power efficiency tradeoff
- LTE and 5G modulation schemes: QPSK, 16-QAM, 64-QAM, 256-QAM
- Adaptive modulation based on channel quality
- Reading: Chapter 7.5-7.7

**Lab:** Python Lab 4 - QPSK/QAM Simulation & EVM Analysis
- Generate QPSK constellation
- Simulate QPSK modulation and demodulation
- Examine eye diagrams for I and Q channels
- Add AWGN and observe constellation spreading
- Calculate and visualize Error Vector Magnitude (EVM)
- Increase noise/distortion and watch EVM degrade
- Observe how degraded constellations lead to demodulation failures
- Optional: Analyze 64-QAM constellations from captured WiFi/LTE signals

**Additional Topics:**
- WiFi modulation: 802.11n/ac/ax (up to 1024-QAM in WiFi 6)
- Spectral efficiency comparison: WiFi vs. cellular
- Multiple access: OFDMA in WiFi 6 and LTE
- Error Vector Magnitude (EVM) fundamentals
- EVM as measure of modulation quality (magnitude + phase error)
- WiFi and 5G specifications using EVM requirements

**FT8: A Modern Weak-Signal Mode**
- FT8 as practical example of 8-FSK modulation
- Technical parameters: 50 Hz bandwidth, 15-second transmit cycles
- Weak-signal performance: operates reliably at -20 dB SNR
- Time synchronization requirements (GPS/NTP)
- Costas arrays for tone sequence generation
- Why Costas arrays: optimal autocorrelation allows multiple overlapping signals
- Forward error correction using LDPC codes (preview of Week 14)
- Why FT8 revolutionized HF amateur radio communications

**Lab Activity:** W3USR Digital Modes Demonstration
- Observe FT8 operation on HF (20m, 40m bands)
- Watch waterfall display showing 8-FSK tones
- Observe automatic decoding and time synchronization
- Listen to APRS on 2m (144.390 MHz)
- Demonstrate PSK31 and RTTY if time permits
- Show computer integration for digital mode decoding

**Homework 4 Assigned:** M-ary modulation, QAM, EVM, WiFi/cellular spectral efficiency problems

---

### Week 11

#### Lesson 21 - Tuesday, April 14
**EXAM 2: Modulation & Digital Systems**
- Coverage: Chapters 4-7
- Format: Closed book, equation sheet provided

#### Lesson 22 - Thursday, April 16
**Exam Review & Introduction to Probability**
- Exam 2 review and discussion
- Motivation for probability in communications
- Random experiments and sample spaces
- Probability axioms
- Reading: Chapter 8.1

**Homework 4 Due**

---

## Phase 4: Noise, Probability & System Performance (Weeks 12-15)

### Week 12

#### Lesson 23 - Tuesday, April 21
**Probability Fundamentals & Channel Capacity**
- Conditional probability
- Bayes' theorem
- Independent events
- Shannon's theorem and channel capacity
- Relationship between SNR, bandwidth, and capacity
- Fundamental limits of communication systems
- Reading: Chapter 8.1-8.2

**📝 READING QUIZ 8** (10 points)
- Topic: Probability and Random Variables
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 24 - Thursday, April 23
**Random Variables & Gaussian Distribution**
- Discrete and continuous random variables
- Probability Mass Functions (PMF)
- Probability Density Functions (PDF)
- Cumulative Distribution Functions (CDF)
- Expected value and variance
- Gaussian (Normal) distribution
- Q-function and error function
- Reading: Chapter 8.3-8.4

---

### Week 13

#### Lesson 25 - Tuesday, April 28
**Noise Fundamentals**
- Thermal noise fundamentals
- Noise power spectral density
- Additive White Gaussian Noise (AWGN)
- Noise figure and noise temperature
- Reading: Chapter 9

**📝 READING QUIZ 9** (10 points)
- Topic: Noise in Communication Systems
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 26 - Thursday, April 30
**Noise in Analog Systems**
- SNR calculations for AM systems
- Noise performance of DSB-SC and SSB
- FM noise performance and threshold effect
- FM improvement over AM
- Reading: Chapter 11.1-11.3

**Lab:** GNU Radio Lab 2 - Noise and SNR Analysis
- Add AWGN to AM and FM signals
- Measure SNR using spectrum analyzer blocks
- Compare noise performance of AM vs. FM
- Observe FM threshold effect

**Homework 5 Assigned:** Probability, noise, and SNR calculations

---

### Week 14

#### Lesson 27 - Tuesday, May 5
**Digital Performance Analysis**
- Bit Error Rate (BER) fundamentals
- Matched filtering
- Signal space and correlation receivers
- Decision regions
- Reading: Chapter 10

**📝 READING QUIZ 10** (10 points)
- Topic: Digital Performance and BER
- 10 questions randomly selected from 50-question bank
- Administered via Brightspace at beginning of class

#### Lesson 28 - Thursday, May 7
**BER, EVM & Channel Coding**
- BER for BPSK
- BER for FSK (coherent and non-coherent)
- BER for QAM
- Performance comparison of modulation schemes
- EVM vs. BER: complementary metrics
- Why modern systems (WiFi/5G) specify EVM limits
- Channel coding fundamentals: block codes, convolutional codes
- Modern codes: LDPC (WiFi), Turbo (LTE), Polar (5G)
- Why channel coding is essential in modern systems
- Reading: Chapter 10

**Lab:** Python Lab 5 - BER Performance Simulation
- Simulate BPSK, QPSK, and QAM in AWGN
- Generate BER vs. SNR curves
- Compare theoretical and simulated performance
- Explore effect of matched filtering

**Homework 5 Due / Homework 6 Assigned:** BER calculations, link budgets, WiFi/cellular system analysis

---

### Week 15

#### Lesson 29 - Tuesday, May 12
**Link Budgets, WiFi, Cellular & SDR Concepts**
- Link budget calculations (Friis equation)
- Path loss at different frequencies: WiFi (2.4/5 GHz) vs. cellular (900 MHz) vs. 5G mmWave (28 GHz)
- Antenna gains, system noise temperature
- Margin analysis for WiFi and cellular systems
- Software-Defined Radio (SDR) architecture
- Modern communication systems overview:
  - WiFi standards evolution (802.11a/g/n/ac/ax/be)
  - LTE and 5G NR architecture basics
  - MIMO and beamforming in WiFi 6 and 5G
  - Frequency bands and channel bandwidths
- Reading: Chapter 11.4-11.7

**Lab Activity:** W3USR Satellite Communications
- Predict satellite pass using tracking software
- Configure azimuth/elevation rotator for satellite tracking
- Demonstrate FM voice satellite contact (if satellite available)
- Or: demonstrate digital satellite telemetry reception

#### Lesson 30 - Thursday, May 14
**HAMVENTION - NO CLASS**
- Instructor attending Hamvention (Dayton Hamvention, the world's largest amateur radio convention)
- **Self-study assignment:** Review comprehensive course material
- Watch recorded lecture on modern wireless systems (WiFi 6, 5G NR, SDR concepts)
- Optional: Explore GNU Radio tutorials or advanced modulation projects
- Prepare questions for final exam review session

**Homework 6 Due** (submit electronically)

---

## Final Exam Period

### Final Exam - Thursday, May 21, 12:45–2:45 PM
**Comprehensive Final Exam**
- Coverage: All course material (Chapters 1-11)
- Emphasis on noise, probability, and system performance (Chapters 8-11)
- Format: Closed book, equation sheet provided

---

*Last updated: January 2026*
