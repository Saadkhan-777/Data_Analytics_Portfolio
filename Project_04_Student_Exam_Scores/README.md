# 📊 Project 04: Student Exam Scores Data Analysis

## 📌 Project Overview

This project presents a comprehensive Exploratory Data Analysis (EDA) on a dataset containing **30,641 student records** from a public school system. The analysis evaluates how various personal, academic, and socio-economic factors influence student test performance across three core subjects: **Math**, **Reading**, and **Writing**.

The primary objective is to uncover key academic performance drivers, isolate socio-economic disparities, and identify actionable insights for educators, school administrators, and policy planners.

---

## ❓ Key Analytical Questions

1. **Feature Impact**: Which demographic, socio-economic, and personal habits affect student test scores most significantly?
2. **Interaction Effects**: Are there compounding or interacting features (e.g., test preparation, parental education, lunch status, weekly study hours) that disproportionately impact student outcomes?

---

## 📁 Dataset Description

The dataset consists of **30,641 rows** and **15 columns**, tracking demographic attributes, home environment factors, study habits, and standardized exam scores.

### Data Dictionary

| Column Name | Data Type | Missing Values | Description / Categories |
| :--- | :--- | :--- | :--- |
| `Gender` | Object / Category | 0 | Gender of the student (`male`, `female`) |
| `EthnicGroup` | Object / Category | 1,840 | Ethnic origin (`group A` through `group E`) |
| `ParentEduc` | Object / Category | 1,845 | Highest education level of parents (`high school`, `some college`, `associate's degree`, `bachelor's degree`, `master's degree`) |
| `LunchType` | Object / Category | 0 | School lunch program (`standard`, `free/reduced`) |
| `TestPrep` | Object / Category | 1,830 | Test preparation course status (`none`, `completed`) |
| `ParentMaritalStatus` | Object / Category | 1,190 | Parents' marital status (`married`, `single`, `divorced`, `widowed`) |
| `PracticeSport` | Object / Category | 631 | Sports participation frequency (`regularly`, `sometimes`, `never`) |
| `IsFirstChild` | Object / Category | 904 | Whether student is the first child (`yes`, `no`) |
| `NrSiblings` | Float64 / Numeric | 1,572 | Number of siblings (range: `0.0` to `7.0`) |
| `TransportMeans` | Object / Category | 3,134 | Mode of school commute (`school_bus`, `private`) |
| `WklyStudyHours` | Object / Category | 955 | Weekly study duration (`< 5`, `5 - 10`, `> 10`) |
| `MathScore` | Int64 | 0 | Math test score (`0` to `100`, Mean: `66.56`) |
| `ReadingScore` | Int64 | 0 | Reading test score (`10` to `100`, Mean: `69.38`) |
| `WritingScore` | Int64 | 0 | Writing test score (`4` to `100`, Mean: `68.42`) |

---

## 🧹 Data Cleaning & Preprocessing Pipeline

1. **Working Copy Creation**: Maintained raw data integrity by generating a working DataFrame copy (`df_copy = df.copy()`).
2. **Redundant Feature Removal**: Dropped the index-like column `Unnamed: 0` to streamline data frame operations.
3. **Data Anomaly Cleaning**:
   - Identified and fixed string formatting errors in categorical variables (e.g., replaced corrupted Excel date-auto-formatting strings like `'10-May'` with the correct study hour range `'5 - 10'`).
4. **Missing Value Analysis**:
   - Identified missing counts across demographic features (`TransportMeans` had highest missing count at 3,134 records).
   - Confirmed **0 missing values** in target numerical variables (`MathScore`, `ReadingScore`, `WritingScore`).

---

## 🔍 Key Findings & Analytical Insights

* **Parental Education Level**: Strong positive correlation with student performance. Students whose parents hold a Master's or Bachelor's degree score higher across all three subjects compared to those with high school education.
* **Socio-Economic Impact (Lunch Type)**: Students on `standard` lunch consistently outperform students receiving `free/reduced` lunch by an average of 10–12 points, highlighting socio-economic security as a major baseline factor.
* **Test Preparation Course**: Completing a test prep course delivers a marked performance uplift, particularly in **Writing** and **Reading** scores.
* **Weekly Study Hours**: Students studying `> 10 hours` per week achieve higher average math and writing scores compared to those studying `< 5 hours`.
* **Gender Performance Dynamics**:
  - **Male** students average higher scores in **Math**.
  - **Female** students average higher scores in **Reading** and **Writing**.

---

## 🛠️ Tech Stack & Dependencies

* **Language**: Python 3.8+
* **Data Manipulation**: `pandas`, `numpy`
* **Data Visualization**: `matplotlib`, `seaborn`
* **Environment**: Jupyter Notebook / Google Colab

---

## 🚀 How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Saadkhan-777/Data_Analytics_Portfolio.git
   cd Data_Analytics_Portfolio/Project_04_Student_Exam_Scores
    
   ```

2. **Install Required Libraries**:
   ```bash
   pip install numpy pandas matplotlib seaborn
   ```

3. **Launch Notebook**:
   ```bash
   jupyter notebook Student_Exam_Scores.ipynb
   ```

---

## 📝 License & Acknowledgments

* **Dataset Source**: Standardized Public School Student Performance Dataset (Kaggle / Public Data).
* **Author**: Saad Khan
* Project completed as part of the Data Science & Analytics Learning Series.
