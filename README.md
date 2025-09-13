# CS5710-Home-Assignment

# Linear Regression — Closed-Form vs Gradient Descent

This script fits a straight line to synthetic data in two ways and compares the results.

## What it does
- **Data generation:** Creates 200 samples with `x ~ U(0,5)` and noise `ε ~ N(0,1)` using the ground-truth model  
  **y = 3 + 4x + ε** (seed = 42).
- **Closed-form (Normal Equation):** Solves  
  **θ = (XᵀX)⁻¹Xᵀy** to get the intercept and slope.
- **Gradient Descent (GD):** Starts from θ = [0,0] and iteratively updates  
  **θ ← θ − η · (2/m) · Xᵀ(Xθ − y)** with **η = 0.05** for **1000** iterations. Tracks MSE each step.
- **Visualization:**
  - Scatter plot of the raw data with **two fitted lines** (closed-form and GD).
  - **Loss curve** (MSE vs iteration) showing GD convergence.
- **Output:** Prints both solutions (intercept & slope) and a brief comparison.  
  On this dataset they converge to (almost) the same values.

## Requirements
```bash
pip install numpy matplotlib
