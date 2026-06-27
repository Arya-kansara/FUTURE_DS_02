# Customer Retention & Churn Analysis
## Business Insights & Recommendations Report

**Prepared by:** Arya Kansara
**Internship:** Future Interns — Data Science & Analytics
**Task:** Task 2 — Customer Retention & Churn Analysis
**Dataset:** Telco Customer Churn Dataset
**Total Customers Analyzed:** 7,043

---

## Executive Summary

A telecom business with 7,043 customers is experiencing a **26.54% churn rate** — 
significantly above the healthy industry benchmark of 5-7%. This means 1 in 4 
customers is leaving the business. With an average customer lifetime of just 
3.8 months and a lifetime value of $246.09, the business is losing customers 
faster than it can retain them.

This analysis identifies the exact customer segments driving churn, the key 
retention drivers, and provides actionable recommendations to reduce churn 
to a sustainable level.

---

## Key Findings

### 1. Overall Churn Metrics
```
Total Customers        : 7,043
Churned Customers      : 1,869  (26.54%)
Retained Customers     : 5,174  (73.46%)
Average Churn Rate     : 26.54%
Average Lifetime       : 3.8 months
Average Monthly Charges: $64.76
Average Lifetime Value : $246.09
```

The 26.54% churn rate is the central problem.
Every percentage point of churn reduced adds
approximately $131 per customer in lifetime value.

---

### 2. Contract Type — The Biggest Driver of Churn

| Contract Type  | Customers | Churned | Churn Rate | Retention |
|---------------|-----------|---------|------------|-----------|
| Month-to-Month | 3,875    | 1,655   | 42.71%     | 57.29%    |
| One Year       | 1,473    | 166     | 11.27%     | 88.73%    |
| Two Year       | 1,695    | 48      | 2.83%      | 97.17%    |

**Insight:**
Month-to-Month customers churn at **15x the rate** of Two-Year customers.
This is the single most impactful finding in this entire analysis.
The product or service is not the problem — the contract structure is.

---

### 3. Tenure — The Danger Zone is Year 1

| Tenure Group  | Customers | Churned | Churn Rate |
|--------------|-----------|---------|------------|
| 0-12 Months  | 2,186     | 1,037   | 47.44%     |
| 13-24 Months | 1,024     | 294     | 28.71%     |
| 25-36 Months | 832       | 180     | 21.63%     |
| 37-48 Months | 762       | 145     | 19.03%     |
| 49-60 Months | 832       | 120     | 14.42%     |
| 61-72 Months | 1,407     | 93      | 6.61%      |

**Insight:**
Almost 1 in 2 new customers leaves within the first 12 months.
After Year 1, churn drops dramatically and continues falling.
If the business can retain a customer through Year 1,
they are very likely to stay long term.

---

### 4. Internet Service — Fiber Optic Problem

| Internet Service | Customers | Churned | Churn Rate |
|-----------------|-----------|---------|------------|
| Fiber Optic      | 3,096    | 1,297   | 41.89%     |
| DSL              | 2,421    | 459     | 18.96%     |
| No Internet      | 1,526    | 113     | 7.40%      |

**Insight:**
Fiber Optic is the premium, most expensive service —
yet it has the highest churn rate at 41.89%.
Premium customers are not feeling they get value for money.
This is a serious service quality or pricing issue.

---

### 5. Payment Method — Auto-Pay Makes Customers Stay

| Payment Method            | Customers | Churned | Churn Rate |
|--------------------------|-----------|---------|------------|
| Electronic Check          | 2,365    | 1,071   | 45.29%     |
| Mailed Check              | 1,612    | 308     | 19.11%     |
| Bank Transfer (automatic) | 1,544    | 258     | 16.71%     |
| Credit Card (automatic)   | 1,522    | 232     | 15.24%     |

**Insight:**
Electronic Check customers churn at **3x the rate** of auto-pay customers.
Manual payment = customer actively thinks about whether to continue.
Auto-pay = passive = customer stays by default.
Simply moving customers to auto-pay could dramatically reduce churn.

---

### 6. Senior Citizens — Disproportionately Affected

| Segment     | Customers | Churned | Churn Rate |
|------------|-----------|---------|------------|
| Senior      | 1,142    | 476     | 41.68%     |
| Non-Senior  | 5,901    | 1,393   | 23.61%     |

**Insight:**
Senior citizens churn at nearly **double the rate** of non-seniors.
Possible reasons include service complexity, price sensitivity,
or lack of dedicated senior support. This segment needs
a tailored retention approach.

---

### 7. Monthly Charges — Higher Price = Higher Churn

