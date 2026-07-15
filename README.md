# 👥 HR Employee Attrition Analysis

An end-to-end data analytics project that identifies *why employees leave, predicts **who is likely to leave next, and translates those findings into an interactive **Power BI dashboard* for HR decision-making.

---

## 📌 Project Overview

Employee attrition costs organizations significantly in hiring, training, and lost productivity. This project analyzes historical HR data to uncover the key drivers of attrition and builds a machine learning model to flag high-risk employees before they leave — giving HR teams a chance to intervene proactively.

*Key business question:* Which employees are most likely to leave, and what factors are driving that decision?

---

## 🛠️ Tech Stack

| Stage | Tools |
|---|---|
| Data Cleaning & EDA | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| Predictive Modeling | Python (Scikit-learn — Logistic Regression, StandardScaler) |
| Dashboard & Reporting | Power BI (DAX, Power Query) |
| Version Control | Git & GitHub |

---

## 🔍 Project Workflow

1. *Data Cleaning & EDA (Python)*
   - Handled missing values, encoded categorical variables, checked class imbalance in the target (Attrition)
   - Explored relationships between attrition and features like OverTime, MonthlyIncome, Department, JobRole, and tenure-based variables

2. *Feature Engineering & Modeling (Python)*
   - Standardized numerical features using StandardScaler
   - Trained a *Logistic Regression* model to predict attrition
   - Extracted feature coefficients to rank the *top drivers of attrition*

3. *Dashboard Development (Power BI)*
   - Built a 3-page interactive report: *Overview, **Model Insights (Deep Dive), and **Employee Details*
   - Added slicers for Department and JobRole for dynamic filtering
   - Used DAX measures to calculate KPIs like Attrition Rate and OverTime Attrition Rate

---

## 📊 Dashboard Pages

### 1. Overview
High-level KPIs and attrition breakdown by overtime status, income, and department.

- *Attrition Rate:* 16.1%
- *Total Employees:* ~1,000
- *Avg Monthly Income:* ~7K
- *OverTime Attrition Rate:* 53.6% (employees who work overtime leave at a much higher rate)

### 2. Model Insights (Deep Dive)
Machine learning results and the top factors driving attrition.

- *Model Accuracy:* 87.8%
- *Model Recall:* 43.6%
- *High-Risk Employees Flagged:* 416
- *Top Drivers of Attrition (by coefficient magnitude):*
  1. OverTime
  2. Laboratory Technician (role)
  3. Business Travel — Frequently
  4. Years at Company
  5. Years in Current Role
  6. Marital Status — Single
  7. Number of Companies Worked
  8. Sales Representative (role)
  9. Years Since Last Promotion
  10. Years With Current Manager

### 3. Employee Details
A searchable, filterable table of at-risk employees (Age, Department, JobRole, MonthlyIncome, OverTime, YearsAtCompany) for HR to drill into individual cases.

---

## 💡 Key Insights

- *OverTime is the single strongest predictor of attrition* — employees working overtime leave at more than 3x the rate of those who don't.
- *Early-career and frequently-traveling employees* are disproportionately at risk.
- *Lack of promotion and long gaps with the same manager* correlate with higher attrition, suggesting stagnation is a major churn driver.
- Compensation alone doesn't explain attrition — engagement and role-related factors matter just as much.

---

## 📁 Repository Structure


HR-Employee-Attrition-Analysis/
│
├── data/
│   └── HR_Attrition_Data.csv
├── notebooks/
│   └── attrition_eda_and_model.ipynb
├── powerbi/
│   └── Attrition_Project.pbix
├── images/
│   └── dashboard_screenshots/
README.md


---

## 🚀 How to Reproduce

1. Clone the repo and open notebooks/attrition_eda_and_model.ipynb
2. Run all cells to reproduce the EDA and Logistic Regression model
3. Open powerbi/Attrition_Project.pbix in Power BI Desktop to explore the dashboard
4. Use the slicers on Page 1 to filter by Department / Job Role

---

## 🔮 Future Improvements

- Test additional models (Random Forest, XGBoost) and compare recall/precision tradeoffs
- Address class imbalance with SMOTE to improve recall
- Add a "Predicted Risk Score" column to the Employee Details page using the trained model
- Deploy the model via a simple API for real-time scoring

---

## 👤 Author

Thejushree | SQL · Power BI · Python
