#  Telco Customer Churn Analysis
**Saiket Systems | Business Analysis Internship Project**

---

##  Project Overview

This project analyzes customer churn in a telecommunications company using real-world data. The goal is to uncover *why* customers leave, *who* is most at risk, and *what* the business can do about it.

**Dataset:** IBM Telco Customer Churn Dataset — 7,043 customers, 21 features

---

##  Project Structure

| File | Description |
|---|---|
| `Understand_the_Dataset.ipynb` | Data loading, structure exploration, missing value detection |
| `Data_Cleaning.ipynb` | Fixing data types, handling blanks, standardizing columns |
| `Explorative_Data_Analysis.ipynb` | Summary statistics, histograms, box plots, churn distribution |
| `Customer_Segmentation_Visualization.ipynb` | Tenure segmentation, donut chart, clustered bar chart |
| `Advanced_Analysis.ipynb` | Churn by demographics, contract type, payment method, internet service |
| `Cleaned_Telco_Customer_Churn.csv` | Final cleaned dataset used across all tasks |

---

##  Tools & Libraries

- **Python** — pandas, matplotlib, seaborn
- **Jupyter Notebook**

---

##  Data Cleaning Summary

The raw dataset had two notable issues before analysis could begin:

- **`TotalCharges`** was stored as text, not a number. It also contained 11 blank rows belonging to brand-new customers (tenure = 0). These were converted to numeric and filled with `0.0`.
- **`SeniorCitizen`** was stored as `0` and `1` instead of readable `No`/`Yes` labels — corrected for clarity.
- Column names were standardized to lowercase with underscores for consistency.
- Two helper columns were added: `numeric_churn` (Yes=1, No=0) for calculations, and `tenure_group` to segment customers into lifecycle stages.

---

##  Key Findings

### Overall Churn Rate
> **26.5%** of customers churned — that's 1 in every 4 customers.

---

### 1️ Churn by Tenure Segment

Customers were grouped into three lifecycle stages:

| Segment | Customers | Churn Rate |
|---|---|---|
| New (0–12 months) | 2,186 | **47.4%** ⚠️ |
| Mid-term (13–36 months) | 1,856 | 25.5% |
| Long-term (37+ months) | 3,001 | 11.9% ✅ |

> The first year is the most critical window. Nearly half of new customers leave before reaching 13 months.

---

### 2️ Churn by Contract Type

| Contract | Churn Rate |
|---|---|
| Month-to-month | **42.7%** |
| One year | 11.3% |
| Two year | **2.8%** |

> Customers on short-term contracts are by far the most likely to leave. Long-term contracts create loyalty.

---

### 3️ Churn by Payment Method

| Payment Method | Churn Rate |
|---|---|
| Electronic check | **45.3%** |
| Mailed check | 19.1% |
| Bank transfer (automatic) | 16.7% |
| Credit card (automatic) | 15.2% |

> Electronic check users churn at nearly triple the rate of automatic payment users.

---

### 4️ Churn by Demographics

| Group | Churn Rate |
|---|---|
| Senior Citizens | **41.7%** |
| Non-Senior Citizens | 23.6% |
| Female | 26.9% |
| Male | 26.2% |

> Senior citizens churn at almost double the rate of non-seniors. Gender has no significant impact.

---

### 5️ Churn by Internet Service

| Internet Service | Churn Rate |
|---|---|
| Fiber optic | **41.9%** |
| DSL | 19.0% |
| No internet | 7.4% |

> Fiber optic customers are churning at a very high rate, suggesting possible dissatisfaction with price or service quality.

---

##  Business Recommendations

1. **Invest in the first 12 months** — new customers are the highest-risk group. Onboarding check-ins and welcome discounts can significantly reduce early churn.
2. **Incentivize longer contracts** — offering discounts for upgrading from month-to-month to annual contracts directly targets the highest-churn segment.
3. **Promote auto-pay enrollment** — customers on automatic payments churn far less. A small discount for switching off electronic checks could shift behavior.
4. **Create a senior loyalty program** — simplified plans and dedicated support for senior citizens address a disproportionately high-risk group.
5. **Investigate fiber optic service quality** — a 41.9% churn rate signals either a pricing or service delivery problem that needs urgent attention.

---

##  How to Run

1. Clone this repository
2. Place the raw CSV in your working directory
3. Run the notebooks **in order** (Task 1 → 2 → 3 → 4 → 5)
4. Task 2 generates `Cleaned_Telco_Customer_Churn.csv` which all subsequent notebooks depend on

```bash
pip install pandas matplotlib seaborn
```

---

*Internship Project — Saiket Systems Business Analysis Program*
