# US Healthcare Cost & Demographics Analysis (Excel)

## Overview
The US healthcare department shared admission data for 10,000 patients, covering demographics, admission details, and insurance/billing information. This project cleans the raw data and analyzes it entirely in Microsoft Excel to answer three core business questions for hospital leadership.

* **Tools used:** Microsoft Excel (data auditing, SUMIFS/COUNTIFS/AVERAGEIFS formulas, PivotTable-style summary tables, native charts)

---

## Problem Statement
Analyzing the Impact of Demographics and Admission Types on Healthcare Costs and Outcomes:
1. **Demographic Analysis** — Which medical conditions are most prevalent across specific patient groups.
2. **Patient Price Optimization** — Key drivers of billing amounts and strategies for patient cost reduction.
3. **Hospital Resource Management** — Admission-type trends over time to optimize workload and staffing planning.

---

## Data Cleaning
The raw export (10,000 rows × 26 columns) contained several real-world data quality issues, all logged and remediated:
* **Typos:** Fixed invalid values (e.g., `"8I"` → `81` in Age).
* **Character Errors:** Fixed digit/letter confusion in Billing Amount (e.g., `"6452O"` → `64520`).
* **Inconsistent Categorization:** Standardized categories (e.g., `"ARTHRITIS"` → `Arthritis`, `"Emer"` → `Emergency`, `"M"` → `Male`).
* **Mixed Date Formats:** Standardized inconsistent date strings (e.g., `"Wednesday, 6 October 2021"` and `06/10/21`).
* **Missing Data Imputation:** Imputed 24 blank Billing Amount values using average billing segmented by Medical Condition + Admission Type.

*Full before/after log is available on the **Data Quality Log** tab of the workbook.*

---

## Key Findings
* **Demographics:** Hypertension is the most prevalent condition overall and skews strongly male; Obesity skews female. Seniors (ages 66–85) carry the heaviest overall condition burden.
* **Pricing Drivers:** Medical Condition is the primary billing driver — Cancer patients average ~3x higher billing than Obesity patients. Insurance provider and age group show minimal impact on average billing amounts.
* **Resource Management:** Emergency and Urgent admissions average ~55% longer stays than Elective admissions. Monthly admission volume remains consistent throughout the year without pronounced seasonal spikes.

---

## Workbook Structure
`US_Healthcare_Case_Study.xlsx` consists of 8 organized tabs:
* `Overview` & `Executive Summary`
* `Raw Data`, `Data Quality Log`, and `Clean Data`
* 3 analysis tabs (1 per business question) containing formula-driven summary tables and visual charts.
