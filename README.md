# Revisiting the Consumption-based CAPM in India  
### A Conditional Approach Using the Consumption–Wealth Ratio (cay)

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

### 🧑‍💻 Authors  
**Tanishq Gupta**, **Sourabh Hukkeri**, **Tushar Singh**  
*Department of Humanities and Social Sciences, Indian Institute of Technology Roorkee*  
📅 *October 2025*

---

## 📘 Overview  

This repository presents our replication and extension of the seminal paper:  
> **Lettau, M., & Ludvigson, S. (2001)**. *Resurrecting the (C)CAPM: A Cross-Sectional Test When Risk Premia Are Time-Varying.* *Journal of Political Economy, 109*(6), 1238–1287.  

We investigate whether the **poor empirical performance of CAPM and C–CAPM** in asset pricing arises from **ignoring time-varying risk premia**, and whether conditioning on the **consumption–wealth ratio (cay)** enhances explanatory power — specifically in the **Indian financial market**.

---

## 🎯 Research Objectives  

- Examine if **risk premia** in Indian markets vary with macroeconomic conditions.  
- Construct an **Indian proxy for the consumption–wealth ratio (cay)**.  
- Test and compare performance of:
  - Classical **CAPM**
  - **Consumption-based CAPM (C–CAPM)**
  - **Scaled (Conditional) models** using cay  
  - **Fama–French Three-Factor Model**

---

## 🧠 Motivation  

Conventional CAPM assumes constant risk premia — but in reality, **investors’ risk aversion and wealth expectations change over time**.  
This motivates a **conditional framework**, where risk premia vary with a state variable — **the consumption–wealth ratio (cay)** — that captures deviations of consumption from its long-run relation with wealth and income.  

---

## 📊 Data Description  

| Category | Variable | Frequency | Source |
|-----------|-----------|-----------|---------|
| Consumption | PFCE (nondurables + services) | Quarterly | MOSPI |
| Asset Wealth | Household Net Worth (proxy) | Quarterly | RBI |
| Labor Income | Wages + Self-employment Income | Quarterly | National Accounts |
| Market Returns | 25 Size × Book-to-Market Portfolios | Monthly / Quarterly | NSE / CMIE Prowess |
| Risk-Free Rate | 91-day Treasury Bill | Quarterly | RBI |

📁 *All cleaned datasets and sources are available under the `/data/` directory.*

---

## ⚙️ Methodology  

### 1️⃣ Constructing the Consumption–Wealth Ratio (cay)

The long-run equilibrium relation among log consumption *(cₜ)*, asset wealth *(aₜ)*, and labor income *(yₜ)* is estimated as:

$$
c_t = \alpha + \beta_a a_t + \beta_y y_t + u_t
$$

The stationary residual *(uₜ)* represents:

$$
cay_t = c_t - \hat{\alpha} - \hat{\beta_a} a_t - \hat{\beta_y} y_t
$$

---

### 2️⃣ Time-Series Estimation

For each portfolio *i*, estimate:

$$
R_{i,t+1} = \alpha_i + \beta_{i1} f_{t+1} + \beta_{i2}(cay_t f_{t+1}) + \varepsilon_{i,t+1}
$$

where *fₜ₊₁* represents the factor (consumption growth or market return).

---

### 3️⃣ Cross-Sectional (Fama–MacBeth) Regression

$$
E[R_i] = \gamma_1 \hat{\beta}_{i1} + \gamma_2 \hat{\beta}_{i2} + \eta_i
$$

- Compute risk prices (γ₁, γ₂)  
- Apply **Shanken correction**  
- Compare **R²** and **pricing errors** across models  


---

<!-- 
### 4️⃣ Model Comparison  

| Model | Scaled by cay? | Key Variable | Expected Outcome |
|--------|----------------|---------------|------------------|
| CAPM | ❌ | Market Return | Poor fit |
| C–CAPM | ❌ | Consumption Growth | Limited explanatory power |
| Conditional CAPM | ✅ | cay × Market Return | Improved R² |
| Conditional C–CAPM | ✅ | cay × Consumption Growth | Comparable to Fama–French |
| Fama–French (3-Factor) | — | SMB, HML, MKT | Benchmark |

-->


---

## 📈 Key Findings  

- **Unconditional CAPM/C–CAPM**: Very low explanatory power in India.  
- **Scaled (Conditional) Models**: Dramatic improvement in fit and significance.  
- **Conditional C–CAPM** explains ~70% of cross-sectional variation — close to **Fama–French (80%)**.  
- **Economic insight:** When consumption is low relative to wealth (high cay), investors demand higher expected returns → risk premia are state-dependent.  

---

## 🧩 Repository Structure  


---

## 📚 References  

1. Lettau, M., & Ludvigson, S. (2001). *Resurrecting the (C)CAPM: A Cross-Sectional Test When Risk Premia Are Time-Varying.* *Journal of Political Economy, 109*(6), 1238–1287.  
2. Fama, E. F., & French, K. R. (1993). *Common Risk Factors in the Returns on Stocks and Bonds.* *Journal of Financial Economics, 33*(1), 3–56.  
3. Agarwalla, S. K., Jacob, J., & Varma, J. R. (2014). *Four-Factor Model in Indian Equities Market.*  
4. Bajpai, S., & Sharma, A. K. (2015). *Empirical Testing of CAPM in India.* *Procedia – Social and Behavioral Sciences, 189*, 259–265.

---

## 🧾 License  

This project is released under the **MIT License** – you’re free to use, modify, and distribute this work with proper attribution.

---

## 🌟 Acknowledgements  

This project was completed as part of the **Financial Economics coursework** under the *Department of Humanities and Social Sciences, IIT Roorkee*.  
Special thanks to the course instructors and peers for insightful feedback and discussions.

---

## 💡 Key Takeaway  

> *Time variation matters.*  
> Conditioning on macroeconomic information — like the consumption–wealth ratio — can **resurrect** the classic CAPM framework and bring it closer to empirical reality.

---

