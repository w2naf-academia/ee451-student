# EE 451: Communications Systems
# Theory Connection Study Sheet — Practical Exam Item 9

**Use this sheet to prepare for item 9 of the practical exam (4 pts).** During the practical, you will pick **one** operating task you performed at the W3USR station and explain how it connects to a course concept from earlier in the semester. You must include at least one **quantitative or technical detail** (a number, a formula, a dB value, a bandwidth, etc.). The instructor will then ask **one short follow-up question** to probe your understanding.

The connections below cover everything we discussed in L24–L27 (and the FT8 / Costas Arrays material from L22 and L23). You are not limited to these — if you see a different connection that you can defend, that is fine. Pick one and rehearse it out loud before exam day.

---

## 1. Phonetic alphabet ↔ Channel-robust symbol coding

**Operating task:** Spelling a callsign on the air using "Whiskey Three Uniform Sierra Romeo" instead of "W-3-U-S-R."

**Course concept:** A noisy channel can corrupt single letters in unpredictable ways. The phonetic alphabet replaces each one-symbol letter with a polysyllabic word whose vowel structure and envelope are *robust* against fading and noise. This is the human-audio analogue of a forward error-correcting code: spend more bandwidth (longer word per letter) to buy reliability against a low-SNR channel.

**Quantitative detail:** A spoken letter occupies roughly 100–200 ms; a phonetic word occupies roughly 400–700 ms. You are spending ~3–4× the time per letter for a much lower probability of being misheard. This is *exactly* the trade-off in repetition codes (e.g., the rate-1/3 repetition code from the Shannon discussion in L23 — 3× the bits, much lower error rate).

**Likely follow-up:** *"What if you had to design a phonetic alphabet for a channel that was even worse — say, 6 dB worse?"* (Answer: lengthen each word, or pick words with even more distinct envelopes; the trade-off curve is the same as picking longer block codes.)

---

## 2. RST report ↔ Human-in-the-loop SNR estimate

**Operating task:** Looking at the S-meter, listening to how clearly you can copy a station, and saying "you're 5-9 here in Scranton."

**Course concept:** RST is a compressed two-axis signal-quality estimate.
- **R** (Readability, 1–5) is essentially a subjective measurement of how often the operator misses a symbol — i.e., a *qualitative bit error rate*.
- **S** (Strength, 1–9) is calibrated against a known reference: **S9 = −73 dBm at the antenna terminals (50 µV across 50 Ω)**, with each S-unit nominally **6 dB**.

So when you say "S9," you are saying the received power is approximately −73 dBm. When you say "S7," you are saying it is approximately 12 dB lower than that.

**Quantitative detail:** S9 = −73 dBm. 1 S-unit ≈ 6 dB. "S9 + 20" means +20 dB above S9, or about −53 dBm. This is the same dB arithmetic from L18 / Ch 9.

**Likely follow-up:** *"If two signals differ by 3 S-units on the meter, what is their power ratio?"* (Answer: 18 dB → about 63×.)

---

## 3. Skip propagation ↔ Frequency-selective channel

**Operating task:** Hearing a Spanish station on 14 MHz but being unable to reach the same station on a VHF (144 MHz) handheld.

**Course concept:** The ionosphere is a *frequency-dependent* part of the channel. Below the **Maximum Usable Frequency (MUF)**, free electrons in the F2 layer refract the wave back to Earth — that is "skip." Above MUF, the signal punches through into space. Below the **Lowest Usable Frequency (LUF)**, the D layer absorbs too heavily.

This is a real-world example of a channel whose transfer function *H(f)* has a strong frequency dependence: HF passes one way (over the horizon), VHF passes another (line of sight). The "channel" we abstracted in problems is, in practice, this kind of layered, frequency-dependent medium.

