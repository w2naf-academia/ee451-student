# EE 451: Communications Systems
## Detailed Lesson-by-Lesson Schedule - Spring 2026

**Class Meeting Times:** Tuesday & Thursday, 2:30 PM - 3:45 PM, Loyola Science Center Room 142<br>
**Textbook:** An Introduction to Analog and Digital Communications (2nd Ed.), Haykin & Moher

---

## Reading Quiz Schedule

Reading quizzes administered through Brightspace at the beginning of selected classes:

| Lesson | Date | Topic | Reading |
|--------|------|-------|---------|
| 2 | Tue, Feb 3 | Fourier Transform, FT Properties, Dirac Delta, Periodic Signals | Chapter 2.1-2.5 |
| 4 | Tue, Feb 10 | Amplitude Modulation Techniques | Chapter 3.1-3.3 |
| 7 | Thu, Feb 19 | SSB, VSB, Receiver Architectures, ASK/OOK | Chapter 3.6-3.8, 7.1-7.2 |
| 11 | Thu, Mar 5 | FM/PM Theory and Modulation | Chapter 4.1-4.5 |
| 13 | Thu, Mar 12 | FM Generation/Demodulation, FSK/BPSK | Chapter 4.6-4.8, 7.3-7.4 |
| 17 | Tue, Apr 7 | Pulse Modulation and Baseband Digital Transmission | Chapter 5, 6 |
| 22 | Thu, Apr 23 | Probability and Random Variables | Chapter 8.1-8.2 |
| 25 | Tue, May 5 | Random Variables, Noise in Analog Communications | Chapter 8.3-8.4, 9 |
| 27 | Tue, May 12 | Digital Performance, BER, System Noise Calculations | Chapter 10, 11.1-11.3 |

---

## Homework Schedule

| Assignment | Assigned | Due | Topics |
|------------|----------|-----|--------|
| Homework 1 | Thu, Jan 29 | Thu, Feb 5 | Complex numbers, phasors, signals |
| Homework 2 | Thu, Feb 12 | Thu, Feb 19 | AM and ASK |
| Homework 3 | Thu, Mar 5 | Thu, Mar 12 | FM, PM, FSK, BPSK |
| Homework 4 | Thu, Apr 16 | Thu, Apr 23 | M-ary modulation, QAM, EVM |
| Homework 5 | Thu, Apr 23 | Thu, May 7 | Probability, noise, SNR |

---

## Exam Schedule

| Exam | Date | Coverage |
|------|------|----------|
| Exam 1 | Thu, Feb 26 | Chapters 2-3, 7.1-7.2 (Fourier Analysis & AM) |
| Exam 2 | Tue, Apr 21 | Chapters 4-7 (Modulation & Digital Systems) |
| Final Exam | Thu, May 21 | Comprehensive (emphasis on Chapters 8-11) |

---

## Lab Schedule

### Python/Jupyter Labs

| Lab | Week | Date | Topic |
|-----|------|------|-------|
| Python Lab 1 | 2 | Thu, Feb 5 | Fourier Analysis and Spectral Visualization |
| Python Lab 2 | 3 | Thu, Feb 12 | AM/ASK Modulation and Envelope Detection |
| Python Lab 3 | 11 | Tue, Apr 14 | CDMA & Spread Spectrum Simulation |
| Python Lab 4 | 11 | Thu, Apr 16 | QPSK/QAM Simulation with EVM Analysis |
| Python Lab 5 | 15 | Tue, May 12 | BER Performance Simulation |

### GNU Radio Labs

| Lab | Week | Date | Topic |
|-----|------|------|-------|
| GNU Radio Lab 1 | 10 | Thu, Apr 9 | FM Broadcast Reception & WiFi Spectrum Analysis |
| GNU Radio Lab 2 | 14 | Thu, May 7 | Noise Analysis and SNR Measurement |

### Baba Yaga's Hut Phasor Labs

| Session | Week | Date | Topic |
|---------|------|------|-------|
| Part 1 | 8 | Tue, Mar 24 | AM Phasor Analysis with I/Q Demodulation |
| Part 2 | 9 | Tue, Mar 31 | DSB-SC, FM, and PM Phasor Analysis |

### W3USR Amateur Radio Station Activities

| Activity | Week | Date | Topic |
|----------|------|------|-------|
| W3USR Activity 1 | 4 | Thu, Feb 19 | HF Station Tour and SSB/AM Reception |
| W3USR Activity 2 | 13 | Tue, Apr 28 | Digital Modes (FT8, APRS, PSK31) |

