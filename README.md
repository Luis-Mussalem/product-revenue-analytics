📈 Product Revenue & Retention Analytics

End-to-end analytical project focused on revenue, retention, and customer lifecycle analysis using a cohort-based methodology.
The project aims to understand how customer value evolves over time and how retention patterns impact long-term revenue performance.

📌 Business Questions

How do customer retention patterns evolve over time?

Do cohorts with higher user retention also generate higher revenue?

How concentrated is revenue across customers and cohorts?

How does customer lifetime value (LTV) change across acquisition periods?

---

📂 Dataset

Source: Kaggle – Online Retail II (UCI)

Scope: Transactional retail data

Granularity: Invoice-level transactions

Time period: 2009–2011

Data Quality & Filtering Criteria

For cohort and retention analysis, only valid transactions were considered:

Identified customers (Customer ID not null)

Positive quantities (excluding returns)

Positive prices

This ensures analytical consistency and business relevance, avoiding distortions caused by refunds or incomplete customer records.

---

🛠️ Tools & Technologies

Python (Pandas, NumPy, Matplotlib, Seaborn)

Jupyter Notebook

Git & GitHub

(Power BI dashboard to be added in the next stage)

---

🔍 Analytical Approach

The analysis follows a structured, lifecycle-driven methodology.

🔹 Time Standardization

All dates were standardized at a monthly level, ensuring consistent temporal aggregation and comparability across customer lifecycles.

We always standardize dates at a monthly level for cohort analysis to ensure consistent temporal aggregation and comparability across customer lifecycles.

🔹 Cohort Definition

Each customer is assigned to a Cohort Month based on their first purchase date

A CohortIndex is calculated as the number of months since the first purchase

CohortIndex represents the number of months since a customer’s first purchase, enabling a lifecycle-based view of retention and revenue behavior.

🔹 Retention Analysis

Retention analysis was conducted using a cohort-based methodology, allowing direct comparison of customer lifecycle behavior across different acquisition periods.

Customer retention matrices were built at the cohort level

Heatmaps were used to visualize retention decay over time

Cohort heatmaps enable a lifecycle-based comparison of customer retention, highlighting early churn patterns and long-term engagement trends across acquisition periods.

🔹 Revenue Cohort Analysis

In addition to user retention, revenue retention was analyzed to capture value concentration effects.

Key findings include:

Revenue-based cohort analysis revealed that not all retained customers contribute equally to revenue

In several cohorts, a small number of high-value customers disproportionately contributed to total revenue in later lifecycle stages

Revenue analysis revealed significant revenue concentration, where a small number of high-value customers disproportionately contributed to cohort revenue in later lifecycle stages.

This highlights why revenue retention cannot be inferred solely from user retention.

🔹 Lifetime Value (LTV)

A simplified, observed LTV per cohort was calculated by dividing:

Total cohort revenue

By the number of customers acquired in the cohort’s first month

Results show:

Early cohorts exhibit higher LTV due to longer observation windows

Later cohorts display more stable and predictable revenue contribution

LTV analysis revealed that early cohorts exhibit higher lifetime value due to longer observation windows, while later cohorts show more stable and predictable revenue contribution, highlighting a maturing acquisition process.

---

📊 BI-Ready Outputs

To support scalable visualization and dashboarding, BI-ready datasets were prepared at multiple levels:

Customer-level transactional data

Cohort-level retention metrics

Cohort-level revenue and LTV metrics

Prepared BI-ready datasets at both customer and cohort levels, enabling scalable dashboarding while keeping analytical logic centralized in Python.

These datasets are designed to minimize complex calculations in BI tools and maintain a clean separation between data preparation and visualization logic.

---

📁 Project Structure

```
product-revenue-analytics/
├── data/
│   ├── raw/
│   │   └── online_retail_II.csv
│   └── processed/
│       ├── customer_level.csv
│       ├── cohort_retention.csv
│       └── cohort_revenue.csv
├── notebooks/
│   └── revenue_retention_analysis.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

🚀 Next Steps

Build an interactive Power BI dashboard to:

Explore retention and revenue cohorts visually

Track KPIs such as active customers, revenue retention, and LTV

Enable executive-level storytelling and decision support