**Quantitative detail:** Typical daytime MUF on a US-to-Europe path near solar maximum is in the range 20–30 MHz; nighttime drops it to 10–15 MHz. F2 critical frequencies near solar max can exceed 10 MHz overhead. VHF (30–300 MHz) almost always exceeds MUF, hence line-of-sight only.

**Likely follow-up:** *"Why does 40 m work better at night than during the day?"* (Answer: D-layer absorption disappears at night, opening the lower bands.)

---

## 4. Antenna gain and beam pointing ↔ Link budget

**Operating task:** Rotating the Yagi from 0° (north) to 60° (Europe) to work a German station, watching the S-meter rise.

**Course concept:** The Friis-style link equation is

  *P*<sub>RX</sub> (dBm) = *P*<sub>TX</sub> (dBm) + *G*<sub>TX</sub> (dBi) + *G*<sub>RX</sub> (dBi) − *L*<sub>path</sub> (dB) − other losses (dB)

A directional antenna is a *line item* in this equation: pointing the rotor at the correct bearing increases *G*<sub>RX</sub> by the antenna's forward gain (and, on transmit, *G*<sub>TX</sub> by the same factor due to reciprocity). Pointing the wrong way pulls in the back lobe — typically 15–25 dB lower than the main lobe.

**Quantitative detail:** A typical triband HF Yagi has ~6–8 dBi forward gain (i.e., 4–6× the EIRP of an isotropic radiator) and 15–25 dB front-to-back rejection. Going from boresight to off-axis can swing your effective SNR by 20+ dB.

**Likely follow-up:** *"What is the half-power beamwidth of a typical HF Yagi, and why does that matter when pointing?"* (Answer: 50–70°; it means you do not need to point exactly — within ±25° of target is fine.)

---

## 5. USB on 20 m ↔ Single-sideband and BFO recovery

**Operating task:** Selecting USB mode on the IC-7610 to listen to a 20 m phone signal that would sound like an unintelligible squeal in AM mode.

**Course concept:** SSB suppresses one sideband and the carrier; only one sideband is transmitted. In USB, the lower sideband and carrier are removed at the transmitter; in LSB, the upper sideband and carrier are removed. The receiver must reinsert a local *beat frequency oscillator* (BFO) at the location where the carrier *would have been* in order to demodulate. If you listen on the wrong sideband, the spectrum gets folded incorrectly and audio becomes garbled (the "Donald Duck" effect).

**Quantitative detail:** Above 10 MHz, the convention is USB; below 10 MHz, LSB. With the IC-7610's default 2.4 kHz SSB filter, a USB signal centered at 14.200 MHz occupies roughly 14.200 to 14.2024 MHz. Compare to AM broadcast at ~10 kHz total bandwidth (carrier + two ~5 kHz sidebands): SSB cuts the bandwidth roughly in half *and* transmits zero power in the carrier (the carrier is suppressed). Both are wins (Ch 3.6 in Haykin).

**Likely follow-up:** *"Why does SSB use half the bandwidth and lower power than AM, with the same intelligibility?"* (Answer: the carrier is gone — that was 50%+ of AM transmit power doing nothing — and only one sideband carries the message; the other was redundant.)

---

## 6. WSJT-X / IC-7610 panadapter ↔ Running FFT of I/Q baseband

**Operating task:** Watching the panadapter / waterfall display on the IC-7610 (or in WSJT-X during the FT8 demo) and seeing signals as bright vertical streaks.

**Course concept:** The radio downconverts RF to I/Q baseband samples. The display software takes the FFT of those samples on a sliding window, plots magnitude vs. frequency on the horizontal axis, and pushes time downward in the waterfall. This is *exactly* the spectrogram from the Baba Yaga lab — same operation, just with a different signal source.

**Quantitative detail:** Typical IC-7610 panadapter span: 50 kHz to 1 MHz, with FFT resolution near 10 Hz at the narrow setting. The FFT bin width *Δf = 1/T* where *T* is the time-window length, so a 100 ms window gives 10 Hz bins.

