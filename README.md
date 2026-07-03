# 🧪 SAPT Workflow with Psi4

> **An automated Google Colab workflow for Symmetry-Adapted Perturbation Theory (SAPT) calculations using Psi4.**

This notebook streamlines SAPT calculations by automating the entire workflow—from Gaussian output processing to SAPT energy decomposition analysis.

---

## ✨ Features

- 📂 Upload Gaussian `.log`, `.out`, `.gjf`, or `.xyz` files
- 🔍 Automatically extract the **final optimized geometry**
- ✂️ Split the complex into two molecular fragments
- ⚙️ Generate Psi4 SAPT input automatically
- 🧮 Run **SAPT0**, **SAPT2**, **SAPT2+**, or **SAPT2+(3)**
- 📊 Extract:
  - Electrostatic Energy
  - Exchange Energy
  - Induction Energy
  - Dispersion Energy
  - Total Interaction Energy
- 📈 Generate publication-ready plots
- 📄 Export results to **Excel**, **CSV**, and **TXT**
- ☁️ Runs entirely on **Google Colab** (no local installation required)

---

## 📁 Repository Structure

```
SAPT-Workflow/
│
├── SAPT_Workflow.ipynb
├── README.md
├── LICENSE
│
├── examples/
│   ├── sample.log
│   └── sample_output.xlsx
│
└── images/
    └── workflow.png
```

---

## 🚀 Workflow

```
Gaussian Output
       │
       ▼
Extract Final Geometry
       │
       ▼
Define Fragment Boundary
       │
       ▼
Generate Psi4 Input
       │
       ▼
Run SAPT Calculation
       │
       ▼
Extract Energy Components
       │
       ▼
Excel • CSV • Figures
```

---

## 📦 Requirements

- Google Colab
- Python 3.11
- Psi4
- Pandas
- NumPy
- Matplotlib

All required packages are installed automatically inside the notebook.

---

## ▶️ How to Use

1. Open the notebook in Google Colab.
2. Run all cells.
3. Upload your Gaussian output (`.log`, `.out`, `.gjf`, or `.xyz`).
4. Enter:
   - Fragment 1 last atom number
   - Charge
   - Multiplicity
5. Start the SAPT calculation.
6. Download the generated results.

---

## 📊 Output Files

The notebook automatically generates:

- `SAPT_Results.xlsx`
- `SAPT_Results.csv`
- `SAPT_Results.txt`
- `SAPT_BarChart.png`
- `sapt.out`

---

## 💡 Applications

This workflow can be used for studying:

- Molecular adsorption
- Host–guest complexes
- Hydrogen bonding
- π–π interactions
- Supramolecular chemistry
- Organic sensing systems
- Noncovalent interactions

---

## 📚 Citation

If you use this workflow in your research, please cite the Psi4 software and consider citing this repository.

---

## 🤝 Contributing

Contributions, feature requests, and bug reports are welcome.

If you have suggestions or improvements, feel free to open an issue or submit a pull request.

---

## 📜 License

This project is released under the **MIT License**.

---

## ⭐ Support

If you find this project useful, please consider giving the repository a **⭐ Star**.

It helps others discover the project and supports future development.