**Optional Extra Credit:** W3USR Satellite Communications activity available by arrangement (contact instructor)

---

## Phase 1: Foundation (Weeks 1-2)

### Week 1

#### Lesson 1 - Thursday, January 29
**Course Introduction & Complex Signal Review**
- Course overview, syllabus, grading policy, amateur radio extra credit opportunities
- Introduction to W3USR amateur radio station capabilities
- Cross-disciplinary applications: radar, sonar, audio processing, biomedical
- Complex numbers and Euler's formula review
- Sinusoids: amplitude, frequency, phase
- Reading: Chapter 1, Chapter 2.1-2.5 (in preparation for Reading Quiz 1 in Lesson 2)

**Assignment:** Install Python/Jupyter environment before next class (see environment.yml)

**Homework 1 Assigned:** Complex numbers, phasors, basic signal operations

---

### Week 2

#### Lesson 2 - Tuesday, February 3
**Signal Analysis Fundamentals & I/Q Representation**
- I/Q (In-phase/Quadrature) representation - industry-critical terminology
- Convolution, unit step and impulse functions
- Energy and power signals
- Phasor representation of sinusoids
- Introduction to analytic signals

**📝 READING QUIZ 1**
- Topic: Fourier Transform, FT Properties, Dirac Delta, Periodic Signals
- Reading: Chapter 2.1-2.5
- Administered via Brightspace at beginning of class

**Note:** Correlation, a related operation to convolution, will be introduced in Lesson 4 after we study Fourier transforms. Correlation is essential for matched filtering and signal detection in communication systems.

#### Lesson 3 - Thursday, February 5
**Fourier Analysis Essentials**
- Fourier series and Fourier transforms
- Properties of Fourier transforms
- Time-frequency duality
- Bandwidth concepts
- Reading: Chapter 3.1-3.3 (in preparation for Reading Quiz 2 in Lesson 4)

**Lab:** Python Lab 1 - Fourier Analysis
- Generate and plot sinusoids
- Compute and visualize Fourier transforms
- Explore time-frequency duality
- Bandwidth calculations

**Homework 1 Due**

---

## Phase 2: Modulation Techniques - Integrated Analog & Digital (Weeks 3-8)

### Week 3

#### Lesson 4 - Tuesday, February 10
**Fourier Analysis Applications & Amplitude Modulation Introduction**
- Spectral analysis of common signals
- Parseval's theorem and energy spectral density
- Introduction to correlation
- Need for modulation - why we modulate signals

**📝 READING QUIZ 2**
- Topic: Amplitude Modulation Techniques
- Reading: Chapter 3.1-3.3
- Administered via Brightspace at beginning of class

#### Lesson 5 - Thursday, February 12
**Amplitude Modulation Theory**
- DSB-SC (Double Sideband Suppressed Carrier) theory
- Full carrier AM
- Envelope detection
- Modulation index and overmodulation

**Lab:** Python Lab 2 - AM/ASK Modulation
- Simulate AM signals with varying modulation depths
- Implement envelope detection
- Compare AM spectra at different modulation indices

**Homework 2 Assigned:** AM and ASK problems

---

### Week 4

#### Lesson 6 - Tuesday, February 17
**Binary Amplitude Shift Keying (ASK)**
- On-Off Keying (OOK)
- Binary ASK as discrete version of AM
- Spectral characteristics of ASK
- Comparison of analog AM and digital ASK
- Reading: Chapter 7.1-7.2, Chapter 3.6-3.8 (in preparation for Reading Quiz 3 in Lesson 7)

#### Lesson 7 - Thursday, February 19
**AM Systems & SSB**
- Single Sideband (SSB) modulation
- Hilbert transform
- SSB generation (filter method, phasing method)
- Vestigial Sideband (VSB) - brief overview

**📝 READING QUIZ 3**
- Topic: SSB, VSB, Receiver Architectures, ASK/OOK
- Reading: Chapter 3.6-3.8, 7.1-7.2
- Administered via Brightspace at beginning of class

**Lab Activity:** W3USR Station Tour & HF Listening
- Tour of W3USR amateur radio station
- Listen to SSB voice communications on HF bands (20m, 40m)
- Identify AM broadcast signals on 80m band
- Demonstrate different receiver modes (AM, SSB, CW)

**Homework 2 Due**

---

### Week 5

