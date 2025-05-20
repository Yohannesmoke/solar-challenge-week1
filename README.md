# 📝 Week 0 Challenge - Interim Report

**Solar Data Discovery: Cross-Country Solar Farm Analysis**
**Date Range:** 15 May – 22 May 2025
**Submitted:** 18 May 2025

---

## 📌 Overview

This repository contains my progress for Week 0 of the 10 Academy Artificial Intelligence Mastery Program. The challenge focuses on analyzing solar farm data from **Benin**, **Sierra Leone**, and **Togo**, with the objective of identifying high-potential regions for solar energy investment.

This README presents a summary of completed tasks (Git & environment setup), the approach for data profiling and EDA, and next steps.

---

## ✅ Task 1: Git & Environment Setup

**Branch:** `setup-task`
**Status:** ✅ Completed and merged into `main`

### ✔️ Steps Completed:

* Initialized a new GitHub repository: `solar-challenge-week1`
* Created and activated a Python virtual environment
* Added `.gitignore`, `requirements.txt`, and folder structure
* Set up CI/CD using **GitHub Actions** with a basic workflow:

  * Installs dependencies
  * Confirms Python version
* Documented the setup process in `README.md`

### 🗂 Folder Structure (so far)

```
solar-challenge-week1/
│
├── .github/workflows/ci.yml
├── .gitignore
├── requirements.txt
├── README.md
├── notebooks/
│   └── README.md
├── scripts/
├── data/  # ignored in .gitignore
└── tests/
```

---

## 🔍 Task 2: Data Profiling, Cleaning & EDA

**Status:** 🔄 In Progress
**Branches Created:**

* `eda-benin` (active)

### ✨ General Approach

For each country:

1. **Data Profiling**

   * Summary statistics (`df.describe()`)
   * Missing values (`df.isna().sum()`)
   * List columns with >5% missing data

2. **Cleaning & Outlier Detection**

   * Z-score method for outliers in `GHI`, `DNI`, `DHI`, `ModA`, `ModB`, `WS`, `WSgust`
   * Handle missing values with median imputation or removal
   * Export cleaned data to `data/<country>_clean.csv` (excluded from Git)

3. **Exploratory Data Analysis (EDA)**

   * Time series plots (GHI, DNI, DHI, Tamb vs Timestamp)
   * Correlation heatmaps
   * Distribution plots (histograms, scatter plots)
   * Cleaning impact on sensor readings
   * Wind analysis (radial plots)
   * Bubble chart (GHI vs Tamb with RH or BP)

---

## 🧠 Insights So Far (from Benin Dataset)

* **Missing Values:** Minor nulls found in wind data and temperature columns.
* **Outliers:** A few extreme values in `DNI` and `ModB` were flagged with |Z| > 3.
* **Early Observations:** Morning and midday solar irradiance peaks are visible. Cleaning appears to improve ModA/ModB readings.

---

## 📅 Remaining Tasks

| Task                                | Status     |
| ----------------------------------- | ---------- |
| EDA for Sierra Leone & Togo         | ⏳ To-do    |
| Cross-Country Comparison            | ⏳ Planned  |
| Statistical Testing (ANOVA)         | ⏳ Optional |
| Streamlit Dashboard (Bonus)         | ⏳ Optional |
| Final Report & Visualization Polish | ⏳ Upcoming |

---

## 🔗 Repository Link

📂 [GitHub Repository](https://github.com/yohannesmoke/solar-challenge-week1)

---

## 🗓 Submission Timeline

* **Interim Submission:** ✅ 18 May 2025
* **Final Submission:** 🗓 22 May 2025

---

## 🙌 Acknowledgements

Thanks to 10 Academy facilitators and peers for their support and guidance:

* Yabebal, Mahlet, Kerod, Rediet, Rehmet

---
