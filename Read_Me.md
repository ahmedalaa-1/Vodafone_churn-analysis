# 📶 Vodafone Customer Churn Analysis

> A Power BI dashboard analyzing customer churn behavior for Vodafone,
> covering contract types, tenure, services, customer profile, and
> payment methods to identify the key drivers of churn.

---

## 📌 Project Overview

This project analyzes customer churn for Vodafone using customer
account, service subscription, and billing data.

The dashboard focuses on understanding who churns, why they churn,
and which customer segments carry the highest churn risk.

The analysis helps identify the customer segments associated with:

- High churn rate
- Short tenure / early-life churn risk
- Low service adoption (Tech Support, Online Security, etc.)
- Disproportionate revenue loss

---

## 🎯 Business Questions

The analysis aims to answer the following questions:

- What is the overall churn rate and how much revenue does it cost?
- Which contract types and tenure groups churn the most?
- How does churn rate change as tenure increases?
- Which services (Tech Support, Internet Service Type, Online Security, etc.) are linked to higher churn?
- How do contract type and tenure interact with churn (cross-analysis)?
- Does subscribing to Tech Support reduce churn for Fiber Optic customers?
- Which customer profile and payment method segments churn the most?

---

## 🗂️ Dataset

The dataset contains customer account, subscription, service,
and payment-related information.

### Main Data Areas

| Data Area | Description |
|---|---|
| Customer Account | Contract type, tenure, senior citizen status, dependents |
| Services | Phone Service, Internet Service Type, Online Security, Online Backup, Tech Support |
| Billing | Monthly Charges, Total Charges, Paperless Billing, Payment Method |
| Churn | Churn flag used to calculate churn rate and revenue lost |

---

## 🛠️ Tools & Technologies

- Power BI
- DAX
- Power Query
- Data Modeling
- Dashboard Design
- Data Analysis
- Data Visualization

---

# 🔄 Data Preparation

The data was prepared and structured for analysis by:

- Reviewing data quality and consistency
- Grouping customers into Tenure Groups (0-15, 15-30, 30-45, 45-60, more than 60)
- Calculating churn KPIs (Churn Rate, Lost Revenue %)
- Building DAX measures for churned customers, churn rate, and revenue lost
- Preparing cross-analysis tables (Tenure × Tech Support, Tenure × Contract Type)
- Preparing data for the dashboard visualizations

---

# 📊 Dashboard

The dashboard consists of **4 analytical pages**:

1. Churn Overview
2. Services & Customer Experience
3. Customer Profile & Payment
4. Cross-analysis & Customer Segmentation

---

# 📄 Page 1 — Churn Overview

![Churn Overview](<Dashboard/Churn overview.png>)

### Purpose

The Churn Overview provides a high-level view of overall churn
performance, revenue impact, and how churn is distributed across
contract type and tenure.

### Key KPIs

| KPI | Result |
|---|---:|
| Total Customers | 7,043 |
| Total Churned | 1,869 |
| Churn Rate | 26.54% |
| Monthly Revenue | 456.12K |
| Monthly Revenue Lost | 139.13K |
| Lost Revenue % | 30.50% |

### Churn by Contract Type

| Contract Type | Total Churned |
|---|---:|
| Month-to-month | 1,655 |
| One year | 166 |
| Two year | 48 |

### Churn by Tenure Group

| Tenure Group | Total Churned |
|---|---:|
| 0-15 | 1,136 |
| 15-30 | 289 |
| 30-45 | 196 |
| 45-60 | 155 |
| more than 60 | 93 |

### Key Findings

- Overall churn rate is **26.54%**, with **1,869** customers lost out of **7,043**.
- Lost revenue represents **30.50%** of monthly revenue — a higher share than the churn rate itself, meaning churned customers tend to be higher-value customers.
- **Month-to-month** contracts account for **1,655** of the **1,869** total churned customers (about **88.6%**).
- The **0-15 months** tenure group alone accounts for **1,136** churned customers (about **60.8%** of total churn) — the highest-risk window is right after signup.
- Churn rate drops steadily as tenure increases, from around **50%** for brand-new customers down to near **0%** for long-tenured customers.