#### Lesson 8 - Tuesday, February 24
**Receiver Architectures**
- Superheterodyne receiver design
- Mixer theory and image frequencies
- Direct conversion receivers (produce I/Q baseband)
- Direct sampling receivers (modern high-speed ADC approach)
- Comparison: superheterodyne vs direct conversion vs direct sampling
- Automatic Gain Control (AGC)

#### Lesson 9 - Thursday, February 26
**EXAM 1: Fourier Analysis & Amplitude Modulation**
- Coverage: Chapters 2-3, 7.1-7.2
- Format: Closed book, equation sheet provided

---

### Week 6

#### Lesson 10 - Tuesday, March 3
**Exam Review & Angle Modulation Introduction**
- Exam 1 review and discussion
- Introduction to frequency and phase modulation
- Narrowband vs. wideband FM
- Reading: Chapter 4.1-4.5 (in preparation for Reading Quiz 4 in Lesson 11)

#### Lesson 11 - Thursday, March 5
**FM/PM Theory & Binary FSK**
- FM/PM mathematical representation
- Frequency deviation and modulation index
- Narrowband FM approximation
- Wideband FM characteristics

**📝 READING QUIZ 4**
- Topic: FM/PM Theory and Modulation
- Reading: Chapter 4.1-4.5
- Administered via Brightspace at beginning of class

**Homework 3 Assigned:** FM, PM, FSK, BPSK problems

---

### Week 7