| Charge Group  | Customers | Churned | Churn Rate |
|--------------|-----------|---------|------------|
| High (>$65)   | 3,899    | 1,354   | 34.73%     |
| Medium ($36-65)| 1,409   | 326     | 23.14%     |
| Low (≤$35)    | 1,735    | 189     | 10.89%     |

**Insight:**
High-paying customers churn 3x more than low-paying customers.
These are the most valuable customers to retain —
losing them hurts revenue the most.

---

## Cohort Analysis Findings

### Worst Performing Cohort
```
Tenure  : 0-12 Months
Contract: Month-to-Month
Churn   : 51.35%

Translation: More than HALF of new monthly
customers leave within their first year.
This is a business emergency.
```

### Best Performing Cohort
```
Tenure  : 0-12 Months
Contract: Two Year
Churn   : 0.00%

Translation: Not a single new customer
on a Two-Year contract left.
Contract type completely eliminates early churn.
```

### Retention Pattern
```
The longer a customer stays → the less likely they leave

Month-to-Month retention improves from 48% to 78% over 6 years
One Year retention stays consistently above 86%
Two Year retention stays consistently above 96%

Key takeaway: Survive Year 1 = Customer stays forever
```

---

## Critical Insight 🚨

**This business does not have a product problem. It has a contract and onboarding problem.**

The evidence:
- Two-Year contract customers churn at only 2.83% 
- Same customers, same product, same price range
- Only difference is contract length
- Customers who commit long-term almost never leave

This means the product is good enough to retain customers.
The business just needs to get customers to commit longer
and survive the critical first 12 months.

---

## Recommendations

### 🚨 Critical — Fix Immediately

**1. Convert Monthly Customers to Long-Term Contracts**
```
Problem  : Month-to-Month churn = 42.71%
           Two-Year churn = 2.83%
Action   : Offer 20-30% discount for annual signup
           Make Two-Year plan the highlighted/default option
           Show clear savings comparison during onboarding
Impact   : Could reduce overall churn by 10-15 percentage points
```

**2. Build a First-Year Retention Program**
```
Problem  : 47.44% of new customers leave within Year 1
Action   : Dedicated onboarding program for new customers
           Monthly check-in calls in first 6 months
           Special loyalty reward after 6 months milestone
           Early warning system for disengaged customers
Impact   : Reducing Year 1 churn by 50% would save ~500 customers
```

---

### ⚠️ Important — Fix Within 3 Months

**3. Investigate and Fix Fiber Optic Issues**
```
Problem  : Fiber Optic churn = 41.89% vs DSL = 18.96%
Action   : Audit Fiber Optic speed and quality complaints
           Compare pricing vs competitors in same market
           Consider service credits for long-term customers
           Proactive quality checks for Fiber customers
Impact   : Fiber Optic has 3,096 customers — fixing this
           has the highest volume impact of any action
```

**4. Move Customers to Automatic Payment**
```
Problem  : Electronic Check churn = 45.29%
           Auto-pay churn = 15-17%
Action   : Offer $5-10 monthly discount for switching to auto-pay
           Send targeted campaign to all Electronic Check users
           Make auto-pay the default option during signup
Impact   : 2,365 customers on Electronic Check
           Moving them to auto-pay could save 700+ customers
```

---

### 💡 Opportunity — Plan for Next 6 Months

**5. Senior Citizen Retention Program**
```
Problem  : Senior churn = 41.68% vs 23.61% for non-seniors
Action   : Dedicated senior customer support line
           Simplified plan options for senior segment
           Technology assistance program
           Partner with senior community organizations
Impact   : 1,142 senior customers — specialized care
           could bring churn in line with non-seniors
```

**6. Premium Customer Retention Program**
```
Problem  : High charge customers churn at 34.73%
Action   : VIP support tier for high-paying customers
           Proactive outreach before renewal
           Exclusive benefits for premium plan customers
Impact   : High-value customers lost = highest revenue impact
           Retaining even 10% more = significant CLV gain
```

---

## Impact Summary

If all recommendations are implemented:

```
Current Churn Rate     → 26.54%
Realistic Target       → 12-15% within 12 months

Current Avg Lifetime   → 3.8 months
Expected Avg Lifetime  → 6-7 months

Current Avg CLV        → $246.09
Expected Avg CLV       → $400-450

For 7,043 customers:
Current Annual Revenue → ~$5.47M
Expected Revenue Gain  → ~$1.08M additional annually
```

---

## Conclusion

The business is losing 1 in 4 customers primarily due to 
three fixable problems: short-term contract structure, 
poor first-year retention, and payment friction.

The good news is that customers who commit to longer 
contracts almost never leave — proving the product works. 
The opportunity is in getting customers to that commitment 
point and supporting them through the critical first year.

Addressing contract conversion and first-year retention 
alone could cut churn in half within 12 months, 
adding over $1M in annual revenue without acquiring 
a single new customer.

