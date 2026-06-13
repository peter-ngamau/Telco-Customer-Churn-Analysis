# Customer Churn Analysis — Telco Dataset
**Saiket Systems | Business Analysis Internship Project**

## Project Overview

This project analyses customer churn behaviour using the IBM Telco Customer Churn Dataset, 
a widely used benchmark dataset in customer retention analytics. The goal is to identify 
which customer segments are most likely to churn and provide data-driven recommendations 
to help a telecommunications business reduce churn rates.

The analysis covers the complete EDA pipeline: data loading, cleaning, univariate and 
bivariate exploration, and visualisation of key churn drivers.

---

## Dataset

| Property | Detail |
|---|---|
| **Source** | IBM Telco Customer Churn Dataset |
| **Records** | ~7,000 customers |
| **Features** | 21 columns |
| **Target Variable** | `Churn` (Yes / No) |

**Key features include:** contract type, tenure, monthly charges, total charges, internet 
service type, payment method, tech support, online security, and demographic attributes 
(gender, senior citizen status, dependents).

---

## Tools & Libraries

| Tool | Purpose |
|---|---|
| Python | Core analysis language |
| pandas | Data loading, cleaning, manipulation |
| matplotlib | Base visualisations |
| seaborn | Statistical charts and heatmaps |
| Jupyter Notebook | Interactive development environment |

---

## Project Pipeline

### Task 1 — Data Loading & Inspection
- Loaded the dataset and reviewed shape, dtypes, and missing values
- Identified `TotalCharges` stored as object type due to blank string entries
- Confirmed churn rate baseline across the dataset

### Task 2 — Data Cleaning
- Converted `TotalCharges` to numeric and handled blank entries
- Converted `SeniorCitizen` from integer (0/1) to readable labels
- Confirmed no duplicate records

### Task 3 — Univariate Analysis
- Explored distribution of churn across contract types, payment methods, and internet services
- Visualised tenure distribution, monthly charge spread, and senior citizen breakdown

### Task 4 — Bivariate Analysis
- Compared churn rates across contract type, internet service, and payment method
- Analysed monthly charges and tenure against churn status
- Explored correlation between numeric features using a heatmap

### Task 5 — Key Findings & Business Recommendations
- Summarised the main churn drivers with supporting visualisations
- Produced business-facing recommendations for retention strategy

---

## Key Findings

| Finding | Detail |
|---|---|
| **Contract type is the strongest churn predictor** | Month-to-month customers churned at a significantly higher rate than one- or two-year contract customers |
| **Tenure drives retention** | Customers in their first 12 months show the highest churn risk — early engagement is critical |
| **Electronic check payment correlates with churn** | Customers paying by electronic check had the highest churn rates compared to other payment methods |
| **Fibre optic customers churn more** | Despite faster service, fibre optic internet customers showed higher churn — likely price sensitivity |
| **Senior citizens are at higher risk** | Senior customers churned at a higher rate than non-seniors |

---

## Business Recommendations

1. **Incentivise longer contracts** — Offer discounts or loyalty rewards to move month-to-month customers onto annual plans
2. **Target the first 12 months** — Introduce proactive onboarding and check-in programmes for new customers
3. **Review fibre optic pricing** — Analyse whether pricing is the churn driver among fibre customers and adjust packages
4. **Senior customer retention programme** — Dedicated support and simplified plans may reduce senior churn
5. **Payment method migration** — Encourage electronic check users to switch to auto-pay options, which correlate with lower churn

---

## Repository Structure
---
Customer-Churn-Analysis/

│

├── churn_analysis.ipynb       # Full analysis notebook

├── customer_churn_data.csv    # Dataset

└── README.md                  # Project documentation

## How to Run

1. Clone the repository:
```bash
   git clone https://github.com/peter-ngamau/Customer-Churn-Analysis.git
```
2. Open `churn_analysis.ipynb` in Jupyter Notebook or VS Code
3. Run all cells in order

---

## Author

**Peter Ngamau**  
Data Analyst | Python · SQL · Power BI  
📍 Nairobi, Kenya  
[LinkedIn](https://linkedin.com/in/peter-ngamau) · [Portfolio](https://peter-ngamau.github.io) · [GitHub](https://github.com/peter-ngamau)

*Internship Project — Saiket Systems Business Analysis Program*
