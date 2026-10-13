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
| **Records analysed** | 1,200 patients in the cleaned table (`cleaned`) |
| **Database** | `master_project` |
| **Target column** | `disease_prediction` (Yes / No) |

## 🗂️ Dataset Description

| Column | Description |
|---|---|
| `patient_id` | Unique patient identifier |
| `age` / `age_group` | Patient age, grouped as 18-30, 31-45, 46-60, 61-75, 76+ |
| `sex` | Male / Female |
| `bmi` | Body Mass Index |
| `blood_pressure` | Blood pressure reading |
| `glucose_level` | Blood glucose level |
| `cholesterol` | Cholesterol level |
| `heart_rate` | Heart rate |
| `smoking` | Smoker (Yes / No) |
| `family_history` | Family history of disease (Yes / No) |
| `physical_activity` | Low / Moderate / High |
| `sleep_hours` | Average sleep duration |
| `disease_prediction` | Predicted disease outcome (Yes / No) |

## ❓ Questions Answered

| # | Question | Focus |
|---|---|---|
| 1 | What is the disease prediction percentage? | Disease prevalence |
| 2 | Which age group has the highest number of predicted disease cases? | Risk by age |
| 3 | What is the disease rate for each sex? | Risk by gender |
| 4 | Which age group has the highest average blood pressure? | Average BP by age |
| 5 | Which physical activity group has the highest average BMI? | BMI vs activity |
| 6 | Which prediction group has the highest average BMI, BP, glucose and cholesterol? | Multi-indicator comparison |
| 7 | Which smoking group has the highest average blood pressure? | BP vs smoking |
| 8 | Which family-history group has the highest average glucose? | Glucose vs family history |
| 9 | Which sex has the highest average cholesterol? | Cholesterol by sex |
| 10 | Which age group has the highest percentage of smokers? | Smoking by age |
| 11 | What is the average sleep duration for Yes and No predictions? | Sleep vs prediction |
| 12 | Which age group has the highest average heart rate? | Heart rate by age |
| 13 | Which age group + sex combination has the most Yes predictions? | Multi-factor demographics |
| 14 | Which patients have the highest BMI, glucose, cholesterol and blood pressure? | Extreme-value analysis |
| 15 | Which combination of age group + sex + smoking + activity + family history has the highest Yes-prediction rate? | Multi-factor risk profile |

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

## ▶️ How to Run

1. Install **MySQL** and MySQL Workbench.
2. Create the database and import the CSV as a table named `cleaned`:
   ```sql
   CREATE DATABASE master_project;
   USE master_project;
   ```
   *(Use Workbench's **Table Data Import Wizard** to load `data/Cleaned_disease_prediction_data.csv` into `cleaned`.)*
3. Make sure an `age_group` column exists (derived from `age`).
4. Open and run `sql/MASTERPROJECT.sql` query by query.

## 📊 Presentation

A visual walkthrough of every query, output and insight is available in
[`presentation/SQL_Project_Healthcare_Disease_Analysis.pdf`](presentation/SQL_Project_Healthcare_Disease_Analysis.pdf).

## 🚀 Possible Next Steps

- Visualise the results in Power BI / Tableau
- Build a machine-learning model for disease prediction in Python
- Add rate-within-group analysis (e.g. disease rate within each sex or age group)

## 👤 Author

**Your Name**
[LinkedIn](https://www.linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)

⭐ If you found this project useful, consider giving it a star!
