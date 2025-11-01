# 📓 Notebooks

This folder contains the main Jupyter Notebook for the project, along with an additional notebook focused on visualization and summary reporting.

## 🗂 Contents

| File | Description |
|------|-------------|
| `CCAPM_India_Replication.ipynb` | Main notebook containing the full workflow: <br>• Data loading and preprocessing <br>• Construction of the Indian `cay` variable <br>• CAPM, C-CAPM, and scaled factor model estimation <br>• Fama–MacBeth cross-sectional regressions <br>• Result analysis and visualizations |
| `Return_Plots.ipynb` | Standalone notebook used for generating plots and summary tables. Includes state-dependent beta analysis (`βᴳ`, `βᴮ`, `βᴳ − βᴮ`) for the six Fama–French portfolios, along with interpretation text for reporting. Can be run independently without re-estimating the full model. |

## 🚀 Usage

1. Ensure the `data/` and `fama-french-portfolios/` folders are present at the repository level.
2. Run `CCAPM_India_Replication.ipynb` to reproduce the full analysis end-to-end.
3. Run `return_plots.ipynb` **only if you need visualizations or the summary table** — it loads pre-computed beta outputs and does not require re-running the full model.
