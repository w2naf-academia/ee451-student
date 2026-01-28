# Communications Systems

**EE 451 • Section 1 • CRN 31101**

**Spring 2026 • TR 2:30–3:45 PM (3 Credits) • Loyola Science Center Room 142**

---

**The University of Scranton**
Department of Physics and Engineering

**Dr. Nathaniel A. Frissell**<br>
174 Loyola Science Center<br>
(570) 941-7003<br>
nathaniel.frissell@scranton.edu<br>
Office Hours: W 9-10 AM, 11 AM-12 PM; R 9-10 AM

---

## Required Materials

Students are expected to bring the following to **every class**:

- **Textbook:** *An Introduction to Analog and Digital Communications*, Simon Haykin and Michael Moher, 2nd ed., Wiley, 2011
  https://www.wiley.com/en-us/An+Introduction+to+Analog+and+Digital+Communications%2C+2nd+Edition-p-9781118313107

- Graphing or scientific calculator

- Good laptop computer with Radioconda Python computing environment (see setup instructions)

---

## Course Catalog Description

An understanding of the basic concepts and principles of analog and digital communication systems and performance of these systems in the presence of noise. Qualitative and quantitative analysis as well as computer tools will be employed in solving selected communication theory and systems problems. Three hours lecture.

---

## Prerequisites by Topic

Verify that you have speaking familiarity with:

- Complex numbers and complex arithmetic by hand and with a calculator; understanding of polar and Cartesian representation of complex numbers.

- Taylor expansions; even and odd functions

- Basic structure of sinusoids
  - Amplitude, frequency, phase
  - Taylor expansions of sinusoids
  - Derivatives and integral relationships of sine and cosine

- Euler's formula relating imaginary numbers to sinusoids.

- Idea of multiplying functions together vs. convolving them.

- Units in equations; units in function arguments esp. polynomial and transcendental functions.

- Unit step function (Heaviside function) and impulse function (Dirac delta function)

- Representation of time delays in functions

- Basic programming in Python (variables, loops, functions, arrays)

- Basic probability concepts (random variables, mean, variance) — helpful but will be reviewed

We will review all of these but fairly quickly, so that we may consolidate them into Fourier analysis and communications signal studies.

---

## Student Learning Outcomes

Upon completion of this course, students will be able to:

1. Apply Fourier analysis to characterize signals in time and frequency domains.

2. Analyze and simulate analog modulation techniques (AM, FM, SSB) and their demodulation.

3. Analyze and simulate digital modulation techniques (ASK, FSK, PSK, QAM) and evaluate spectral efficiency tradeoffs.

4. Explain I/Q (in-phase/quadrature) signal representation and its role in modern communication systems.

5. Evaluate communication system performance in the presence of noise using SNR, BER, and EVM metrics.

6. Use software tools (Python, GNU Radio) to simulate and analyze communication systems.

7. Describe the architecture and modulation schemes used in modern wireless systems (WiFi, cellular, satellite).

---

## Class Attendance and Zoom/Teams Participation

Class attendance is not formally required but the discussions and demonstrations will be important. Students who miss quizzes, exams, or other in-class assessments may be given the opportunity to make them up based on circumstances and instructor discretion. Please let me know if you will not be able to attend class. Please arrive for class on time.

Even though this is an in-person class, I have ability to teach via telecon. This way if anyone needs to miss class or cannot be on-campus for any reason, they can still participate and complete the course. Even so, students are expected to be present in-person unless there is illness or exceptional circumstances. Please always contact the instructor for permission prior to joining by telecon.

---

## Late Submission of Assignments

Assignments that are submitted late will be graded at the discretion of the instructor. Late assignments may be subject to a penalty or given no credit at all.

---

## Grade Determination and Assessment

The grade breakdown of this course will consist of the following weighted components:

| Component | Weight | Description |
|-----------|--------|-------------|
| Homework | 15% | 5 assignments |
| Lab Reports | 15% | Python, GNU Radio, Phasor, and W3USR activities |
| Reading Quizzes | 10% | Via Brightspace |
| Exams | 50% | 2 midterms (15% each) + final (20%) |
| Course Notebook | 10% | Daily diary and final essay |

See the detailed schedule for specific due dates and topics.

### Homework (15%)

Five homework assignments covering course topics. You may collaborate with fellow class members; working together is encouraged. However, do not directly copy each other's solutions—this is considered cheating. If you work together, put down solutions in your own words and equations. Do not copy any solution from the internet. Violations will result in a zero for that assignment and possible reporting to the Dean. Late homework will not be accepted without extenuating circumstances.

