# 📊 Fama-French Portfolios

This folder contains the data and scripts used to construct and analyze Fama-French portfolios for the replication and testing of CAPM, C-CAPM, and conditional models in the Indian market. These files are essential for computing portfolio returns and risk factors, as well as for running Fama–MacBeth regressions.

## 🗂 Contents

| File | Description |
|------|-------------|
| `Fama_French_Construction.ipynb` | Jupyter Notebook source file for constructing Fama-French 6 portfolios and factors. Includes code for loading, processing, and analyzing portfolio returns. |
| `FF_factors_SMB_HML.csv` | CSV file containing standard Fama-French factors: SMB (Small minus Big), HML (High minus Low), and market excess returns. |
| `FF6_counts.csv` | Number of stocks in each Fama-French 6 portfolio per period. Useful for weighting and portfolio diagnostics. |
| `FF6_portfolios.csv` | Returns for each Fama-French 6 portfolio. Used as the dependent variables in empirical tests. |

## 🚀 Usage

1. Load the CSV files into your analysis environment (Python, R, etc.).
2. Use `Fama_French_6.ipynb` as a guide to replicate the portfolio construction and factor calculations.
3. The portfolio returns and factor data can be combined with the `cay` variable and other macroeconomic series to test conditional CAPM models.