---

# 📄 Page 2 — Services & Customer Experience

![Services & Customer Experience](<Dashboard/services & customer experience.png>)

### Purpose

This page examines how service subscriptions and billing choices
relate to churn.

### Churn by Service Subscription

| Service | Segment | Total Churned |
|---|---|---:|
| Tech Support | No | 1,446 |
| Tech Support | Yes | 310 |
| Tech Support | No internet service | 113 |
| Phone Service | Yes | 1,699 |
| Phone Service | No | 170 |
| Internet Service Type | Fiber optic | 1,297 |
| Internet Service Type | DSL | 459 |
| Internet Service Type | No | 113 |
| Online Security | No | 1,461 |
| Online Security | Yes | 295 |
| Online Security | No internet service | 113 |
| Online Backup | No | 1,233 |
| Online Backup | Yes | 523 |
| Online Backup | No internet service | 113 |
| Paperless Billing | Yes | 1,400 |
| Paperless Billing | No | 469 |

### Key Findings

- **Fiber optic** customers make up **1,297** of the **1,869** churned customers (about **69.4%**) — by far the highest-churn internet service type.
- Customers **without Tech Support** account for **1,446** churned customers, compared to only **310** who had Tech Support — Tech Support is strongly linked to retention.
- Customers **without Online Security** account for **1,461** churned customers, compared to **295** who had it.
- **Paperless Billing** users make up **1,400** of the **1,869** churned customers (about **74.9%**).
- Most churned customers **did** have Phone Service (**1,699**), so phone service alone isn't a differentiator — it's the add-on services that matter.

---

# 📄 Page 3 — Customer Profile & Payment

![Customer Profile & Payment](<Dashboard/Customer Profile & Payment.png>)

### Purpose

This page looks at how demographic factors and payment method
relate to churn.

### Churn by Customer Profile

| Segment | Value | Total Churned |
|---|---|---:|
| Senior Citizen | No (0) | 1,393 |
| Senior Citizen | Yes (1) | 476 |
| Dependents | No | 1,543 |
| Dependents | Yes | 326 |

### Churn by Payment Method

| Payment Method | Total Churned |
|---|---:|
| Electronic check | 1,071 |
| Mailed check | 308 |
| Bank transfer (automatic) | 258 |
| Credit card (automatic) | 232 |

### Key Findings

- Customers **without dependents** account for **1,543** of the **1,869** churned customers (about **82.6%**).
- **Electronic check** is by far the most common payment method among churned customers, at **1,071** (about **57.3%** of total churn) — more than the other three payment methods combined.
- **Automatic payment methods** (Bank transfer and Credit card) show much lower churn counts (**258** and **232**), suggesting customers on manual/electronic check payments are more likely to leave.

---

# 📄 Page 4 — Cross-analysis & Customer Segmentation

![Cross-analysis & Customer Segmentation](<Dashboard/Cross-analysis & Customer Segmentation.png>)

### Purpose

This page drills into how tenure, contract type, and Tech Support
interact to reveal the highest-risk customer segments.

### Churn Rate by Tenure — Month-to-month Contract

| Tenure Group | Total Churned | Churn Rate | Total Monthly Charges |
|---|---:|---:|---:|
| 0-15 | 1,121 | 50.68% | 130,871.50 |
| 15-30 | 267 | 34.10% | 55,319.40 |
| 30-45 | 155 | 32.98% | 36,387.85 |
| 45-60 | 88 | 29.14% | 24,839.90 |
| more than 60 | 24 | 22.22% | 9,875.50 |
| **Total** | **1,655** | **42.71%** | **257,294.15** |

### Churn Rate by Tech Support — Month-to-month Contract

