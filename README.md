# Subscription App ROAS Diagnostics

## Project Overview

This project is a marketing analytics case study for a mobile language learning app using a monthly subscription monetization model.

The app spends $100,000 per month on Meta Ads. Although top-funnel metrics such as CTR, CPI, and install volume appear stable, ROAS remains at 0.28, below the current target of 0.45.

The goal of the project is to investigate why paid acquisition is not generating enough revenue, starting from raw data validation and continuing toward KPI reconstruction, campaign diagnostics, and dashboard development.

---

## Business Problem

The company needs to understand why Meta Ads performance is under target despite stable acquisition volume.

At the current monthly spend of $100,000:

- Current ROAS: 0.28
- Target ROAS: 0.45
- Current revenue: ~$28,000
- Target revenue: ~$45,000
- Revenue gap: ~$17,000 per month

The key analytical question:

**Where does the marketing funnel break: traffic quality, platform mix, geo allocation, creative performance, or post-install monetization?**

---

## Dataset

The project uses a synthetic but business-consistent marketing dataset created for analytical practice.

The raw dataset contains user-level paid acquisition records with the following fields:

- user_id
- event_date
- platform
- country
- creative
- impressions
- clicks
- install_flag
- subscription_flag
- revenue_usd
- spend_usd

The dataset was intentionally designed to include realistic data quality issues often found in marketing analytics workflows.

---

## Project Workflow

### Stage 1 — Data Quality & Cleaning

Completed.

The raw dataset was profiled and cleaned before KPI reconstruction.

Main checks included:

- missing values
- exact duplicate rows
- invalid funnel logic
- impossible ad interaction records
- inconsistent category labels
- revenue and subscription tracking mismatches

### Stage 2 — KPI Reconstruction

Planned / In progress.

The cleaned dataset will be used to rebuild core marketing KPIs:

- CTR
- CPI
- install conversion rate
- subscription conversion rate
- CPA per subscription
- revenue
- ROAS
- budget share
- revenue share

### Stage 3 — ROAS Diagnostic Analysis

Planned / In progress.

The analysis will focus on identifying the main drivers of poor ROAS by:

- platform
- country
- creative
- funnel stage
- frequency
- monetization performance

### Stage 4 — Dashboard Development

Planned.

The final dashboard will summarize acquisition efficiency, monetization issues, and budget reallocation opportunities.

---

## Data Cleaning Summary

The raw dataset contained several structural and logical data quality issues.

| Issue | Action |
|---|---|
| 800 exact duplicate rows | Removed |
| Revenue recorded without subscription flag | Corrected when revenue matched the subscription price |
| Subscription recorded without install flag | Corrected when valid subscription revenue was present |
| Clicks greater than impressions | Removed as corrupted records |
| Negative spend values | Removed together with corrupted interaction rows |
| Inconsistent platform, country, and creative labels | Standardized |

After cleaning, the dataset became suitable for KPI reconstruction and further analysis.

---

## Initial Business Hypotheses

Based on the case context, the poor ROAS may be driven by several issues:

1. Budget may be overallocated to low-performing segments.
2. Android traffic may generate installs but weak subscription revenue.
3. Some countries may consume budget without reaching target ROAS.
4. Creative fatigue may be increasing CPI and reducing traffic quality.
5. Product monetization may be affected by weak long-term rebill retention.

These hypotheses will be tested in the next analytical stages.

---

## Expected Business Output

The final project will provide:

- a cleaned analytical dataset;
- reconstructed campaign KPIs;
- ROAS breakdown by platform, geo, and creative;
- identification of the main efficiency leaks;
- dashboard for ongoing campaign monitoring;
- actionable recommendations for budget reallocation.

---

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   │   └── marketing_raw_2025_case_ready.csv
│   └── processed/
│       └── marketing_cleaned_2025.csv
│
├── notebooks/
│   └── 01_data_cleaning.ipynb
│
├── dashboard/
│   └── dashboard_preview.png
│
├── docs/
│   └── business_case.md
│
├── README.md
└── requirements.txt

