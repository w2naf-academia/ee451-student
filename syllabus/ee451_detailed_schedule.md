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
| 18 | Thu, Apr 9 | Noise in Communications Systems | Chapter 9 |
| 22 | Thu, Apr 23 | Probability and Random Variables | Chapter 8.1-8.2 |
| 25 | Tue, May 5 | Random Variables, Noise in Analog Communications | Chapter 8.3-8.4, 9 |
| 27 | Tue, May 12 | Digital Performance, BER, System Noise Calculations | Chapter 10, 11.1-11.3 |

---

## Homework Schedule

| Assignment | Assigned | Due | Topics |
|------------|----------|-----|--------|
| Homework 1 | Thu, Jan 29 | Thu, Feb 5 | Complex numbers, phasors, signals |
| Homework 2 | Thu, Feb 12 | Thu, Feb 19 | AM and ASK |
| Homework 3 | Thu, Mar 5 | Tue, Mar 24 | FM, PM, FSK, BPSK |
| Homework 4 | Thu, Apr 16 | Thu, Apr 23 | M-ary modulation, QAM, EVM |
| Homework 5 | Thu, Apr 23 | Thu, May 7 | Probability, noise, SNR |

---

## Exam Schedule

| Exam | Date | Coverage |
|------|------|----------|
| Exam 1 | Thu, Feb 26 | Chapters 2-3, 7.1-7.2 (Fourier Analysis & AM) |
| Exam 2 | Tue, Apr 21 | Chapters 4-7, 9, 11 (Modulation, Noise & Link Budgets) |
| Final Exam | Thu, May 21 | Comprehensive (emphasis on Chapters 8-11) |

---

## Lab Schedule

### Python/Jupyter Labs

| Lab | Week | Date | Topic |
|-----|------|------|-------|
| Python Lab 1 | 2 | Thu, Feb 5 | Fourier Analysis and Spectral Visualization |
| Python Lab 2 | 4 | Thu, Feb 19 | AM/ASK Modulation and Envelope Detection |
| Python Lab 3 | 11 | Tue, Apr 14 | CDMA & Spread Spectrum Simulation |
| Python Lab 4 | 11 | Thu, Apr 16 | QPSK/QAM Simulation with EVM Analysis |
| Python Lab 5 | 15 | Tue, May 12 | BER Performance Simulation |

### GNU Radio Labs

| Lab | Week | Date | Topic |
|-----|------|------|-------|
| GNU Radio Lab 1 | 10 | Thu, Apr 9 | FM Broadcast Reception & WiFi Spectrum Analysis |
| GNU Radio Lab 2 | 14 | Tue, May 5 | Noise Analysis and SNR Measurement |

### Baba Yaga's Hut Phasor Labs

| Session | Week | Date | Topic |
|---------|------|------|-------|
| Part 1 | 8 | Thu, Mar 26 | AM Phasor Analysis with I/Q Demodulation |
| Part 2 | 9 | Tue, Mar 31 | DSB-SC, FM, and PM Phasor Analysis |

### W3USR Amateur Radio Station Activities

| Activity | Week | Date | Topic |
|----------|------|------|-------|
| W3USR Activity 1 | 4 | Thu, Feb 19 | HF Station Tour and SSB/AM Reception |
| W3USR Activity 2 | 11 | Thu, Apr 16 | Digital Modes (FT8, APRS, PSK31) |

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

**Homework 2 Assigned:** AM and ASK problems

---

### Week 4

#### Lesson 6 - Tuesday, February 17
**Binary Amplitude Shift Keying (ASK)**
- On-Off Keying (OOK)
- Binary ASK as discrete version of AM
- Spectral characteristics of ASK
- ASK demodulation (coherent and envelope detection)
- Superheterodyne receiver and image frequency problem
- Comparison of analog AM and digital ASK
- Reading: Chapter 7.1-7.2, Chapter 3.6-3.8 (in preparation for Reading Quiz 3 in Lesson 7)

