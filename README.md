# EE 451: Communications Systems - Student Materials

**Spring 2026 | TR 2:30-3:45 PM | Loyola Science Center Room 142**

Welcome to EE 451! This repository contains course materials including lecture notebooks, homework assignments, and resources.

**Final Exam:** Thursday, May 21, 12:45-2:45 PM

## Contents

```
├── README.md                 # This file
├── environment.yml           # Conda environment configuration
├── lectures/                 # Interactive Jupyter notebooks
│   └── lecture_XX_notebook.ipynb
├── labs/                     # Lab worksheets
│   ├── python_lab_*.ipynb        # Python/Jupyter labs
│   ├── gnuradio_lab_*.md         # GNU Radio labs
│   └── w3usr_activity_*.md       # W3USR station activities
├── homework/                 # Homework assignments
│   └── homework_*.md
├── syllabus/                 # Course documents
│   ├── syllabus.md
│   ├── ee451_detailed_schedule.md
│   └── university_policies_resources.md
├── exams/                    # Exam study guides
│   ├── midterm_1_study_guide.md
│   ├── midterm_2_study_guide.md
│   └── final_exam_study_guide.md
├── resources/                # Reference materials
│   ├── w3usr_equipment.md
│   ├── GE-Frequency-Modulation-Primer-(1941).pdf
│   └── the-hut-on-phasors-legs.pdf
└── pdf/                      # PDF versions for Brightspace
    ├── homework/
    ├── syllabus/
    ├── exams/
    ├── labs/
    └── resources/
```

**Note:** Markdown files are the primary format and render nicely on GitHub. PDF versions are in the `pdf/` subdirectory for uploading to Brightspace.

## Getting Started

### 1. Install Radioconda

Radioconda is a conda distribution that includes Python, Jupyter, GNU Radio, and SDR tools pre-configured.

**Download:** https://github.com/ryanvolz/radioconda/releases

Choose the installer for your operating system:
- **Windows:** `radioconda-*-Windows-x86_64.exe`
- **macOS:** `radioconda-*-MacOSX-x86_64.pkg` (Intel) or `radioconda-*-MacOSX-arm64.pkg` (Apple Silicon)
- **Linux:** `radioconda-*-Linux-x86_64.sh`

### 2. Create the Course Environment

After installing radioconda, open a terminal (or Anaconda Prompt on Windows) and run:

```bash
# Navigate to this repository
cd path/to/ee451-student

# Create the environment
conda env create -f environment.yml

# Activate the environment
conda activate ee451
```

### 3. Launch Jupyter Lab

With the environment activated:

```bash
jupyter lab
```

This will open Jupyter Lab in your web browser. Navigate to the `lectures/` folder to open the notebooks.

### 4. Verify Installation

In Jupyter Lab, create a new notebook and run:

```python
import numpy as np
import scipy
import matplotlib.pyplot as plt

print(f"NumPy: {np.__version__}")
print(f"SciPy: {scipy.__version__}")
print("Installation successful!")
```

## Using the Lecture Notebooks

1. **Before class:** Read assigned textbook sections
2. **During class:** Follow along with the Jupyter notebook on your laptop
3. **Experiment:** Modify code cells to explore concepts
4. **Save your work:** Use "File > Save" or Ctrl+S frequently

### Tips for Jupyter Notebooks

- **Run a cell:** Press `Shift+Enter`
- **Run all cells:** Menu > Run > Run All Cells
- **Clear outputs:** Menu > Edit > Clear All Outputs
- **Restart kernel:** Menu > Kernel > Restart Kernel

## Homework Assignments

Homework assignments are in the `homework/` folder (markdown format, with PDFs in `pdf/homework/`). Submit your work through Brightspace by the due date.

**LaTeX Tip:** Mathematical expressions in the PDFs use standard notation. When writing solutions, you can use the same LaTeX syntax in Jupyter notebooks:
- Inline: `$E_b/N_0$` renders as $E_b/N_0$
- Display: `$$P = \frac{A^2}{2R}$$`

## Lab Worksheets

Lab worksheets are in the `labs/` folder. There are three types of labs:

### Python Labs (Jupyter Notebooks)

- **python_lab_1_fourier.ipynb** - Fourier Analysis and Spectrum
- **python_lab_2_am_ask.ipynb** - AM and ASK Modulation
- **python_lab_3_cdma.ipynb** - CDMA and Spread Spectrum
- **python_lab_4_qam_evm.ipynb** - QPSK/QAM and EVM
- **python_lab_5_ber.ipynb** - BER Performance Simulation

Complete the TODO cells, answer all questions, and submit the completed notebook to Brightspace.

### GNU Radio Labs (Markdown Worksheets)

- **gnuradio_lab_1_fm_wifi.md** - FM Broadcasting & WiFi Signals
- **gnuradio_lab_2_noise_snr.md** - Noise, SNR, and Signal Quality

Build the specified flowgraphs, capture screenshots, and complete the worksheet. Submit the PDF and your .grc files.

### W3USR Activities (Markdown Worksheets)

- **w3usr_activity_1_hf_tour.md** - HF Station Tour & Propagation
- **w3usr_activity_2_digital_modes.md** - Digital Modes & Data Communication
- **w3usr_activity_3_satellite.md** - Satellite Communication

Complete these during W3USR station visits. Answer questions based on your observations.

## GNU Radio Labs

Some labs use GNU Radio for software-defined radio experiments. If you installed radioconda, GNU Radio is already available:

```bash
conda activate ee451
gnuradio-companion
```

For RTL-SDR experiments, you'll also need an RTL-SDR USB dongle (available from the instructor during lab sessions or ~$25 online).

## Troubleshooting

### "conda: command not found"

Make sure you've installed radioconda and it's in your PATH. On Windows, use the "Anaconda Prompt" instead of regular Command Prompt.

### Package import errors

Ensure you've activated the environment:
```bash
conda activate ee451
```

### Jupyter won't start

Try reinstalling jupyterlab:
```bash
conda activate ee451
conda install -c conda-forge jupyterlab
```

### Need help?

- Check the course discussion board on Brightspace
- Attend office hours
- Email the instructor

## Resources

- **Textbook:** *An Introduction to Analog and Digital Communications (2nd Ed.)* by Haykin & Moher
- **W3USR Station:** See `resources/w3usr_equipment.md` for amateur radio station documentation
- **GE FM Primer (1941):** Historical reference on frequency modulation fundamentals
- **Phasor Lab:** Materials for the "Baba Yaga's Hut" phasor analysis lab
- **GNU Radio:** https://wiki.gnuradio.org/
- **Radioconda:** https://github.com/ryanvolz/radioconda

---

## Acknowledgments

This course material was prepared by Nathaniel Frissell using [Claude.ai](https://claude.ai).

- **W3USR amateur radio station** for equipment access and demonstrations
- **Case Western Reserve University (W8EDU)** for Baba Yaga's Hut phasor lab materials

---

Good luck with EE 451!
