# GPR-Based Surrogate Model for Fatigue Safety Factor Prediction in Stepped Shafts

This repository contains the dataset and code for a Gaussian Process Regression (GPR) surrogate model that predicts the fatigue safety factor (SF) of stepped rotating shafts, eliminating the need for repeated ANSYS simulations during design exploration. The model takes five inputs — minor diameter (d), major diameter (D), fillet radius (r), bending moment (M), and loading ratio (R) — and outputs a probabilistic SF estimate with uncertainty bounds.

The model achieves R² = 0.9905, RMSE = 0.187, and a 5-fold cross-validation R² = 0.971 ± 0.022, validated against 314 high-fidelity ANSYS simulations generated via Latin Hypercube Sampling across five loading ratios (R = -2, -1, -0.5, 0, 0.3).

## Repository Structure
```
fatigue-surrogate-gpr/
├── data/          # ANSYS simulation outputs across 5 R values
├── model.ipynb    # GPR model, training, evaluation, and plots
└── report.pdf     # Full technical report
```

## Preprint
[Under review]

## Requirements
- Python 3.x
- scikit-learn
- pandas, numpy, matplotlib
