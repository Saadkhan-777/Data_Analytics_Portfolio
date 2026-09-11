# Telecom Customer Churn Analysis

## Overview
This project focuses on analyzing customer churn for a telecommunications provider to identify key operational patterns and underlying risk factors driving customer attrition. Using exploratory data analysis (EDA) techniques in Python, the project details data cleaning workflows, feature type adjustments, missing data verification, and univariate/bivariate visual explorations using `numpy`, `pandas`, `matplotlib`, and `seaborn`.

---

## Dataset Description
The analysis uses the **Telecom Customer Churn** dataset containing 7,043 customer records and 21 features.

* **Target Variable**: `Churn` (Whether the customer left the company: `Yes` or `No`).
* **Total Rows**: 7,043
* **Total Columns**: 21

### Features Breakdown
* **Demographics**: `customerID`, `gender`, `SeniorCitizen` (converted from 0/1 to Yes/No), `Partner`, `Dependents`
* **Services**: `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`
* **Account Info**: `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`

---

## Key Highlights & Data Preprocessing
* **Type Conversion & Handling Blank Values**: Identified whitespace strings (`" "`) in `TotalCharges` for customers with a `tenure` of 0. Replaced whitespace values with `"0"` and converted `TotalCharges` to `float64`.
* **Value Mapping**: Standardized `SeniorCitizen` from binary integers (`0`, `1`) to readable string flags (`"no"`, `"yes"`) for consistent visual mapping.
* **Integrity Checks**: Confirmed zero duplicate rows across customer IDs and zero missing (`NaN`) values post-cleaning.

---

## Tech Stack
* **Python**: Core programming language
* **Pandas**: Data manipulation, statistical summary, type casting, and grouping
* **NumPy**: Numeric operations and array structures
* **Matplotlib & Seaborn**: Data visualizations and count distributions

---

## Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Saadkhan-777/Data_Analytics_Portfolio.git
   cd Data_Analytics_Portfolio/Project_03_Customer_Churn

   ```

2. **Install required dependencies:**
   ```bash
   pip install numpy pandas matplotlib seaborn
   ```

3. **Run the Notebook:**
   Launch Google Colab or Jupyter Notebook and run `Customer_Churn_Analysis.ipynb`:
   ```bash
   jupyter notebook
   ```

---

## Visualizations Included
* **Target Distribution**: Bar chart of overall churn count breakdown using `sns.countplot` with labeled totals.
* **Demographic & Service Relationships**: Categorical distributions mapping churn rates against contract types, tenure ranges, internet services, and payment methods.
