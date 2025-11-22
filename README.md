# Revisiting the Consumption-Based CAPM in India  
### A Conditional Approach Using the Consumption–Wealth Ratio (cay)

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 👨‍🎓 Authors  
**Tanishq Gupta**, **Sourabh Hukkeri**, **Tushar Singh**  
Department of Humanities and Social Sciences,  
Indian Institute of Technology Roorkee  
📅 November 2025

---

## 📘 Overview  

This project **replicates and extends** the asset-pricing framework of:

> **Lettau, M. & Ludvigson, S. (2001).**  
> *Resurrecting the (C)CAPM: A Cross-Sectional Test When Risk Premia Are Time-Varying.*  
> *Journal of Political Economy, 109*(6), 1238–1287.

We investigate whether the **poor performance of CAPM and C–CAPM in India** arises due to the **assumption of constant risk premia**, and whether conditioning on the **consumption–wealth ratio (cay)** improves cross-sectional pricing performance.

---

## 🎯 Research Objectives  

- Examine whether **risk premia in India are time-varying**  
- Construct an **Indian analogue of the consumption–wealth ratio (cay)**  
- Test and compare multiple asset-pricing models:
  ✔ CAPM  
  ✔ Human Capital CAPM (HCAPM)  
  ✔ Consumption CAPM (CCAPM)  
  ✔ Scaled (conditional) models using `cay`  
  ✔ Fama–French Three-Factor Model (benchmark)  

---

## 🧠 Motivation  

Traditional models assume **investors have constant risk preferences**, but macroeconomic shocks change household consumption–wealth dynamics.  
When consumption is **low relative to wealth**, investors demand **higher compensation for bearing risk**.  
Thus, risk premia may be **state-dependent**, implying that a **conditional model** should outperform static asset-pricing models.

---

## 📊 Data Description (Aligned with Paper — Table 1)

| Variable | Description | Frequency | Source |
|-----------|-------------|-----------|--------|
| Household Consumption *(cₜ)* | PFCE – nondurables + services | Monthly | CMIE CPHS |
| Household Income *(yₜ)* | Monthly household income (weighted) | Monthly | CMIE CPHS |
| Asset Wealth *(aₜ)* | PCA-based synthetic wealth index | Monthly | CMIE Aspirational Data |
| Market Returns *(Rₘ)* | 6 Size–Value Portfolios (India) | Monthly | NSE / CMIE ProwessIQ |
| Risk-Free Rate *(Rᶠₜ)* | 91-day T-bill (annualized to monthly) | Monthly | RBI DBIE |
| Book-to-Market *(B/M)* | Equity book value / market cap | Annual | CMIE ProwessIQ |

> All nominal variables are **deflated using the CPI** (2012 = 100).

---

## ⚙️ Methodology Overview  

### **Asset-Pricing Models Estimated**

| Category | Models |
|---------|--------|
| **Unconditional** | CAPM, HCAPM, CCAPM |
| **Conditional** | Scaled versions using `cayₜ` |
| **Benchmark** | Fama–French 3-Factor Model |

- Time-series estimation:  
  ```math
  R_{i,t+1} = \alpha_i + \beta_i f_{t+1} + \beta_{cay} (cay_t \cdot f_{t+1}) + \varepsilon_{t+1}

