# Philippine GDP Solver Comparison

Fits a cubic spline through Philippine quarterly GDP data (Q1 1981 to Q4 2025) and compares three solvers for the resulting tridiagonal linear system.

## Files

**`philippines_gdp_quarterly.csv`**  
Quarterly GDP data from 1981 to 2025. Columns: period, time index, expenditure components (household consumption, government spending, capital formation, exports, imports, statistical discrepancy), and total GDP in million PHP.

**`GDP_solvers_comparison.ipynb`**  
Loads the CSV, sets up the cubic spline interpolation problem as a tridiagonal system, then solves it three ways:

- Thomas Algorithm (direct, O(n))
- Jacobi (iterative)
- Gauss-Seidel (iterative)

Outputs three plots: the GDP time series with the spline overlaid, convergence history for the two iterative solvers, and a runtime/iteration count comparison across all three.

## Requirements

```
numpy
pandas
matplotlib
```

## Usage

Open and run `GDP_solvers_comparison.ipynb` in Jupyter or Colab. The CSV must be in the same directory as the notebook.