## Project Overview

This project is a marketing analytics case study for a mobile language learning app using a monthly subscription monetization model.

The app spends $100,000 per month on Meta Ads. Although top-funnel metrics such as CTR, CPI, and install volume appear stable, ROAS remains at 0.28, below the current target of 0.45.

The goal of the project is to investigate why paid acquisition is not generating enough revenue, starting from raw data validation and continuing toward KPI reconstruction, campaign diagnostics, and dashboard development.

---

## Business Problem

The company needs to understand why Meta Ads performance is under target despite stable acquisition volume.

At the current monthly spend of $100,000:

- Current ROAS: 0.28
- Target ROAS: 0.45
- Current revenue: ~$28,000
- Target revenue: ~$45,000
- Revenue gap: ~$17,000 per month

The key analytical question:

**Where does the marketing funnel break: traffic quality, platform mix, geo allocation, creative performance, or post-install monetization?**

---

## Dataset

The project uses a synthetic but business-consistent marketing dataset created for analytical practice.

The raw dataset contains user-level paid acquisition records with the following fields:

- user_id
- event_date
- platform
- country
- creative
- impressions
- clicks
- install_flag
- subscription_flag
- revenue_usd
- spend_usd

The dataset was intentionally designed to include realistic data quality issues often found in marketing analytics workflows.

---

## Project Workflow

### Stage 1 — Data Quality & Cleaning

Completed.

The raw dataset was profiled and cleaned before KPI reconstruction.

Main checks included:

- missing values
- exact duplicate rows
- invalid funnel logic
- impossible ad interaction records
- inconsistent category labels
- revenue and subscription tracking mismatches

### Stage 2 — KPI Reconstruction

Planned / In progress.

The cleaned dataset will be used to rebuild core marketing KPIs:

- CTR
- CPI
- install conversion rate
- subscription conversion rate
- CPA per subscription
- revenue
- ROAS
- budget share
- revenue share

### Stage 3 — ROAS Diagnostic Analysis

Planned / In progress.

The analysis will focus on identifying the main drivers of poor ROAS by:

- platform
- country
- creative
- funnel stage
- frequency
- monetization performance

### Stage 4 — Dashboard Development

Planned.

The final dashboard will summarize acquisition efficiency, monetization issues, and budget reallocation opportunities.

---

## Data Cleaning Summary

The raw dataset contained several structural and logical data quality issues.

| Issue | Action |
|---|---|
| 800 exact duplicate rows | Removed |
| Revenue recorded without subscription flag | Corrected when revenue matched the subscription price |
| Subscription recorded without install flag | Corrected when valid subscription revenue was present |
| Clicks greater than impressions | Removed as corrupted records |
| Negative spend values | Removed together with corrupted interaction rows |
| Inconsistent platform, country, and creative labels | Standardized |

After cleaning, the dataset became suitable for KPI reconstruction and further analysis.

---

## Initial Business Hypotheses

Based on the case context, the poor ROAS may be driven by several issues:

1. Budget may be overallocated to low-performing segments.
2. Android traffic may generate installs but weak subscription revenue.
3. Some countries may consume budget without reaching target ROAS.
4. Creative fatigue may be increasing CPI and reducing traffic quality.
5. Product monetization may be affected by weak long-term rebill retention.

These hypotheses will be tested in the next analytical stages.

---

## Expected Business Output

The final project will provide:

- a cleaned analytical dataset;
- reconstructed campaign KPIs;
- ROAS breakdown by platform, geo, and creative;
- identification of the main efficiency leaks;
- dashboard for ongoing campaign monitoring;
- actionable recommendations for budget reallocation.

---

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   │   └── marketing_raw_2025_case_ready.csv
│   └── processed/
│       └── marketing_cleaned_2025.csv
│
├── notebooks/
│   └── 01_data_cleaning.ipynb
│
├── dashboard/
│   └── dashboard_preview.png
│
├── docs/
│   └── business_case.md
│
├── README.md
└── requirements.txt