#### Lesson 7 - Thursday, February 19
**SSB Introduction, Python Lab 2, & W3USR Activity 1**
- SSB motivation: bandwidth and power efficiency vs. DSB
- SSB key formulas (USB, LSB, Hilbert transform overview)
- Bandwidth/power comparison: AM vs. DSB-SC vs. SSB
- Full SSB treatment (derivation, generation methods, VSB, demodulation) continues in Lesson 8

**📝 READING QUIZ 3**
- Topic: SSB, VSB, Receiver Architectures, ASK/OOK
- Reading: Chapter 3.6-3.8, 7.1-7.2
- Administered via Brightspace at beginning of class

**Lab:** Python Lab 2 - AM/ASK Modulation
- DSB-SC modulation and coherent demodulation
- Full carrier AM and envelope detection
- OOK modulation and threshold detection
- Spectral analysis: AM vs. ASK spectra comparison

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
**FSK Demodulation & Applications**
- Coherent FSK detection (matched filters / correlators)
- Non-coherent FSK detection (envelope detection)
- Frequency discriminator for FM/FSK demodulation
- Phase-Locked Loop (PLL) for FM demodulation
- BER comparison: coherent vs non-coherent FSK vs BPSK
- Practical applications: Bell 103 modem, Caller ID, APRS, Bluetooth GFSK
- Reading: Chapter 4.6-4.8, 7.3-7.4 (in preparation for Reading Quiz 5 in Lesson 13)

#### Lesson 13 - Thursday, March 12
**BPSK Theory & Demodulation Essentials**
- Binary Phase Shift Keying fundamentals
- BPSK signal generation and constellation
- Coherent BPSK detection (correlation receiver, Costas loop overview)
- Why BPSK cannot use envelope detection (phase information requires coherent reference)
- BER performance of BPSK
- Spectral efficiency comparison: ASK vs FSK vs BPSK

**📝 READING QUIZ 5**
- Topic: FM Generation/Demodulation, FSK/BPSK
- Reading: Chapter 4.6-4.8, 7.3-7.4
- Administered via Brightspace at beginning of class

---

**SPRING BREAK: March 14-22 (No Classes)**

---

### Week 8

#### Lesson 14 - Tuesday, March 24
**Homework 3 Review & Baba Yaga Introduction**
- Return and review Homework 3 solutions (~45 min)
  - Common mistakes and key takeaways
  - FM/PM problems, Carson's rule, FSK/MSK, BPSK
- Introduction to Baba Yaga's Hut phasor lab (~25 min)
  - Lab objectives and equipment overview
  - I/Q demodulator concept and setup
  - Safety briefing and pair assignments
  - Reference: w8edu_cwru/the-hut-on-phasors-legs.pdf

**Homework 3 Due**

#### Lesson 15 - Thursday, March 26
**"Baba Yaga's Hut" - Phasor Analysis Lab (Part 1 of 2)**
- Full 75-minute lab session
- Build I/Q demodulator using function generators and oscilloscopes
- Examine AM signals in time, frequency, and phasor domains simultaneously
- Vary modulation depth and observe effects in all three representations
- Couple to AM radio for audio demodulation
- Students work in pairs on the one shared setup
- Reference: w8edu_cwru/the-hut-on-phasors-legs.pdf

---

## Phase 3: Noise, ISI & Advanced Digital (Weeks 9-11)

### Week 9

#### Lesson 16 - Tuesday, March 31
**"Baba Yaga's Hut" - Phasor Analysis Lab (Part 2 of 2)**
- Full 75-minute lab session
- Examine DSB-SC (suppressed carrier) signals
- Explore FM and PM in phasor representation
- Vary carrier phase and observe rotation in phasor domain
- Complete lab worksheets and analysis
- Students work in pairs on the one shared setup
- Reading: Chapter 9 (in preparation for Reading Quiz 6 in Lesson 18)

#### Thursday, April 2 - NO CLASS (Holy Thursday)

---

**EASTER BREAK: April 3-6 (No Classes)**

---

### Week 10

#### Lesson 17 - Tuesday, April 7
**Noise Fundamentals & SNR**
- Thermal noise generation and statistical properties
- White noise and Additive White Gaussian Noise (AWGN) channel model
- Noise power spectral density: N₀/2
- Signal-to-noise ratio (SNR) definition and calculation
- Noise figure and noise temperature
- Cascaded noise figure (Friis formula)
- System noise temperature and receiver design implications
- Reading: Chapter 9

