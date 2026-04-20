# Gardein growth analytics — meat substitute market intelligence

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org/)

Strategic analytics project for **Conagra’s Gardein** brand in the U.S. **frozen meat substitute** category. Using multi-year retail-style POS data, we benchmark **Gardein vs Morningstar Farms** (and the broader competitive set), run **exploratory and bivariate analysis**, engineer features from product text, and fit **multivariate regression** models to explain **dollar sales** and highlight **geographic** opportunities.

> **Disclaimer:** This repository contains academic / course-style analytics and narrative deliverables. It is **not** an official Conagra or Gardein publication. Insights are for learning and portfolio use unless separately authorized.

---

## Highlights

| Theme | What we did |
|--------|-------------|
| **Market structure** | Compared category and sub-segment share (e.g. original “meat source” flavour mix vs plant-based substitutes). |
| **Competitive intelligence** | Synthesized positioning patterns (health messaging, sustainability, ingredient innovation, partnerships). |
| **Modeling** | Multivariate regression on dollar sales with distribution, price, pack size, product, brand, meat source, and geography; assessed fit and key coefficients. |
| **Geography** | Regional deep dives and visualizations to align sales performance with regression-based regional effects. |

---

## Visuals (placeholders — add your exports)

Replace the paths below with images in a folder such as `docs/images/` after you export charts from the notebooks or slides.

<!-- Screenshot: executive summary or key market-share chart -->
![Market share overview](docs/images/PLACEHOLDER_market_share.png)

<!-- Screenshot: regression / model summary or coefficient plot -->
![Model summary](docs/images/PLACEHOLDER_regression_summary.png)

<!-- Screenshot: map or regional sales visualization -->
![Geographic analysis](docs/images/PLACEHOLDER_geography.png)

**Tip:** Keep images **under ~1–2 MB** each for fast GitHub loading; use PNG for slides, WebP if you optimize.

---

## Repository layout

| Path | Description |
|------|-------------|
| `Univariate Analysis - Predictive Modeling -2024.ipynb` | Univariate exploration and predictive modeling workflow on category data. |
| `Geography_based_visualization.ipynb` | Regional filters and geography-focused charts (multi-year panels). |
| `Geography_based_visualization (1).ipynb` | Alternate copy of the geography notebook (clean up duplicates before sharing if desired). |
| `reg (1).ipynb` | Regression-focused notebook. |
| `FINAL GROUP 7.docx` | Written report (objectives, EDA, regression, recommendations). |
| `Group_7.pptx` | Executive slide deck. |
| `*.xlsx` | Supporting spreadsheets (Morningstar / other brand extracts — **large files**; see Data note below). |

---

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows
pip install pandas numpy matplotlib seaborn jupyter openpyxl scipy statsmodels
jupyter notebook
```

> Notebooks reference **specific Excel filenames** (e.g. frozen substitute meat POS extracts). Place those files in the same directory as the notebook, or update `pd.read_excel(...)` paths.

---

## Data & privacy

- Source files can be **large** and may be **confidential**. Before pushing to GitHub:
  - Prefer a **public sample** (aggregated or synthetic) **or**
  - Keep raw data **local only** and document what columns are expected in this README **or**
  - Use [Git LFS](https://git-lfs.github.com/) for large binaries if you must version them.
- Remove IDs, internal-only paths, or credentials if any appear in notebook outputs (clear outputs: *Cell → All Output → Clear*).

---

## Key methods (short)

1. **Cleaning:** Missing values, duplicate checks, dropping low-value columns.  
2. **Feature engineering:** Parsed product strings for franchise, meat source, product type, flavour, pack ounces (ounces).  
3. **Multicollinearity:** Variance Inflation Factor (VIF) review; consolidate or drop highly correlated predictors.  
4. **Regression:** Dollar sales as a function of pack size, price per unit, ACV-weighted distribution, geography, product, brand, meat source (reference levels documented in the report).  
5. **Geo EDA:** Cuts by Nielsen-style geographies (e.g. California, Northeast, Total US multi-outlet + convenience).

---

## Team (Group 7)

Ashish Patil · **Isha Narkhede** · Javed Mohammed · Neha Govekar · Pallavi Sawant · Raj Nathwani  

---

## License

Add a `LICENSE` file for any code you own (e.g. MIT). **Notebook outputs and underlying POS extracts** may be subject to school or partner terms—only publish what you are allowed to redistribute.
