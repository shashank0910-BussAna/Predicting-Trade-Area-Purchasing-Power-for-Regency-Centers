# Predicting Trade Area Purchasing Power for Regency Centers

## Overview
This project builds a predictive analytics model to estimate trade area purchasing power for Regency Centers, a leading owner and operator of grocery-anchored shopping centers across the United States. The goal was to shift from descriptive demographic analysis to a data-driven predictive framework that supports investment, leasing, and development decisions.

## Business Problem
Regency Centers evaluates trade areas using demographic indicators but lacked a predictive model to forecast future purchasing power. This project closes that gap by building machine learning models that estimate purchasing power across 445 trade areas and rank them by retail potential.

## Dataset
- **Source:** Regency Centers proprietary demographic dataset
- **Size:** 445 trade areas (cleaned from 530 records)
- **Variables:** Median Household Income, Population, Daytime Population, Total Households, Average Home Value, Education Attainment, Five-Year Income Growth, Household Growth
- **Geographic Coverage:** West, Northeast, Southeast, Central, and Mid-Atlantic divisions

## Methodology
1. **Exploratory Data Analysis** — Descriptive statistics and geographic distribution analysis
2. **Pearson Correlation Analysis** — Identified population (r = 0.931) as the primary driver of purchasing power
3. **Principal Component Analysis (PCA)** — PC1 explained 37.6% of portfolio variance; built a Purchasing Power Index (PPI)
4. **VIF-Based Variable Selection** — Resolved severe multicollinearity (Total Households VIF = 85.3)
5. **Machine Learning Models:**
   - Linear Regression (baseline)
   - Random Forest (200 trees)
   - Gradient Boosting (200 estimators)

## Results
| Model | Test R² | MAE |
|-------|---------|-----|
| Linear Regression | 0.91+ | — |
| Random Forest | 0.91+ | — |
| **Gradient Boosting** | **0.936** | **0.163 PPI units** |

- Population accounts for **93.8% to 97.8%** of predictive power across ensemble models
- Total portfolio purchasing power: **$6.21 trillion** across 445 trade areas
- West and Northeast divisions lead in aggregate purchasing power ($1.645T and $1.515T)

## Dashboard
An interactive **Python Dash dashboard** was developed featuring:
- 18 charts
- 7 KPI cards
- Business-ready interface for investment and leasing teams

## Tools & Technologies
- Python (Pandas, Scikit-learn, Dash, Matplotlib)
- Machine Learning (Random Forest, Gradient Boosting, PCA)
- Statistical Analysis (Pearson Correlation, VIF, Multiple Regression)

## Team
Developed as part of CEN6940 Computing Practicum at the University of North Florida (Spring 2026) by a team of 6 students.

## Key Takeaway
Market size (population) — not per-household income — is the primary driver of aggregate retail purchasing capacity, accounting for nearly 94-98% of predictive power across all models.
