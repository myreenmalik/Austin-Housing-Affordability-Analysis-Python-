# 🏠 Austin Housing Affordability Analysis

An analysis of rent burden across census tracts in Travis County, Texas using 2022 American Community Survey (ACS) data from the U.S. Census Bureau.

---

## Overview

This project examines housing affordability in Austin by calculating **rent burden** — the percentage of household income spent on rent — across 260 census tracts in Travis County. The goal is to identify which neighborhoods are most cost-burdened and what factors drive affordability gaps.

---

## Key Findings

| Metric | Result |
|---|---|
| Total census tracts analyzed | 260 |
| Cost-burdened tracts (>30% of income on rent) | 33 (12.7%) |
| Most burdened tract | Census Tract 6.08 — 406% rent burden |
| Income-burden correlation | r = -0.401, p < 0.001 |
| Model R² (income + rent → burden) | 0.118 |

> **Notable:** A cluster of East Austin tracts (6.01, 6.05–6.08) show extreme rent burden, with Tract 6.08 at over 400% — meaning median rent exceeds annual median income.

---

## Visualizations

- Distribution of rent burden across all Travis County tracts
- Median rent vs. median income scatterplot by tract
- Top 10 most rent-burdened tracts (bar chart)

---

## Methods

- Data cleaning and reshaping with **pandas**
- Rent burden calculation: `(median_rent × 12) / median_income`
- Pearson correlation analysis with **scipy**
- Linear regression model with **scikit-learn**
- Visualizations with **matplotlib**

---

## Data Sources

- [ACS 5-Year Estimates 2022 — Median Gross Rent (B25064)](https://data.census.gov/table/ACSDT5Y2022.B25064?g=050XX00US48453$1400000)
- [ACS 5-Year Estimates 2022 — Median Household Income (B19013)](https://data.census.gov/table/ACSDT5Y2022.B19013?g=050XX00US48453$1400000)

---

## Setup

```bash
pip install pandas matplotlib seaborn scipy scikit-learn
```

Then open `analysis.ipynb` in VS Code, Cursor, or Jupyter and run all cells.

---

*Data sourced from the U.S. Census Bureau. Analysis conducted in Python.*