**Likely follow-up:** *"If I want finer frequency resolution on the waterfall, what do I have to give up?"* (Answer: time resolution — bin width and window length are inversely related, by Heisenberg / time-frequency duality.)

---

## 7. FT8 ↔ 8-ary FSK with engineered narrow bandwidth

**Operating task:** Watching FT8 decodes appear in WSJT-X with reported SNRs of −15 dB or worse during the L22 demo.

**Course concept:** FT8 is binary-FSK scaled up — 8 tones, 3 bits per symbol, a symbol rate equal to the tone spacing (orthogonal at minimum). Carson's rule gives the bandwidth.

**Quantitative detail:**
- 7 tone gaps × 6.25 Hz spacing + 1 tone width ≈ 50 Hz signal bandwidth (8 tones in a row). The "tone width" term accounts for the spectral spread of the outermost tones — each tone's main lobe extends roughly ±3.125 Hz from its center, adding half a tone-width at each end of the tone row. Equivalently: each tone occupies a 6.25 Hz "bin" (by the minimum-orthogonality condition Δf = 1/T_s), and 8 bins × 6.25 Hz each = 50 Hz.
- 79 symbols ÷ 6.25 baud ≈ 12.6 s per transmission (each symbol is 1/6.25 = 160 ms long)
- WSJT-X reports SNR in a 2500 Hz reference bandwidth. The bandwidth advantage alone is **10·log₁₀(2500/50) = 17 dB**. So a "−15 dB SNR" report actually means **+2 dB SNR in the signal's own 50 Hz bandwidth** — entirely decodable.
- **LDPC** (Low-Density Parity-Check) FEC adds another ~8–10 dB of coding gain. LDPC is a class of linear block error-correcting code defined by a *sparse* parity-check matrix and decoded iteratively (belief propagation). It is one of the modern near-Shannon-limit codes mentioned in L23, and is also used in WiFi (802.11n/ac/ax), 5G, and DVB-S2.

**Likely follow-up:** *"How would the bandwidth change if FT8 used 16 tones at the same symbol rate?"* (Answer: 15 gaps × 6.25 Hz + tone width ≈ 100 Hz signal bandwidth; you would gain 1 bit/symbol but lose 3 dB of bandwidth advantage relative to 2500 Hz reference noise — 10·log₁₀(2500/100) = 14 dB instead of 17 dB.)

---

## 8. Costas array sync sequence ↔ Thumbtack autocorrelation

**Operating task:** WSJT-X automatically locking onto FT8 transmissions even when stations are not time- or frequency-synchronized to each other.

**Course concept:** Each FT8 frame embeds three 7-symbol Costas-array synchronization sequences. A Costas array is a permutation matrix in which all displacement vectors between any two "ones" are distinct — that property gives the sequence a near-ideal autocorrelation function: one sharp central peak with all sidelobes ≤ 1. The decoder cross-correlates the received signal against the known Costas pattern and recovers exact time offset and frequency offset of every transmission, even in noise.

**Quantitative detail:** FT8 uses a 7×7 Costas array. Each sync sequence is 7 symbols × 160 ms = 1.12 s, and three of them are spaced through the 12.6 s frame. The autocorrelation peak-to-sidelobe ratio is approximately 7:1 for a length-7 sequence.

**Likely follow-up:** *"Why can't FT8 just use a barker code instead?"* (Answer: Barker codes are 1D — perfect for time alignment but not frequency alignment. Costas arrays are 2D, so they pin down both time and frequency simultaneously, which is exactly what FT8 needs because stations drift in both.)

---

## 9. ITU band assignments ↔ Propagation regime depends on frequency

**Operating task:** Choosing 20 m for a daytime overseas contact instead of 80 m or 6 m.

**Course concept:** The ITU divides the radio spectrum into named bands (HF, VHF, UHF, etc.) because each octave behaves *qualitatively differently* with respect to propagation, antenna size, and atmospheric absorption. The boundaries are not arbitrary — they line up with where the dominant propagation mechanism changes.

