# Strategic Market Analysis - Conagra's Gardein 🥬

> **UT Dallas MSBA capstone (Group 7)** - A strategic analytics case study on Conagra's Gardein brand in the U.S. frozen meat-substitute category. Benchmarks **Gardein vs Morningstar Farms** and the broader competitive set using multi-year retail POS data, **multivariate regression** on dollar sales, and geographic opportunity mapping.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![statsmodels](https://img.shields.io/badge/statsmodels-8CAAE6?style=flat)
![Category-CPG](https://img.shields.io/badge/Category-CPG%20%2F%20Frozen-green?style=flat)

> **📄 Deliverables:** 🔗 [**Final Report (PDF)**](./FINAL%20REPORT.pdf) · 🔗 [**Executive Deck (PPTX)**](./Group_7.pptx)

---

## 🎯 Business Question

Gardein sits in a crowded and rapidly shifting plant-based frozen category. Management needed to understand:

1. **Where is Gardein winning and losing** relative to Morningstar Farms and the broader competitive set?
2. **Which product and pricing levers** (pack size, price per unit, distribution, meat source, flavor) most influence dollar sales?
3. **Which U.S. geographies** offer the strongest growth opportunity - and why?

## 🔍 Approach

| Stage | Methods |
|---|---|
| **Data** | Multi-year retail POS extracts for Gardein, Morningstar Farms, and competitor brands (Nielsen-style syndicated data format) |
| **Cleaning** | Missing-value treatment, duplicate checks, column pruning |
| **Feature engineering** | Parsed product description strings → franchise, meat source, product type, flavor, pack size (ounces) |
| **EDA** | Univariate + bivariate distributions; category and sub-segment share |
| **Multicollinearity** | VIF review, consolidation / removal of collinear predictors |
| **Modeling** | Multivariate OLS regression on dollar sales with controls for distribution (ACV), price, pack size, product, brand, meat source, and geography |
| **Geographic analysis** | Regional cuts (California, Northeast, Total US Multi-Outlet + Convenience) aligned to regression region effects |

## 📊 Key Findings *(see the [Final Report](./FINAL%20REPORT.pdf) for details)*

*High-level takeaways - for full coefficients, significance tests, and recommendations, see the PDF report and slide deck.*

- Dollar sales are driven most strongly by **ACV-weighted distribution** and **price per unit**, with meaningful secondary effects from **pack size** and **product type**.
- **Gardein vs Morningstar Farms** positioning diverges on health messaging, ingredient innovation, and sustainability - each with distinct implications for shelf strategy.
- Regional performance shows asymmetric opportunity: certain geographies over-index on the category but under-index on Gardein, flagging clear white-space for distribution expansion.

---

## 🖼️ Visuals

> *Export 2–3 key charts (market share, regression coefficient plot, geographic map) from the notebooks or slide deck into a `docs/images/` folder and reference them here. Placeholders removed until real exports are added so the README doesn't show broken image icons.*

<!-- Example, once you add real files:
<p align="center">
  <img src="./docs/images/market_share.png" alt="Category share Gardein vs competitors" width="80%" />
</p>
-->

---

## 👥 Team (Group 7)

Ashish Patil · **Isha Narkhede** · Javed Mohammed · Neha Govekar · Pallavi Sawant · Raj Nathwani

### 👤 My contribution (Isha)

*[Fill this section in - recruiters specifically look for it on team projects. A few concrete sentences on what you personally owned is far stronger than silence. Examples of angles to cover:]*

- *What workstream did you lead or co-lead? (e.g., "Led the regression modeling and feature engineering from product description strings")*
- *What technical pieces are yours? (e.g., "Built the VIF diagnostics and final OLS specification in `reg.ipynb`")*
- *What did you present? (e.g., "Authored the geography slides in the final deck and the corresponding section of the written report")*

---

## 📁 Repository Contents

| File | What it is |
|---|---|
| [`FINAL REPORT.pdf`](./FINAL%20REPORT.pdf) | **Written report** - objectives, EDA, regression results, recommendations (main deliverable) |
| [`Group_7.pptx`](./Group_7.pptx) | **Executive slide deck** - summarized findings for presentation |
| `reg.ipynb` | Regression modeling notebook - feature engineering, VIF, OLS fit, diagnostics |
| `Geography_based_visualization.ipynb` | Regional analysis notebook - geography cuts, multi-year panels, maps |
| `2023_MorningStar_Gardein.xlsx` | Competitor POS data - Morningstar Farms + Gardein |
| `2023_Other_Brand_Data.xlsx` | Broader category POS data - other competing brands |

## ⚙️ Reproducing the Analysis

```bash
# Create a virtual environment
python -m venv .venv
source .venv/bin/activate        # macOS / Linux
# .venv\Scripts\activate         # Windows

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter openpyxl scipy statsmodels

# Open the notebooks
jupyter notebook
```

The notebooks expect the Excel files in the same directory. If your copies live elsewhere, update the `pd.read_excel(...)` paths at the top of each notebook.

## 🔒 Data Note

The POS extracts included here are syndicated retail data shared for coursework. Before forking or redistributing:

- Confirm redistribution is permitted under the original data license
- Consider replacing with aggregated / synthetic samples for public demo purposes
- Clear notebook outputs (`Cell → All Output → Clear`) if any contain internal identifiers

This repository is an **academic / course deliverable**. It is not an official Conagra or Gardein publication and the findings should not be interpreted as company positions.

## 📬 Contact

**Isha Narkhede** · [Portfolio](https://isha-n-portfolio.netlify.app/) · [LinkedIn](https://linkedin.com/in/isha-narkhede) · ishajayant207@gmail.com