### Lab Reports (15%)

Hands-on laboratory activities include Python/Jupyter simulations (5 labs), GNU Radio with RTL-SDR (2 labs), "Baba Yaga's Hut" phasor analysis (2 sessions), and W3USR amateur radio station activities (2 sessions, with optional satellite extra credit). Lab reports are due one week after the lab session unless otherwise specified.

### Reading Quizzes (10%)

Reading quizzes administered through Brightspace at the beginning of selected classes. Multiple-choice questions are randomly selected from a question bank covering the assigned reading. Purpose: Encourage students to read assigned textbook sections before class.

### Exams (50%)

Two midterm exams (15% each) and a comprehensive final exam (20%). Exams may be in-person, take-home, or a combination of both.

### Course Notebook and Essay (10%)

Please keep a daily diary of the course—at least one sentence written each class day of something interesting, new, insightful, research-idea-generating, patentable, etc. that you attained from the day's meeting. For the final, prepare a few sentences about a line of inquiry that came from the class: An idea for a research project, for a patent or a product, for an item of performance art or painting or sculpture, or for anything else pertinent to the class material and the engineering experience. We will also ask for constructive criticism of the semester. The essay and course notebook will be graded for submission only, but we will read every word of each one and return a comment to the writer. **Due at the final exam.**

### Amateur Radio Extra Credit Opportunities

Amateur (ham) radio is a licensed radio service for radio enthusiasts, communicators, builders, engineers, experimenters, and scientists. This is a great community to be part of if you are an engineer or physicist, and the amateur radio curriculum is closely aligned with that of communications systems. Extra credit points will be added to the final exam, up to a maximum of 30 points combined from all activities below.

**Amateur Radio Licenses:** Extra credit will be awarded based on earning the following amateur radio license classes. License examination must be completed during the semester to earn credit.

- Technician Class License (5 Extra Credit Points)
- General Class License (10 Extra Credit Points)
- Amateur Extra Class License (15 Extra Credit Points)

**Lackawanna Blind Association Tutoring:** This year, we are conducting a Community Based Learning (CBL)-affiliated project to help clients at the Lackawanna Blind Association earn their technician-class amateur radio license and become active in the amateur radio community. You will earn 5 extra credit points for every hour you spend tutoring clients at the Blind Association.

---

## Grading Scale

The grading scale below represents the minimum guaranteed letter grade for a given final numerical grade. I do make adjustments to the final grading scale based on overall class performance, so your final letter grade may be higher than what is shown on this chart.

| Grade | Percentage | Grade | Percentage |
|-------|------------|-------|------------|
| A     | 93–100%    | C+    | 77–79%     |
| A-    | 90–92%     | C     | 73–76%     |
| B+    | 87–89%     | C-    | 70–72%     |
| B     | 83–86%     | D+    | 65–69%     |
| B-    | 80–82%     | D     | 60–64%     |
|       |            | F     | 0–59%      |

---

## Course Schedule

Class meets Tuesday & Thursday, 2:30–3:45 PM.

### Phase 1: Foundation (Weeks 1–2)

| Week | Date | Topics | Textbook |
|------|------|--------|----------|
| 1    | Jan 27 | **Course intro, prerequisites review** | Ch 1–2.1 |
|      |      | Complex numbers, Euler's formula, I/Q representation | |
|      |      | Sinusoids, phasors, convolution, unit step/impulse | |
|      |      | *Python/Jupyter setup* | |
| 2    | Feb 3 | **Fourier analysis essentials** | Ch 2.2–2.5 |
|      |      | Fourier transforms, properties, time-frequency duality | |
|      |      | Bandwidth concepts, correlation | |
|      |      | *Python Lab 1: Fourier Analysis* | |

### Phase 2: Modulation Techniques (Weeks 3–8)

