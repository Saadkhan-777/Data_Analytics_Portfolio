# Titanic Dataset - Data Analysis & Exploration

Welcome to my **first Data Analysis project**! In this project, I performed Exploratory Data Analysis (EDA) and Data Cleaning on the iconic **Titanic Dataset** using Python's core data science stack: **NumPy**, **Pandas**, **Matplotlib**, and **Seaborn**.

---

## 📌 Project Overview

The objective of this project is to analyze the Titanic passenger manifest to understand passenger demographics, inspect missing values, clean data, and discover key insights regarding passenger survival rates.

---

## 🛠️ Tech Stack & Libraries Used

- **Python 3**
- **Pandas**: Data manipulation, cleaning, and structural inspection (`DataFrame`, `.head()`, `.info()`, `.describe()`, `.fillna()`).
- **NumPy**: Numerical computing and foundational array handling.
- **Matplotlib**: Basic visualization and histogram plotting.
- **Seaborn**: Statistical data visualization.

---

## 🚀 Key Steps & Workflow

1. **Environment Setup & Data Loading:**
   - Imported required data science libraries.
   - Loaded raw dataset (`Titanic-Dataset.csv`) into a Pandas DataFrame.
   - Created a clean working copy (`df_clean`) to ensure data preservation.

2. **Exploratory Data Analysis (EDA):**
   - **Structure Inspection:** Checked DataFrame shape (`891 rows, 12 columns`), column names, and data types.
   - **Statistical Summary:** Executed `.describe()` to obtain summary statistics (mean, median, std, min, max) across numerical variables.
   - **Categorical Inspection:** Checked unique values for key categorical columns (`Sex`, `Embarked`, `Pclass`, `Survived`).

3. **Data Quality & Missing Value Assessment:**
   - Evaluated missing/null values:
     - `Age`: 177 missing values
     - `Cabin`: 687 missing values
     - `Embarked`: 2 missing values
   - Verified duplicate records (`0 duplicates found`).

4. **Data Cleaning & Imputation:**
   - Analyzed the distribution of the `Age` variable using statistical measures (`Mean: ~29.70`, `Median: 28.0`) and histogram visualization.
   - Imputed missing `Age` values using the **median age (28.0)** to minimize skewness from extreme values.
   - Inspected mode distribution for `Embarked` port values (`S: 644`, `C: 168`, `Q: 77`).

---

## 📁 Repository Structure

```text
├── Titanic-Dataset.csv     # Raw dataset
├── titanic_analysis.ipynb # Jupyter / Colab Notebook with step-by-step code
└── README.md              # Project documentation
```

---

## 📊 Key Findings & Summary Statistics

- **Total Passengers Analyzed:** 891
- **Overall Survival Rate:** ~38.4%
- **Passenger Classes:** 1st, 2nd, and 3rd Class (majority in 3rd Class)
- **Age Distribution:** Right-skewed distribution centered around ~28–30 years.

---

## 💻 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/titanic-data-analysis.git
   cd titanic-data-analysis
   ```

2. **Install required packages:**
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. **Run the notebook:**
   ```bash
   jupyter notebook titanic_analysis.ipynb
   ```
   *Alternatively, open the notebook directly in Google Colab.*

---

## 🎯 What I Learned

- How to inspect dataset structures, data types, and shape using Pandas.
- How to handle missing values appropriately using median imputation.
- How to visualize distributions using histograms and Matplotlib.
- Best practices in maintaining raw and clean DataFrame copies.

---

*Created as my first data science portfolio project.*