| Tech Support | Total Churned | Churn Rate |
|---|---:|---:|
| No | 1,350 | 50.37% |
| Yes | 206 | 30.70% |
| **Total** | **1,556** | **46.43%** |

### Churn Rate by Tenure & Tech Support — Fiber Optic Customers

| Tech Support | 0-15 | 15-30 | 30-45 | 45-60 | more than 60 | Total |
|---|---|---|---|---|---|---|
| No | 657 (69.45%) | 189 (47.85%) | 115 (37.83%) | 96 (31.07%) | 44 (15.94%) | 1,101 (49.37%) |
| Yes | 63 (62.38%) | 33 (27.97%) | 38 (29.01%) | 28 (17.07%) | 34 (9.66%) | 196 (22.63%) |
| **Total** | **720 (68.77%)** | **222 (43.27%)** | **153 (35.17%)** | **124 (26.22%)** | **78 (12.42%)** | **1,297 (41.89%)** |

### Key Findings

- New month-to-month customers (**0-15** months) churn at **50.68%**, more than double the rate of customers past 45 months (**29.14%**).
- Within month-to-month contracts, customers **without Tech Support** churn at **50.37%**, compared to **30.70%** for those **with Tech Support** — a **~20 point** gap.
- The single riskiest segment is **Fiber Optic + No Tech Support + 0-15 months tenure**, churning at **69.45%**.
- Having Tech Support consistently lowers churn across every tenure group for Fiber Optic customers — even long-tenured Fiber Optic customers without Tech Support (more than 60 months) still churn at **15.94%**, while those with Tech Support churn at only **9.66%**.

---

# 💡 Key Insights

### 1. Churn Is Concentrated in Month-to-month Contracts

**1,655** of **1,869** churned customers (**88.6%**) were on month-to-month
contracts, compared to only **166** one-year and **48** two-year customers.

### 2. Early Tenure Is the Highest-Risk Window

The **0-15 months** tenure group accounts for **60.8%** of all churn, and
within month-to-month contracts churn rate starts at **50.68%** and
steadily declines as tenure grows.

### 3. Lack of Tech Support Strongly Predicts Churn

Customers without Tech Support churn at roughly double the rate of
those with it, both overall (**1,446 vs 310**) and within month-to-month
contracts (**50.37% vs 30.70%**).

### 4. Fiber Optic + No Tech Support + New Customer Is the Riskiest Segment

This combination churns at **69.45%**, the highest churn rate found in
the cross-analysis.

### 5. Revenue Loss Is Disproportionate to Churn Rate

Churn rate is **26.54%**, but lost revenue is **30.50%** of monthly
revenue — churned customers skew toward higher monthly charges.

### 6. Paperless Billing and Electronic Check Correlate with Churn

**74.9%** of churned customers used Paperless Billing, and **57.3%** paid
via Electronic check — both far higher than the other options.

---

# 📈 Business Recommendations

Based on the analysis, areas for further investigation and action
include:

- Launching retention offers targeted at new (0-15 month) month-to-month customers, especially in the first billing cycles.
- Promoting or bundling Tech Support with Fiber Optic plans to reduce churn in the highest-risk segment.
- Reviewing Fiber Optic pricing and service quality, given its disproportionate share of churn.
- Encouraging migration from Electronic check to automatic payment methods (Bank transfer / Credit card), which show lower churn.
- Offering incentives for month-to-month customers to move to one- or two-year contracts.
- Investigating why customers without dependents churn more, to see if it reflects price sensitivity or lack of loyalty drivers.

---

# 📁 Repository Structure

```text
📦 Vodafone-Customer-Churn-Analysis
│
├── 📂 Project file
│   └── Vodafone Churn Dashboard.pbix
│
├── 📂 Dataset
│   └── dataset.xlsx
│
├── 📂 Dashboard
│   ├── page-1-churn-overview.png
│   ├── page-2-services-customer-experience.png
│   ├── page-3-customer-profile-payment.png
│   └── page-4-cross-analysis-segmentation.png
│
└── 📜 README.md
```
