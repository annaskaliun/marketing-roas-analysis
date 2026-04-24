# Subscription App ROAS Diagnostics

## Project Overview

Meta Ads spend: **$100,000/month**  
Current ROAS: **0.28**  
Target ROAS: **0.45**

The account was generating stable installs, with no obvious decline in CTR or CPI. However, revenue efficiency remained below target.

The objective was to identify why stable acquisition volume was not converting into enough subscription revenue and to determine which segments were responsible for the ROAS gap.

---

## Business Problem

At the current spend level, the app generates about **$28,000** in revenue, while the target ROAS requires about **$45,000**.

This creates a monthly revenue gap of approximately **$17,000**.

The analysis focuses on finding the source of this gap across:

- platform performance
- geo allocation
- creative efficiency
- funnel conversion
- post-install monetization

---

## Dataset

The `data/` folder contains two dataset versions:

- `raw/marketing_raw_2025_case_ready.csv` — raw, unprocessed user-level acquisition data;
- `processed/marketing_cleaned_2025.csv` — cleaned dataset prepared for KPI reconstruction and analysis.

Main fields include acquisition dimensions, funnel flags, revenue, and ad spend.

---

## Project Workflow

### Stage 1 — Data Quality & Cleaning

**Status:** Completed ✅ 
**Tool used:** Python / pandas

The raw dataset was profiled and cleaned before KPI reconstruction.

Main checks included:

- missing values;
- exact duplicate rows;
- invalid funnel logic;
- impossible ad interaction records;
- inconsistent category labels;
- revenue and subscription tracking mismatches.

A detailed step-by-step report is available in the `notebooks/` folder.

### Stage 2 — KPI Reconstruction  

Planned / In progress. 🟡

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

Planned / In progress. 🟡

The analysis will focus on identifying the main drivers of poor ROAS by:

- platform
- country
- creative
- funnel stage
- frequency
- monetization performance

### Stage 4 — Dashboard Development 

Planned. ⏳

The final dashboard will summarize acquisition efficiency, monetization issues, and budget reallocation opportunities.

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
