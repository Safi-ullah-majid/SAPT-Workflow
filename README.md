<div align="center">

# ⚛️ SAPT Workflow with Psi4

[![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Psi4](https://img.shields.io/badge/Psi4-Quantum%20Chemistry-orange?style=for-the-badge)](https://psicode.org)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Stars](https://img.shields.io/github/stars/yourusername/SAPT-Workflow?style=for-the-badge&logo=github)](https://github.com/yourusername/SAPT-Workflow)

**An automated Google Colab workflow for Symmetry-Adapted Perturbation Theory (SAPT) calculations using Psi4.**

*From Gaussian output → SAPT energy decomposition → publication-ready results. No local installation required.*

[🚀 Open in Colab](#) · [📖 Documentation](#) · [🐛 Report Bug](#) · [💡 Request Feature](#)

---

</div>

## 📸 Overview

> SAPT decomposes noncovalent interaction energies into physically meaningful components — electrostatics, exchange, induction, and dispersion — giving you deep insight into what drives molecular recognition and binding.

This workflow automates the entire pipeline so you can go from a Gaussian output file to a fully analyzed SAPT result in minutes.

---

## ✨ Features

| Feature | Details |
|---|---|
| 📂 **File Support** | Upload `.log`, `.out`, `.gjf`, or `.xyz` files |
| 🔍 **Auto Geometry Extraction** | Pulls the final optimized geometry from Gaussian output |
| ✂️ **Fragment Detection** | Splits the complex into two molecular fragments |
| ⚙️ **Input Generation** | Auto-generates Psi4 SAPT input files |
| 🧮 **SAPT Levels** | SAPT0 · SAPT2 · SAPT2+ · SAPT2+(3) |
| 📊 **Energy Decomposition** | Electrostatic · Exchange · Induction · Dispersion · Total |
| 📈 **Visualization** | Publication-ready bar charts and plots |
| 📄 **Export** | Excel · CSV · TXT outputs |
| ☁️ **Zero Setup** | Runs entirely on Google Colab |

---

## 🚀 Workflow Pipeline

```
┌─────────────────────┐
│   Gaussian Output   │  (.log / .out / .gjf / .xyz)
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Extract Final      │  Automatically parses optimized geometry
│  Geometry           │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Define Fragment    │  Set fragment boundary atom number,
│  Boundary           │  charge & multiplicity
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Generate Psi4      │  Auto-built SAPT input with correct
│  Input File         │  dimer-centered basis
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Run SAPT           │  SAPT0 / SAPT2 / SAPT2+ / SAPT2+(3)
│  Calculation        │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Extract Energy     │  Elst · Exch · Ind · Disp · Total
│  Components         │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────────────┐
│  Excel · CSV · Figures · TXT   │
└─────────────────────────────────┘
```

---

## ▶️ Quick Start

### 1 — Open in Colab
Click the badge above or open `SAPT_Workflow.ipynb` directly in Google Colab.

### 2 — Run All Cells
All dependencies (Psi4, Pandas, NumPy, Matplotlib) install automatically.

### 3 — Upload Your File
Upload your Gaussian output when prompted (`.log`, `.out`, `.gjf`, or `.xyz`).

### 4 — Enter Parameters

```
Fragment 1 last atom number  →  e.g., 42
Charge of complex            →  e.g., 0
Multiplicity                 →  e.g., 1
SAPT level                   →  SAPT0 / SAPT2 / SAPT2+ / SAPT2+(3)
```

### 5 — Download Results
All output files are auto-generated and ready to download.

---

## 📊 Output Files

```
SAPT-Workflow/results/
│
├── SAPT_Results.xlsx       ← Full energy table (Excel)
├── SAPT_Results.csv        ← Machine-readable data
├── SAPT_Results.txt        ← Human-readable summary
├── SAPT_BarChart.png       ← Publication-ready bar chart
└── sapt.out                ← Raw Psi4 output
```

---

## 📦 Dependencies

All packages are installed automatically inside the notebook. For reference:

```python
psi4          # Quantum chemistry engine
pandas        # Data handling & Excel export
numpy         # Numerical operations
matplotlib    # Plotting & visualization
```

> **Requirements:** Google Colab · Python 3.11

---

## 💡 Applications

This workflow is well-suited for studying:

- 🧲 **Noncovalent interactions** — hydrogen bonds, π–π stacking, van der Waals
- 🏠 **Host–guest complexes** — macrocycle binding, inclusion compounds
- 🔬 **Molecular adsorption** — surface-molecule interactions
- 🧬 **Supramolecular chemistry** — self-assembly, recognition
- 📡 **Organic sensing systems** — sensor-analyte binding analysis

---

## 📁 Repository Structure

```
SAPT-Workflow/
│
├── 📓 SAPT_Workflow.ipynb      ← Main notebook
├── 📄 README.md
├── 📜 LICENSE
│
├── examples/
│   ├── sample.log              ← Example Gaussian output
│   └── sample_output.xlsx      ← Example results
│
└── images/
    └── workflow.png
```

---

## 📚 Citation

If you use this workflow in your research, please cite the Psi4 package and consider citing this repository:

```bibtex
@misc{SAPT-Workflow,
  author       = {Your Name},
  title        = {SAPT Workflow with Psi4},
  year         = {2025},
  publisher    = {GitHub},
  url          = {https://github.com/yourusername/SAPT-Workflow}
}
```

> **Psi4 Citation:** D.G.A. Smith et al., *J. Chem. Theory Comput.* **2020**, 16, 2, 727–760.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get involved:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

Bug reports and feature requests can be submitted via [Issues](#).

---

## 📜 License

Released under the **MIT License** — see [`LICENSE`](LICENSE) for details.

---

<div align="center">

**If this project helped your research, please consider giving it a ⭐ Star.**

*It helps others discover the workflow and motivates continued development.*

[![Star History](https://img.shields.io/github/stars/yourusername/SAPT-Workflow?style=social)](https://github.com/yourusername/SAPT-Workflow)

</div>
