# Synthetic Immigration Case Data

## Overview

This project generates a **synthetic dataset** representing immigration case workflows.  
The dataset is fully artificial and contains **no real client data**.

The project is designed to simulate realistic operational patterns found in immigration case management systems, including case lifecycles, staff assignments, jurisdictions, and time-based trends.

---

## Objectives

- Generate a realistic synthetic dataset suitable for:
  - Exploratory data analysis (EDA)
  - Time-series analysis
  - Dashboard development
- Model common immigration case attributes and workflows
- Demonstrate clean, modular Python code for data generation and analytics

---

## Dataset Description

The generated dataset contains **3,000 synthetic immigration cases** with the following attributes:

| Column | Description |
|------|------------|
| CaseID | Unique case identifier (ID-0001 … ID-3000) |
| Attorney | Assigned attorney (Attorney 1–7) |
| Paralegal | Assigned paralegal (Paralegal 1–5) |
| Legal Assistant | Assigned legal assistant (Legal Assistant 1–3) |
| Status | Case status: Open, Pending, or Closed |
| Open Date | Date the case was opened |
| Pending Date | Date the case was submitted (if applicable) |
| Close Date | Date the case was closed (if applicable) |
| Jurisdiction | USCIS, Immigration Court, or BIA |
| Case Type | Type of immigration case (e.g., Asylum, AOS, Naturalization) |

### Business Rules Enforced
- Pending dates always occur **after** open dates
- Close dates always occur **after** pending dates
- Status is consistent with lifecycle dates
- Jurisdiction is constrained by case type
- Case volume follows **trend + seasonality** over time

---

## Notebooks

### 1️⃣ `synthetic_immigration_data.ipynb`
- Generates the synthetic dataset
- Implements:
  - Time-series intake logic
  - Staff assignment with realistic workload imbalance
  - Case lifecycle rules and validation checks
- Outputs a clean pandas DataFrame ready for analysis

### 2️⃣ `synthetic_data_analysis.ipynb`
- Performs exploratory analysis and aggregation
- Builds reusable **count tables** for:
  - Status
  - Jurisdiction
  - Staff roles
  - Year and Year-Month time series
- Produces:
  - Line charts
  - Stacked bar charts
  - Pie charts
- Demonstrates how the dataset can support dashboards and reporting

---

## Technologies Used

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn

---

## Disclaimer

All data in this repository is **synthetic** and generated for educational and demonstration purposes only.  
No real individuals, cases, or organizations are represented.

---

## Author

Created by **Martin Milon Velarde**
