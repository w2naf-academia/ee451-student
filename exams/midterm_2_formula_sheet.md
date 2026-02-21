---
header-includes:
  - \renewcommand{\arraystretch}{1.8}
  - \setlength{\parskip}{0.5em}
---

# EE 451: Communications Systems — Midterm Exam 2 Formula Sheet

\vspace{1em}

**FM/PM Formulas:**

| Name | Formula |
|------|---------|
| FM instantaneous frequency | $f_i(t) = f_c + k_f \cdot m(t)$ |
| FM frequency deviation | $\Delta f = k_f \cdot \max\lvert m(t) \rvert$ |
| FM modulation index | $\beta = \Delta f / f_m$ |
| Carson's rule (FM bandwidth) | $B_{\text{FM}} = 2(\Delta f + f_m) = 2f_m(\beta + 1)$ |
| NBFM criterion | $\beta \ll 1$ (typically $\beta < 0.3$) |
| PM instantaneous phase | $\theta_i(t) = 2\pi f_c t + k_p \cdot m(t)$ |
| PM phase deviation | $\Delta\phi = k_p \cdot \max\lvert m(t) \rvert$ |
| PM instantaneous frequency | $f_i(t) = f_c + \frac{k_p}{2\pi}\frac{dm(t)}{dt}$ |
| PM frequency deviation (sinusoidal) | $\Delta f_{\text{PM}} = k_p \cdot A_m \cdot f_m$ |

\vspace{0.5em}

**Digital Modulation Formulas:**

| Name | Formula |
|------|---------|
| Bit duration | $T_b = 1 / R_b$ |
| FSK modulation index | $h = \Delta f \cdot T_b$ |
| FSK orthogonality (coherent) | $\Delta f_{\min} = 1/(2T_b) = R_b/2$ |
| MSK (Minimum Shift Keying) | $h = 0.5$, so $\Delta f = R_b/2$ |
| FSK bandwidth approximation | $B_{\text{FSK}} \approx 2\Delta f + R_b$ |
| Null-to-null bandwidth (BPSK/ASK) | $B = 2R_b$ |
| M-ary bits per symbol | $k = \log_2(M)$ |
| Symbol rate | $R_s = R_b / k$ |
| QPSK null-to-null bandwidth | $B_{\text{QPSK}} = 2R_s = R_b$ |
| Spectral efficiency | $\eta = R_b / B$ (bits/s/Hz) |

\vspace{0.5em}

**Noise Formulas:**

| Name | Formula |
|------|---------|
| Thermal noise power | $P_n = kTB$ where $k = 1.38 \times 10^{-23}$ J/K |
| SNR (dB) | $\text{SNR} = 10\log_{10}(P_s / P_n)$ |
| Noise figure (linear) | $F = \text{SNR}_{\text{in}} / \text{SNR}_{\text{out}}$ |
| Noise figure (dB) | $NF = 10\log_{10}(F)$ |
| Equivalent noise temperature | $T_e = (F - 1) \cdot T_0$ |
| System noise temperature | $T_{\text{sys}} = T_{\text{ant}} + T_e$ |
| Friis cascaded noise figure | $F_{\text{total}} = F_1 + \frac{F_2 - 1}{G_1} + \frac{F_3 - 1}{G_1 G_2} + \cdots$ |
| Noise power (dBm) | $N = -174 + 10\log_{10}(B)$ where $B$ is in Hz |

\vspace{0.5em}

**Link Budget Formulas:**

| Name | Formula |
|------|---------|
| EIRP | $\text{EIRP} = P_t \cdot G_t$ (linear) or $P_t + G_t$ (dB) |
| Friis transmission equation | $P_r = P_t G_t G_r \left(\frac{\lambda}{4\pi d}\right)^2$ |
| Free-space path loss (dB) | $L_p = 20\log_{10}(d) + 20\log_{10}(f) + 32.45$ |
| (units for path loss formula) | $d$ in km, $f$ in MHz |
| Link margin | $\text{Margin} = \text{SNR} - \text{SNR}_{\text{req}}$ |

\vspace{0.5em}

**Useful Identities:**

| Name | Formula |
|------|---------|
| dB conversion | $X_{\text{dB}} = 10\log_{10}(X)$ |
| dBm to watts | $P_W = 10^{(P_{\text{dBm}} - 30)/10}$ |
| Watts to dBm | $P_{\text{dBm}} = 10\log_{10}(P_W) + 30$ |
| Euler's formula | $e^{j\theta} = \cos\theta + j\sin\theta$ |

**Reference:** $T_0 = 290$ K (standard reference temperature). $k = 1.38 \times 10^{-23}$ J/K (Boltzmann's constant).
