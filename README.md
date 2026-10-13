# 🩺 Healthcare Disease Analysis & Prediction (SQL Project)

An end-to-end **SQL exploratory data analysis** of a patient health dataset. Using 15 business-style questions, the project looks at how age, sex, lifestyle habits (smoking, physical activity, sleep) and clinical indicators (BMI, blood pressure, glucose, cholesterol, heart rate) relate to **predicted disease outcomes**.

> **Tools:** MySQL · SQL (aggregations, subqueries, `CASE WHEN`, `GROUP BY`, window-free percentage logic)
> **Domain:** Healthcare Analytics

---

## 📌 Project Overview

| Item | Details |
|---|---|
| **Project title** | Healthcare Disease Analysis & Prediction |
| **Dataset** | Disease prediction dataset (cleaned) |
| **Business domain** | Healthcare |
| **Records analysed** | 10,000 patients in the cleaned table (`cleaned`) |
| **Database** | `master_project` |
| **Target column** | `disease_prediction` (Yes / No) |

## 🔍 Key Insights

- **Prevalence:** 75.83% of patients have no disease predicted, while 24.17% (290 patients) are predicted to have the disease.
- **Age:** The **61-75** age group has the most predicted disease cases (104), followed by 46-60 (70).
- **Blood pressure:** The **76+** group has the highest average blood pressure (126.33).
- **Health indicators:** Patients predicted "Yes" have slightly higher average BMI (26.85 vs 26.05), BP (127.33 vs 122.96), glucose (117.05 vs 107.98) and cholesterol (210.2 vs 201.18) than the "No" group.
- **Lifestyle:** Average BMI is almost identical across activity levels, with the **High** activity group marginally highest. Patients predicted "No" sleep slightly longer on average (7.02 h vs 6.86 h).
- **Smoking:** Non-smokers show a higher average blood pressure than smokers (124.60 vs 122.17). The **31-45** and **46-60** age groups have the largest share of smokers.
- **Demographics:** The **61-75** group, both male and female, has the most positive predictions.
- **Risk profile:** Several small segments reach a 100% Yes-prediction rate, e.g. 76+ Female smokers with low activity and no family history (see Q15 output).

## 🛠️ SQL Concepts Used

- Aggregate functions: `COUNT`, `AVG`, `MAX`, `SUM`, `ROUND`
- `GROUP BY`, `ORDER BY`, `WHERE`, `LIMIT`
- Subqueries (percentage-of-total and `MAX()` lookups)
- Conditional aggregation with `CASE WHEN`
- Multi-column grouping for segmentation analysis

## 📁 Repository Structure

```
├── data/
│   └── Cleaned_disease_prediction_data.csv
├── sql/
│   └── MASTERPROJECT.sql
├── presentation/
│   └── SQL_Project_Healthcare_Disease_Analysis.pdf
└── README.md
```


## 🚀 Possible Next Steps

- Visualise the results in Power BI
- Build a machine-learning model for disease prediction in Python

## 👤 Author

**Suraj Kapare**
[LinkedIn](https://linkedin.com/in/suraj-kapare-437941283) · [GitHub](https://github.com/surajkapare)

⭐ If you found this project useful, consider giving it a star!
