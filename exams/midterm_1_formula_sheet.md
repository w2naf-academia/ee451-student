---
header-includes:
  - \renewcommand{\arraystretch}{1.8}
  - \setlength{\parskip}{0.5em}
---

# EE 451: Communications Systems — Midterm Exam 1 Formula Sheet

\vspace{1em}

**Fourier Transform Pairs:**

| Time Domain | Frequency Domain |
|-------------|-----------------|
| $\delta(t)$ | $1$ |
| $1$ | $\delta(f)$ |
| $e^{-at}u(t), \; a > 0$ | $\frac{1}{a + j2\pi f}$ |
| $\text{rect}(t/T)$ | $T \cdot \text{sinc}(fT)$ |
| $\cos(2\pi f_0 t)$ | $\frac{1}{2}[\delta(f - f_0) + \delta(f + f_0)]$ |
| $\sin(2\pi f_0 t)$ | $\frac{j}{2}[\delta(f + f_0) - \delta(f - f_0)]$ |

\vspace{0.5em}

**Fourier Transform Properties:**

| Property | Time Domain | Frequency Domain |
|----------|------------|-----------------|
| Linearity | $a x_1(t) + b x_2(t)$ | $a X_1(f) + b X_2(f)$ |
| Time shift | $x(t - t_0)$ | $X(f) e^{-j2\pi f t_0}$ |
| Frequency shift | $x(t) e^{j2\pi f_0 t}$ | $X(f - f_0)$ |
| Scaling | $x(at)$ | $\frac{1}{\lvert a \rvert} X(f/a)$ |
| Convolution | $x(t) * h(t)$ | $X(f) \cdot H(f)$ |
| Modulation | $x(t)\cos(2\pi f_0 t)$ | $\frac{1}{2}[X(f - f_0) + X(f + f_0)]$ |

\vspace{0.5em}

**Parseval's Theorem:**

$$E = \int_{-\infty}^{\infty} |x(t)|^2 \, dt = \int_{-\infty}^{\infty} |X(f)|^2 \, df$$

**Useful Integral:**

$$\int_{-\infty}^{\infty} \text{sinc}^2(x) \, dx = 1$$

\vspace{0.5em}

**Trigonometric Identities:**

| Identity | Formula |
|----------|---------|
| Product | $\cos(A)\cos(B) = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$ |
| Half-angle | $\cos^2(A) = \frac{1}{2}[1 + \cos(2A)]$ |

\vspace{0.5em}

**AM Formulas:**

| Type | Formula |
|------|---------|
| Full AM | $s(t) = A_c[1 + \mu \, m_n(t)] \cos(2\pi f_c t)$ |
| Total power (general) | $P_{\text{total}} = \frac{A_c^2}{2R}\left(1 + \mu^2 \langle m_n^2(t) \rangle\right)$ |
| Total power (single tone) | $P_{\text{total}} = \frac{A_c^2}{2R}\left(1 + \frac{\mu^2}{2}\right)$ since $\langle \cos^2 \rangle = \tfrac{1}{2}$ |
| Efficiency | $\eta = \frac{\mu^2 \langle m_n^2(t) \rangle}{1 + \mu^2 \langle m_n^2(t) \rangle}$ |
| DSB-SC | $s(t) = A_c \, m(t) \cos(2\pi f_c t)$ |
| SSB (USB) | $s(t) = \tfrac{1}{2}A_c[m(t)\cos(2\pi f_c t) - \hat{m}(t)\sin(2\pi f_c t)]$ |

\vspace{0.5em}

**Receiver and Other:**

| Name | Formula |
|------|---------|
| Image frequency (high-side injection) | $f_{\text{image}} = f_{\text{RF}} + 2 f_{\text{IF}}$ |
| Filter quality factor | $Q = f_{\text{center}} / B_{\text{channel}}$ |
| sinc function (Haykin Eq. 2.9) | $\text{sinc}(x) = \sin(\pi x)/(\pi x)$ |
| Euler's formula | $e^{j\theta} = \cos(\theta) + j\sin(\theta)$ |

**Reference:** Standard AM broadcast channel bandwidth in the Americas: $B_{\text{channel}} = 10$ kHz.
