# Running Blade AI — MSc Thesis Pipeline

**"Performance Optimization of Running Blade Prosthetics Using Advanced Materials"**
Mansoura University — Faculty of Engineering, Biomedical Engineering

---

## What this is

A fully automated, code-driven research pipeline for AI-driven design and optimization of carbon-fiber running blade prostheses. No manual CAD redraws. No manual ANSYS clicks.

The pipeline goes:

```
Parametric Blade Generator (nTop + Python)
              ↓
Automated FEA Dataset (PyANSYS / APDL)
              ↓
Graph Neural Network Surrogate Model (PyTorch Geometric)
              ↓
Multi-Objective Optimization (NSGA-II / RL)
              ↓
Pareto-Optimal Blade Designs
              ↓
Validation (Full FEA on top candidates)
```

---

## Project structure

```
running-blade-ai/
│
├── geometry/              # nTop notebook files and exported geometries
│   ├── ntop/              # .ntop blade notebook files
│   └── exports/           # STL / STEP exports from nTop
│
├── simulation/            # FEA automation
│   ├── scripts/           # PyANSYS / APDL scripts
│   └── results/           # Raw ANSYS output files
│
├── data/                  # Generated datasets
│   ├── raw/               # Direct outputs from nTop and ANSYS
│   └── processed/         # Cleaned, merged dataset CSV files
│
├── ml/                    # Machine learning models
│   ├── surrogate/         # Traditional ML surrogates (RF, XGBoost)
│   └── gnn/               # Graph Neural Network surrogate
│
├── optimization/          # Multi-objective optimization
│   └── nsga2/             # NSGA-II and Pareto front generation
│
├── notebooks/             # Jupyter notebooks for exploration and viz
│
├── scripts/               # Core automation scripts
│   ├── blade_generator.py
│   ├── automation.py
│   └── dataset_builder.py
│
├── docs/                  # Research log and notes
│   └── research_log.md
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Setup

```bash
git clone https://github.com/YOUR_USERNAME/running-blade-ai.git
cd running-blade-ai
python -m venv venv
venv\Scripts\activate       # Windows
pip install -r requirements.txt
```

---

## Current phase

- [x] Phase 0 — Research architecture and repo setup
- [ ] Phase 1 — Parametric blade generator (nTop + Python automation)
- [ ] Phase 2 — Automated FEA dataset generation (PyANSYS)
- [ ] Phase 3 — GNN surrogate model (PyTorch Geometric)
- [ ] Phase 4 — Multi-objective optimization (NSGA-II)
- [ ] Phase 5 — Validation and analysis

---

## Author

Esraa Ahmed Rashad — Biomedical Engineering, Mansoura University
