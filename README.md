# HR Analytics Dashboard 📊

An interactive Tableau dashboard analyzing employee attrition, job satisfaction, and workforce KPIs, built on the IBM HR Analytics employee dataset.

## 📁 Files

| File | Description |
|---|---|
| `HR_Analytics_Dashboard.twb` | Tableau workbook — open in Tableau Desktop or Tableau Public |
| `HR Data.xlsx` | Source dataset the workbook connects to |

## 📌 Key Numbers

- **1,470** employee records across **3** departments (Sales, R&D, HR) and **9** job roles
- **Overall attrition rate: 16.1%** (237 of 1,470 employees left)
- **Average employee age: 36.9 years**
- Workforce split: 882 Male / 588 Female
- **Attrition by department:** Sales 20.6% · HR 19.0% · R&D 13.8%
- **Attrition by gender:** Male 17.0% · Female 14.8%

## 🗂️ Dataset Fields

The data covers 1,470 employee records with fields including:

- **Demographics:** Age, Gender, Marital Status, Education, Education Field
- **Job details:** Department, Job Role, Job Level, Business Travel, Over Time
- **Compensation:** Monthly Income, Daily/Hourly/Monthly Rate, Percent Salary Hike, Stock Option Level
- **Tenure:** Years At Company, Years In Current Role, Years Since Last Promotion, Years With Curr Manager, Total Working Years, Num Companies Worked
- **Satisfaction & performance:** Job Satisfaction, Environment Satisfaction, Relationship Satisfaction, Work Life Balance, Job Involvement, Performance Rating
- **Target variable:** Attrition (Yes/No)

## 🧮 Key Calculated Fields

| Field | Logic |
|---|---|
| Total Employees | `COUNTD([Employee Number])` |
| Avg. Age | `AVG([Age])` |
| Attrition Count | Sum of records where `Attrition = "Yes"` |
| Attrition Rate | Attrition Count ÷ Total Employees |
| Active Employee Find | Sum of records where `Attrition = "No"` |
| Age (bin) | Custom bins for age-group histogram |
| CF_age band | Grouped age-band dimension |

## 📈 Dashboard Sheets

- **All KPI** — high-level summary of headcount, attrition rate, and average age
- **Attrition by Gender** — attrition split across male/female employees
- **Department wise Attrition** — attrition rate compared across departments
- **Job Role Satisfaction Rating** — average satisfaction rating by job role
- **Donut chart** — job role / category distribution, built from two combined pie charts
- **Histogram (Age bins)** — employee age distribution using bins, a parameter control, and a gradient color scale

## 🛠️ Tools Used

- Tableau Desktop / Tableau Public (workbook version 18.1, built on Tableau 2026.2)

## 🚀 How to View

1. Download both `HR_Analytics_Dashboard.twb` and `HR Data.xlsx` (keep them in the same folder)
2. Open the `.twb` file in Tableau Desktop, **or**
3. Publish it to [Tableau Public](https://public.tableau.com/) for a free, interactive, shareable version

## ⚠️ Data Note

This dataset is the well-known public **IBM HR Analytics Employee Attrition** sample dataset, used widely for HR analytics practice. No real employee information is included.

---
*Feel free to fork, explore, and adapt this project for your own HR analytics practice.*