#### Lesson 18 - Thursday, April 9
**Link Budgets, ISI & Eye Diagrams + GNU Radio Lab**

**Part A: Link Budgets & ISI Overview (~30 min)**
- Friis transmission equation and free-space path loss
- EIRP, received power, and link margin
- Complete link budget example (satellite or point-to-point)
- Intersymbol Interference (ISI) overview: causes, eye diagrams, raised cosine filtering

**📝 READING QUIZ 6**
- Topic: Noise in Communications Systems
- Reading: Chapter 9
- Administered via Brightspace at beginning of class

**Part B: GNU Radio Lab 1 - RTL-SDR FM Reception & WiFi Spectrum Analysis (~40 min)**

**Lab Activity 1: FM Broadcast Reception (20 min)**
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

**Lab Activity 2: Understanding FM Demodulation (10 min)**
- Examine WBFM block internals (discriminator + de-emphasis)
- Discuss pre-emphasis/de-emphasis (75 μs time constant in US)
- Why limiter is critical: removes amplitude noise before FM demod

**Lab Activity 3: WiFi Spectrum Analysis (10 min)**
- Retune RTL-SDR to 2.4 GHz WiFi band
- Capture WiFi signals and identify OFDM spectrum shape
- Compare OFDM spectrum (flat-topped, rectangular) to single-carrier FM (narrow, peaked)

---

### Week 11

#### Lesson 19 - Tuesday, April 14
**OFDM, Spread Spectrum & CDMA**
- OFDM fundamentals: subcarrier orthogonality, FFT/IFFT, cyclic prefix
- WiFi 802.11a/g OFDM parameters (64 subcarriers, 312.5 kHz spacing, 4 μs symbol)
- OFDM advantages (multipath robust, adaptive modulation) and disadvantages (PAPR)
- Direct Sequence Spread Spectrum (DSSS): processing gain, interference rejection
- Frequency Hopping Spread Spectrum (FHSS) overview (Bluetooth: 79 channels, 1600 hops/sec)
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

## Phase 4: Exams, Probability & System Performance (Weeks 12-15)

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
**Probability Fundamentals & Channel Capacity**
- Conditional probability review: P(A|B) = P(A ∩ B) / P(B)
- Bayes' theorem and Maximum A Posteriori (MAP) detection
- Worked examples: binary detection, MAP symbol decision

**Shannon's Channel Capacity Theorem**
- Channel capacity definition: maximum reliable data rate
- Shannon-Hartley theorem: C = B log₂(1 + SNR) bits/sec
- Spectral efficiency limit: η_max = log₂(1 + SNR) bits/s/Hz
- Bandwidth vs. SNR trade-offs
- Worked examples: WiFi and LTE capacity calculations

**Channel Coding Introduction**
- Why channel coding: add redundancy for error correction
- Simple example: repetition code (rate 1/3)
- Modern codes: LDPC, Turbo, Polar (approaching Shannon limit)
- Practical system design trade-off example

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
- SNR calculations for AM and FM systems

**📝 READING QUIZ 8**
- Topic: Random Variables, Noise in Analog Communications
- Reading: Chapter 8.3-8.4, 9
- Administered via Brightspace at beginning of class

**Lab:** GNU Radio Lab 2 - Noise and SNR Analysis
- Add AWGN to AM and FM signals
- Measure SNR using spectrum analyzer blocks
- Compare noise performance of AM vs. FM
- Observe FM threshold effect

#### Lesson 26 - Thursday, May 7
**Data Communication Systems: Sampling & Quantization**
- Sampling theorem, Nyquist rate, aliasing
- Quantization noise and SQNR
- Pulse Code Modulation (PCM)
- Companding (μ-law and A-law)
- Delta modulation and adaptive delta modulation
- Reading: Chapter 10 (in preparation for Reading Quiz 9 in Lesson 27)

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

*Last updated: March 8, 2026*
