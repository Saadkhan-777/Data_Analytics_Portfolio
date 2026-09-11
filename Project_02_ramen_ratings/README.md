# Ramen Ratings Data Analysis (Data Analysis Project #2)

A comprehensive exploratory data analysis (EDA) of the global **Ramen Ratings** dataset using **Python**, **NumPy**, **Pandas**, **Matplotlib**, and **Seaborn**.

---

## 📌 Project Overview
This is my **2nd data analysis project** focusing on end-to-end data cleaning, preprocessing, feature engineering, and exploratory visual analysis. The primary objective of this project is to analyze global instant ramen reviews to uncover trends across packaging styles, brand distributions, geographic origins, and overall ratings.

---

## 📂 Dataset Overview
The raw dataset (`ramen-ratings.csv`) contains **2,580 entries** and **7 initial features**:
* **Review #**: Unique review identification number assigned chronologically.
* **Brand**: The manufacturing company/brand of the ramen product.
* **Variety**: The specific flavor name or product variant.
* **Style**: Packaging format (`Pack`, `Bowl`, `Cup`, `Tray`, `Box`, `Can`, `Bar`).
* **Country**: The country of origin for the brand/product.
* **Stars**: The rating assigned to the ramen (originally stored as object/string format).
* **Top Ten**: Historical annual ranking status (e.g., `2016 #10`, `2015 #1`, missing for non-ranked items).

---

## 🛠️ Data Cleaning & Preprocessing Workflow
1. **Working Copy Creation**: Created an isolated DataFrame copy (`df_clean`) to protect raw source data.
2. **Type Conversion & Handling Non-Numeric Values**:
   - Identified string/unrated values (`"Unrated"`) in the `Stars` column using `pd.to_numeric(errors='coerce')`.
   - Converted `Stars` into a numerical float (`float64`) datatype for statistical analysis.
3. **Missing Value Imputation**:
   - Imputed missing packaging `Style` values (`0.08%` missing) using modal imputation (`.mode()[0]`).
4. **Feature Engineering**:
   - **`Is_Top_Ten`**: Engineered a binary flag (`1` / `0`) indicating whether a ramen product was ever featured in the annual Top Ten list.
   - **`Top Ten Status`**: Created a categorical label (`"Top Ten"` vs `"Not Top Ten"`).
   - **`Rating Category`**: Binned numerical star ratings into 4 discrete categories (`Low` [0-2], `Fair` [2-3], `Good` [3-4], `Excellent` [4-5]) using `pd.cut`.
5. **Text Cleaning & Normalization**:
   - Stripped unwanted whitespace across text fields (`Brand`, `Variety`, `Style`, `Country`).
   - Standardized `Brand` naming conventions using title-case formatting (`.str.title()`).
6. **Redundant Column Removal**:
   - Dropped the original sparse and noisy `Top Ten` column after extracting structured binary features.

---

## 🔑 Key Insights & Findings
* **Dataset Scale**: Evaluated **2,580 total reviews** spanning **355+ distinct brands** across **38 countries**.
* **Average Global Rating**: The overall average rating across all evaluated instant ramen products is **~3.65 / 5.00 stars** ($	ext{std} pprox 1.015$).
* **Top Brands by Review Count**:
  1. **Nissin** (381 reviews) — Dominates total review volume by a wide margin.
  2. **Nongshim** (98 reviews)
  3. **Mama** (98 reviews)
  4. **Maruchan** (76 reviews)
  5. **Paldo** (66 reviews)
* **Packaging Styles**:
  - `Pack` is the most popular style (**1,531 reviews**), followed by `Bowl` (**481 reviews**) and `Cup` (**450 reviews**).
  - High-end/specialty packaging like `Box` ($\mu pprox 4.29$) and `Bar` ($\mu = 5.0$) boast higher average star ratings compared to mass-market `Cup` ($\mu pprox 3.50$) or `Tray` ($\mu pprox 3.55$) formats.
* **Geographic Distribution**:
  - Top countries by submission volume: **Japan** (352), **USA** (323), **South Korea** (309), **Taiwan** (224), and **Thailand** (191).
  - Highest average product ratings are observed in regions like **Brazil**, **Sarawak**, **Malaysia** ($\mu pprox 4.15$), and **Singapore** ($\mu pprox 4.13$).

---

## 🧰 Tools & Technologies Used
* **Python**: Core programming language.
* **Pandas**: Data manipulation, filtering, string operations, binning, and aggregation.
* **NumPy**: Numeric operations and conditional logic (`np.where`).
* **Matplotlib & Seaborn**: Data visualization and distribution plots.

---

## 🚀 How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/Saadkhan-777/Data_Analytics_Portfolio.git
   cd Data_Analytics_Portfolio/Project_02_ramen_ratings
   ```
2. Install required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Place `ramen-ratings.csv` in the project root directory.
4. Launch the Jupyter Notebook or Google Colab and run all cells sequentially.

---

## 👤 Author
**Saad Khan**  
*Data Science & Agentic AI Student | Passionate about Data Analytics & Visualization*
