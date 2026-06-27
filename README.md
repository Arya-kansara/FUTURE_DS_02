# FUTURE_DS_02 — Customer Retention & Churn Analysis

## 📌 Project Overview
This project analyzes customer churn data for a telecom business to identify 
why customers are leaving, which segments are most at risk, and what actions 
can reduce customer loss. Completed as **Task 2** of the Data Science & 
Analytics Internship at **Future Interns**.

---

## ❓ Problem Statement
The business is experiencing a **26.54% churn rate** — meaning 1 in 4 customers 
is leaving. With an average customer lifetime of just 3.8 months and a lifetime 
value of $246.09, the business needed answers to:

- Why are customers leaving?
- Which customer segments churn the most?
- Does contract type, payment method, or service type affect churn?
- How long do customers typically stay before leaving?
- What can the business do RIGHT NOW to reduce churn?

Without structured analysis, the business had no clear picture of WHO was 
leaving or WHY — making it impossible to take targeted action.

---

## ✅ Solution Approach
A three-stage analysis was performed:

1. **Python (Pandas)** — Loaded, cleaned, and prepared the raw dataset.
   Engineered new features including Churn_Flag (0/1), Tenure Groups,
   Charge Groups, and Senior Citizen labels for better analysis.

2. **Cohort Analysis (Python)** — Grouped customers by tenure and contract
   type to identify retention patterns over time. Built a cohort table
   showing churn rates across 18 different customer segments.

3. **Power BI** — Built a 3-page interactive dashboard covering overall
   churn metrics, customer segmentation, and cohort retention analysis.
   Final insights and recommendations written as a client-ready report.

---

## 🛠️ Tools Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn) — data cleaning,
  feature engineering, cohort analysis, visualization
- **Power BI** — interactive 3-page churn dashboard
- **Jupyter Notebook** — step-by-step analysis documentation
- **GitHub** — version control and public portfolio submission

---

## 🧹 Data Cleaning Summary
- Dataset: 7,043 customers, 21 columns
- Verified 0 missing values and 0 duplicate rows
- Fixed TotalCharges column (stored as object → converted to float)
- Converted Churn column (Yes/No → 1/0) for mathematical calculations
- Created Tenure_Group column (0-12, 13-24, 25-36, 37-48, 49-60, 61-72 months)
- Created Charge_Group column (Low ≤$35, Medium $36-65, High >$65)
- Converted SeniorCitizen (0/1 → Non-Senior/Senior) for readability
- Exported cleaned dataset as cleaned_churn_data.csv

Full cleaning steps available in `notebooks/churn_analysis.ipynb`

---

## 📊 Cohort Analysis Summary
Grouped customers by Tenure Group × Contract Type to track retention:

| Worst Cohort | Best Cohort |
|-------------|------------|
| 0-12 Months + Month-to-Month | 0-12 Months + Two Year |
| 51.35% Churn Rate 🚨 | 0.00% Churn Rate ✅ |

Same new customers. Same time period.
Contract type alone determines whether they stay or leave.

---



## 📊 Dashboard Preview

### Page 1 — Churn Overview
<img width="820" height="461" alt="Customer_Retention and Churn Analysis" src="https://github.com/user-attachments/assets/8b0c63ff-0e4f-477d-806b-439e9df7dc44" />

KPI cards (Total Customers, Churned, Retained, Churn Rate, Avg Lifetime),
Churn vs Retained donut, Churn by Contract Type, Churn by Tenure Group,
Churn by Payment Method.

### Page 2 — Customer Segmentation Analysis
<img width="830" height="469" alt="Customer_Segmentation" src="https://github.com/user-attachments/assets/57bfeb63-7bb0-4958-9edb-df419a154476" />
Churn by Internet Service, Senior vs Non-Senior churn,
Churn by Monthly Charge Group, Churn by Gender.

### Page 3 — Cohort & Retention Analysis
<img width="831" height="458" alt="cohort   retention" src="https://github.com/user-attachments/assets/f37d1ea6-6b26-4bb9-98d3-fd14b550129a" />
Retention Rate by Contract across Tenure (Line Chart),
Churn Rate by Tenure & Contract (Clustered Bar),
Overall Churn Trend across Tenure (Line Chart).

---

## 🔍 Key Insights (Summary)

- Overall churn rate is **26.54%** — 1 in 4 customers leaving
- **Month-to-Month contracts** drive the most churn (42.71%)
  vs Two-Year contracts at just 2.83% — a 15x difference
- **First 12 months** is the critical danger zone — 47.44% churn rate
  drops to just 6.61% for customers who reach 61-72 months
- **Fiber Optic** customers churn at 41.89% despite paying premium prices
- **Electronic Check** payment customers churn at 45.29% vs 15-17%
  for automatic payment customers
- **Senior citizens** churn at 41.68% — nearly double the 23.61%
  rate for non-seniors

📄 Full findings, cohort analysis, and recommendations:
[business_insights.md]
---

## 💡 Top Recommendation

> Convert Month-to-Month customers to longer contracts.
> Two-Year contract customers churn at 0% in their first year.
> The product works — customers just need to commit longer.

