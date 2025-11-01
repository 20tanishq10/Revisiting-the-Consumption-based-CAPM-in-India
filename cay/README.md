# CAY (Consumption-Wealth Ratio)

This folder contains the necessary files for constructing the **Consumption-Wealth ($\text{cay}$) ratio**, which is the crucial conditioning variable used in our asset pricing models.

## 📁 Contents

* **`CAY_construction.ipynb`**: The Python Jupyter Notebook used to perform the cointegration test and calculate the $\text{cay}$ series from the raw macro data.

* **`cay_index.csv`**: The computed, final time series of the stationary $\text{cay}$ index, ready for use in subsequent model analyses.

## 📝 Description

The cay ratio represents the stationary residual (uₜ) from the long-run cointegrating equilibrium among log consumption (ln(Cₜ)), log asset wealth (ln(Aₜ)), and log labor income (ln(Yₜ)):

$$
\text{cay}_t = \ln(C_t) - \hat{\alpha} - \hat{\beta_a} \ln(A_t) - \hat{\beta_y} \ln(Y_t)
$$

The index is fundamental to our conditional C-CAPM tests, as it proxies for investors' expectations about future financial conditions.

## ▶️ Usage

1. **To Reproduce the CAY Series:** Run the cells in the **`CCAPM_India_Replication.ipynb`** notebook sequentially.

2. **To Use the Final Data:** The **`cay_index.csv`** file is used as a direct input for the time-series regressions in the main `All_Models_Combined.ipynb` notebook (`./Models/`).