| Week | Date | Topics | Textbook |
|------|------|--------|----------|
| 3    | Feb 10 | **Amplitude Modulation (Analog + Digital)** | Ch 3.1–3.3, 7.1–7.2 |
|      |      | AM theory: DSB-SC, envelope detection | |
|      |      | Binary ASK (On-Off Keying) | |
|      |      | *Python Lab 2: AM/ASK modulation* | |
| 4    | Feb 17 | **AM Systems & Receiver Architectures** | Ch 3.6–3.8 |
|      |      | SSB modulation, Hilbert transform, VSB | |
|      |      | Superheterodyne, direct conversion, direct sampling | |
|      |      | *W3USR: HF station tour, SSB/AM listening* | |
| 5    | Feb 24 | **EXAM 1** / Angle Modulation Intro | Ch 2–3, 7.1–7.2 |
| 6    | Mar 3 | **FM/PM Theory & Binary FSK** | Ch 4.1–4.5, 7.3–7.4 |
|      |      | Frequency deviation, narrowband vs wideband FM | |
|      |      | Binary FSK, CPFSK, MSK | |
| 7    | Mar 10 | **FM Systems & Binary PSK** | Ch 4.6–4.8, 7.2 |
|      |      | FM generation (VCO, Armstrong), Carson's rule | |
|      |      | BPSK fundamentals, coherent detection | |
|      |      | *Baba Yaga's Hut Lab (Part 1)* | |
| —    | Mar 14–22 | **SPRING BREAK – No Classes** | |
| 8    | Mar 24 | **Pulse Modulation & Sampling** | Ch 5 |
|      |      | Sampling theorem (real vs I/Q), Nyquist rate | |
|      |      | PAM, quantization, PCM, delta modulation | |
|      |      | *Baba Yaga's Hut Lab (Part 2)* | |

### Phase 3: Advanced Digital Communications (Weeks 9–11)

| Week | Date | Topics | Textbook |
|------|------|--------|----------|
| 9    | Mar 31 | **Baseband Digital & Spread Spectrum Intro** | Ch 6 |
|      |      | ISI, eye diagrams, synchronization (PLL, Costas) | |
|      |      | OFDM basics, spread spectrum (DSSS, FHSS) | |
|      |      | *GNU Radio Lab 1: FM reception, WiFi spectrum* | |
| —    | Apr 3–6 | **EASTER BREAK – No Classes** | |
| 10   | Apr 7 | **CDMA & M-ary Modulation** | Ch 7.5–7.7 |
|      |      | CDMA, Walsh codes, GPS, 3G cellular | |
|      |      | QPSK, M-ary PSK, QAM (16/64/256-QAM), EVM | |
|      |      | FT8 digital mode with Costas arrays | |
|      |      | *Python Labs 3 & 4: CDMA, QPSK/QAM/EVM* | |
|      |      | *W3USR: Digital modes (FT8, APRS)* | |
| 11   | Apr 14 | **EXAM 2** / Probability Intro | Ch 4–7 |

### Phase 4: Noise, Probability & System Performance (Weeks 12–15)

| Week | Date | Topics | Textbook |
|------|------|--------|----------|
| 12   | Apr 21 | **Probability & Random Variables** | Ch 8.1–8.4 |
|      |      | Probability axioms, Bayes' theorem, Shannon capacity | |
|      |      | PDFs, CDFs, Gaussian distribution, Q-function | |
| 13   | Apr 28 | **Noise in Communication Systems** | Ch 9, 11.1–11.3 |
|      |      | Thermal noise, AWGN, noise figure | |
|      |      | SNR in AM and FM, FM threshold effect | |
|      |      | *W3USR: Digital modes (FT8, APRS)* | |
| 14   | May 5 | **Digital Performance & Channel Coding** | Ch 10 |
|      |      | BER fundamentals, matched filtering | |
|      |      | BER for BPSK, FSK, QAM; EVM vs BER | |
|      |      | Channel coding: LDPC, Turbo, Polar codes | |
|      |      | *GNU Radio Lab 2: Noise and SNR analysis* | |
| 15   | May 12 | **Link Budgets & Modern Systems** | Ch 11.4–11.7 |
|      |      | Link budget calculations, path loss | |
|      |      | WiFi, LTE, 5G overview; SDR concepts | |
|      |      | *Python Lab 5: BER simulation* | |
|      |      | *May 14: No class (Hamvention)* | |

### Final Exam (Thursday, May 21, 12:45–2:45 PM)

Comprehensive exam covering all course material, with emphasis on noise and system performance (Chapters 8–11).

---

## University Policies and Resources

Please review the separate **University Policies and Resources** document for important information regarding:

- Student Conduct Statement
- Academic Dishonesty Policy
- Students with Disabilities / Accommodations
- Mental Health Resources
- Writing Center Services
- CARE Team Referrals
- Center for Health Education & Wellness (CHEW)
- Title IX / Required Reporter Obligations
- Non-Discrimination Statement

---

*This course material was prepared by Nathaniel Frissell with assistance from [Claude.ai](https://claude.ai).*

*The instructor reserves the right to modify this document and will give students advanced notice.*