#### Lesson 12 - Tuesday, March 10
**Binary FSK & MSK**
- Binary Frequency Shift Keying (FSK)
- Continuous Phase FSK (CPFSK)
- Minimum Shift Keying (MSK)
- FSK as digital counterpart to FM
- Comparison of FSK bandwidth to FM (Carson's rule application)
- Reading: Chapter 7.3-7.4, Chapter 4.6-4.8 (in preparation for Reading Quiz 5 in Lesson 13)

#### Lesson 13 - Thursday, March 12
**FM Generation & Demodulation**
- Direct FM generation (VCO)
- Indirect FM generation (Armstrong method)
- Frequency discriminators
- PLL-based FM demodulation (operates on IQ baseband)

**📝 READING QUIZ 5**
- Topic: FM Generation/Demodulation, FSK/BPSK
- Reading: Chapter 4.6-4.8, 7.3-7.4
- Administered via Brightspace at beginning of class

**Homework 3 Due**

---

**SPRING BREAK: March 14-22 (No Classes)**

---

### Week 8

#### Lesson 14 - Tuesday, March 24
**Binary PSK & Carson's Rule**
- Binary Phase Shift Keying (BPSK) fundamentals
- BPSK as phase modulation of IQ carrier
- Coherent detection of BPSK (requires IQ demodulation)
- Carson's rule for FM bandwidth
- Pre-emphasis and de-emphasis in FM

**Lab Activity:** **"Baba Yaga's Hut" - Phasor Analysis Lab (Part 1 of 2)**
- Build I/Q demodulator using function generators and oscilloscopes
- Examine AM signals in time, frequency, and phasor domains simultaneously
- Vary modulation depth and observe effects in all three representations
- Couple to AM radio for audio demodulation
- Students work in pairs on the one shared setup
- Reference: w8edu_cwru/the-hut-on-phasors-legs.pdf

#### Lesson 15 - Thursday, March 26
**Pulse Modulation & Sampling Theorem**
- Sampling theorem and Nyquist rate
  - **Real sampling:** 2× bandwidth (traditional approach)
  - **IQ (complex) sampling:** 1× bandwidth (what SDRs like RTL-SDR use)
  - Why the difference: IQ sampling separates positive and negative frequencies
- Aliasing and anti-aliasing filters
- Pulse Amplitude Modulation (PAM)
- Natural and flat-top sampling
- Reading: Chapter 5 (part 1 of reading for Reading Quiz 6 in Lesson 17; see also Chapter 6 in Lesson 16)

---

## Phase 3: Advanced Digital Communications (Weeks 9-11)

### Week 9

#### Lesson 16 - Tuesday, March 31
**PCM & Delta Modulation**
- Quantization and quantization noise
- Pulse Code Modulation (PCM)
- Companding (μ-law and A-law)
- Delta modulation and adaptive delta modulation
- Line codes (NRZ, RZ, Manchester, etc.)
- Reading: Chapter 6 (part 2 of reading for Reading Quiz 6 in Lesson 17; see also Chapter 5 in Lesson 15)

**Lab:** **"Baba Yaga's Hut" - Phasor Analysis Lab (Part 2 of 2)**
- Examine DSB-SC (suppressed carrier) signals
- Explore FM and PM in phasor representation
- Vary carrier phase and observe rotation in phasor domain
- Complete lab worksheets and analysis
- Students work in pairs on the one shared setup

#### Thursday, April 2 - NO CLASS (Holy Thursday)

---

**EASTER BREAK: April 3-6 (No Classes)**

---

### Week 10

#### Lesson 17 - Tuesday, April 7
**Baseband Digital Transmission & Synchronization**
- Intersymbol Interference (ISI): causes and effects
- Eye diagrams: open vs. closed, noise margin, timing margin, jitter
- Nyquist criterion for zero-ISI pulse shaping
- Raised cosine filtering (roll-off factor α, bandwidth tradeoff)
- Multipath propagation and OFDM preview (WiFi, LTE)
- Carrier and symbol timing synchronization
- Phase-Locked Loop (PLL) and Costas loop for carrier recovery
- Timing recovery methods: early-late gate, Gardner algorithm
- Python example: eye diagram generation with raised cosine filter
- Reading: Chapter 5, 6

**📝 READING QUIZ 6**
- Topic: Pulse Modulation and Baseband Digital Transmission
- Reading: Chapter 5, 6
- Administered via Brightspace at beginning of class

#### Lesson 18 - Thursday, April 9
**ISI Mitigation, OFDM & Spread Spectrum Introduction**
- OFDM fundamentals: divide wideband channel into narrowband subcarriers
- Subcarrier orthogonality and FFT/IFFT implementation
- Cyclic prefix: absorbs multipath delay, converts to circular convolution
- WiFi 802.11a/g OFDM parameters (64 subcarriers, 312.5 kHz spacing, 4 μs symbol)
- OFDM advantages (multipath robust, adaptive modulation) and disadvantages (PAPR)
- Direct Sequence Spread Spectrum (DSSS) introduction
- Processing gain: spread BW / data BW (GPS example: 43 dB)
- Frequency Hopping Spread Spectrum (FHSS) overview (Bluetooth: 79 channels, 1600 hops/sec)
- Applications: WiFi 802.11b (DSSS), GPS (DSSS), Bluetooth (FHSS), military
- Reading: Chapter 6, Supplemental materials

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

### Week 11

#### Lesson 19 - Tuesday, April 14
**Spread Spectrum & CDMA**
- Deep dive into DSSS processing gain and interference rejection
- PN sequences: m-sequences, Gold codes, autocorrelation properties
- CDMA (Code Division Multiple Access) fundamentals
- Walsh codes and orthogonality
- IQ spreading: separate codes for I and Q channels
- Multi-user CDMA: near-far problem, power control
- Applications: 3G cellular (CDMA2000, WCDMA), GPS
- Comparison: CDMA vs. TDMA vs. FDMA
- Reading: Supplemental materials

**Lab:** Python Lab 3 - CDMA & Spread Spectrum Simulation
- Generate and analyze PN sequences
- Simulate DSSS spreading and despreading
- Demonstrate processing gain against interference
- Multi-user CDMA with Walsh codes
- Compare CDMA to TDMA/FDMA

#### Lesson 20 - Thursday, April 16
**M-ary Modulation, QAM, FT8 & W3USR Digital Modes**
- Extension from binary to M-ary signaling (log₂(M) bits/symbol)
- QPSK: 4 phase states, 2 bits/symbol, Gray coding
- Offset QPSK (OQPSK) for satellite links
- Higher-order PSK: 8-PSK, 16-PSK limitations
- QAM (Quadrature Amplitude Modulation): vary amplitude and phase
- 16-QAM, 64-QAM, 256-QAM constellations
- Spectral efficiency comparison: BPSK through 256-QAM
- WiFi and LTE adaptive modulation (MCS index)
- Error Vector Magnitude (EVM): modulation quality metric
- EVM specifications: WiFi, LTE, 5G NR requirements
- FT8: 8-FSK weak-signal mode, Costas arrays, LDPC coding
- Reading: Chapter 7.5-7.7, Supplemental FT8 materials

**Lab Activity:** W3USR Activity 2 - Digital Modes Demonstration
- Observe FT8 operation on HF (20m, 14.074 MHz) using WSJT-X
- Identify Costas array tones on waterfall display
- Observe SNR reports (negative dB values common)
- APRS on 2m VHF (144.390 MHz): 1200 bps AFSK packets
- Decode position reports, weather data, messages

**Lab:** Python Lab 4 - QPSK/QAM Simulation & EVM Analysis
- Generate QPSK and QAM constellations
- Simulate modulation and demodulation
- Add AWGN and observe constellation spreading
- Calculate and visualize Error Vector Magnitude (EVM)

**Homework 4 Assigned:** M-ary modulation, QAM, EVM, spectral efficiency (due Lesson 22)

---

## Phase 4: Noise, Probability & System Performance (Weeks 12-15)

### Week 12

#### Lesson 21 - Tuesday, April 21
**EXAM 2: Modulation & Digital Systems**
- Coverage: Chapters 4-7, 9 (Lessons 10-20)
- Topics: FM/PM, FSK, BPSK, noise fundamentals, ISI, OFDM, spread spectrum, QAM, EVM
- Format: Closed book, equation sheet provided
- Duration: 75 minutes, 100 points

#### Lesson 22 - Thursday, April 23
**Exam Review & Introduction to Probability**
- Exam 2 review and discussion
- Common errors and corrections
- Motivation for probability in communications
- Random experiments and sample spaces
- Probability axioms
- Conditional probability and Bayes' theorem
- Independent events
- Reading: Chapter 8.1-8.2

**📝 READING QUIZ 7**
- Topic: Probability and Random Variables
- Reading: Chapter 8.1-8.2
- Administered via Brightspace at beginning of class

**Homework 4 Due**

**Homework 5 Assigned:** Probability, noise, and SNR (due Lesson 26)

---

### Week 13

#### Lesson 23 - Tuesday, April 28
**FT8 & Modern Digital Modes**
- Carrier and symbol timing synchronization concepts
- Phase-locked loops (PLL) and Costas loops for IQ carrier recovery
- Why synchronization is critical in practice

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

#### Lesson 24 - Thursday, April 30
**Random Variables & Gaussian Distribution**
- Discrete and continuous random variables
- Probability Mass Functions (PMF)
- Probability Density Functions (PDF)
- Cumulative Distribution Functions (CDF)
- Expected value and variance
- Gaussian (Normal) distribution
- Q-function and error function
- Reading: Chapter 8.3-8.4, Chapter 9 (in preparation for Reading Quiz 8 in Lesson 25)

---

### Week 14

#### Lesson 25 - Tuesday, May 5
**Noise Fundamentals**
- Thermal noise fundamentals
- Noise power spectral density
- Additive White Gaussian Noise (AWGN)
- Noise figure and noise temperature

**📝 READING QUIZ 8**
- Topic: Random Variables, Noise in Analog Communications
- Reading: Chapter 8.3-8.4, 9
- Administered via Brightspace at beginning of class

#### Lesson 26 - Thursday, May 7
**Noise in Analog Systems**
- SNR calculations for AM systems
- Noise performance of DSB-SC and SSB
- FM noise performance and threshold effect
- FM improvement over AM
- Reading: Chapter 11.1-11.3, Chapter 10 (in preparation for Reading Quiz 9 in Lesson 27)

**Lab:** GNU Radio Lab 2 - Noise and SNR Analysis
- Add AWGN to AM and FM signals
- Measure SNR using spectrum analyzer blocks
- Compare noise performance of AM vs. FM
- Observe FM threshold effect

**Homework 5 Due**

---

### Week 15

#### Lesson 27 - Tuesday, May 12 (LAST CLASS)
**Digital Performance, Channel Coding & Course Review**
- Bit Error Rate (BER) fundamentals
- BER for BPSK, FSK, and QAM
- Performance comparison of modulation schemes
- Matched filtering and signal space concepts
- Channel coding overview: LDPC (WiFi), Turbo (LTE), Polar (5G)
- EVM vs. BER: complementary metrics
- Course review and final exam preparation
- Q&A session

**📝 READING QUIZ 9**
- Topic: Digital Performance, BER, System Noise Calculations
- Reading: Chapter 10, 11.1-11.3
- Administered via Brightspace at beginning of class

**Lab:** Python Lab 5 - BER Performance Simulation
- Simulate BPSK, QPSK, and QAM in AWGN
- Generate BER vs. SNR curves
- Compare theoretical and simulated performance

*Note: No class Thursday, May 14 (Hamvention) or Tuesday, May 19 (finals week). Final exam is Thursday, May 21.*

---

## Final Exam Period

### Final Exam - Thursday, May 21, 12:45–2:45 PM
**Comprehensive Final Exam**
- Coverage: All course material (Chapters 1-11)
- Emphasis on noise, probability, and system performance (Chapters 8-11)
- Format: Closed book, equation sheet provided

---

*Last updated: January 31, 2026*