**Quantitative detail:**

| Band | Range | λ | Dominant propagation | Why |
|---|---|---|---|---|
| HF | 3–30 MHz | 100 m – 10 m | Ionospheric skip (F2 refraction) | Below MUF |
| VHF | 30–300 MHz | 10 m – 1 m | Line-of-sight; sporadic E | Above MUF; small antennas |
| UHF | 300 MHz – 3 GHz | 1 m – 10 cm | Strict line-of-sight; satellites | Atmosphere transparent; tiny antennas |

**Likely follow-up:** *"WiFi sits at 2.4 GHz instead of 14 MHz. What does it gain by going up there?"* (Answer: bandwidth — WiFi at 2.4 GHz uses 20 or 40 MHz channels, and at 5 GHz it goes up to 80–160 MHz. At 14 MHz the entire amateur band is only 350 kHz wide. Shannon capacity scales with bandwidth, which is why all data-hungry services live at GHz frequencies.)

---

## 10. Q-signals ↔ Source coding (compressed phrasing)

**Operating task:** Saying "QSY to 14.250" instead of "let us change frequency to 14.250 MHz," or hearing "lots of QRN here" instead of "there is a lot of natural atmospheric noise here."

**Course concept:** Q-signals are a small fixed alphabet of three-letter codes mapped to high-frequency-of-use phrases — the same idea as a source code (Huffman / Morse code) where common symbols get short codes. The "compression ratio" is enormous: "QRZ" (3 letters) replaces "Who is calling me?" (15 letters + spaces).

**Quantitative detail:** A typical Q-signal is 3 letters; the phrase it replaces averages 15–25 characters. Compression ratio ≈ 5–8×. Morse code: "E" (the most common English letter) is one dot; "Z" (uncommon) is dash-dash-dot-dot — same Huffman-style principle.

**Likely follow-up:** *"What is the trade-off of using Q-signals?"* (Answer: a fixed, finite codebook — Q-signals can only express a pre-agreed vocabulary, so anything outside the codebook still has to be sent in plain text. Same trade-off as Huffman vs. arithmetic coding.)

---

## 11. QSB (fading) ↔ Time-varying multipath channel

**Operating task:** Hearing the same station rise and fall in strength over 5–30 seconds — sometimes vanishing entirely, sometimes booming in.

**Course concept:** QSB ("the signal is fading") is the operator's name for what we modeled as a *time-varying channel*. The HF channel has multiple ionospheric paths whose lengths change with the ionosphere; the paths interfere constructively and destructively at the receiver, modulating the received amplitude. The same effect appears as multipath fading on cellular and WiFi channels at much faster timescales.

**Quantitative detail:** HF QSB rates are typically 0.05–0.3 Hz (cycles of 3–20 s). Cellular fast-fading from mobile motion is on the order of the Doppler frequency *f*<sub>D</sub> = *v*/λ — at 1 GHz and 30 m/s this is 100 Hz (10 ms cycles).

**Likely follow-up:** *"How would FT8 handle a 10 s deep fade in the middle of a 12.6 s transmission?"* (Answer: poorly — only ~17 of the 79 symbols would survive, which is on the edge of what LDPC can recover. FT8's real defenses against fading are LDPC's ability to fix erasures *plus* the long 160 ms symbol period (more energy accumulated per symbol), not the frame length itself.)

---

## How to use this sheet

1. **Read all 11 connections once.** Pick one or two that resonate.
2. **For your chosen connection, rehearse out loud** — the operating task, the concept, the quantitative detail. Aim for ~60 seconds.
3. **Anticipate the follow-up.** The likely-follow-up questions in this sheet are *examples* of what the instructor might ask; the actual question may differ. Be ready to extend your answer one step further.
4. **You are not limited to this sheet.** Any defensible connection between an operating task and a course concept is acceptable.

Good luck.
