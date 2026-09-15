# 📱 Project 05: Mobile Sales Dashboard — Power BI

An interactive Power BI dashboard analyzing mobile phone sales data across Indian cities, brands, and models. Built as the 5th project in my Data Science & Analytics Learning Series, focusing on business intelligence and data visualization skills using a single-page, fully filterable report layout.

---

## 📊 Dashboard Overview

The dashboard provides a comprehensive view of mobile sales performance through the following KPI cards and visualizations:

### KPI Cards
| Metric | Value (Sample) |
|--------|---------------|
| Total Sales | 49M |
| Total Quantity | 1K |
| Transactions | 251 |
| Average | 40K |

### Visuals Included

| Visual | Chart Type | Description |
|--------|-----------|-------------|
| Total Sales by City | Map | Bubble map showing geographic sales distribution across Indian cities |
| Total Quantity by Month | Line Chart | Monthly trend of units sold throughout the year |
| Total Sales by Mobile Model | Bar Chart | Horizontal bar ranking models by revenue |
| Total Sales by Day Name | Area Chart | Sales pattern across days of the week |
| Transactions by Payment Method | Pie Chart | Breakdown of UPI, Debit Card, Cash, and Credit Card usage |
| Customer Ratings | Funnel Chart | Distribution of customer ratings (1–5) |
| Brand Summary Table | Table | Brand-wise Total Sales, Total Quantity, and Transactions |

---

## 🎛️ Filters / Slicers

The report includes the following interactive slicers to drill into specific segments:

- **Month** — Tile-style slicer (January – December)
- **Mobile Model** — Dropdown
- **Payment Method** — Dropdown
- **Brand** — Dropdown
- **Day Name** — Dropdown

All visuals cross-filter each other for dynamic exploration.

---

## 🗂️ Data Model

**Source Table:** `Sales_Data`

**Key Columns used across visuals:**

| Column | Type | Used In |
|--------|------|---------|
| Date | Date | Month slicer, line chart |
| City | Text | Map visual |
| Brand | Text | Slicer, table |
| Mobile Model | Text | Slicer, bar chart |
| Payment Method | Text | Slicer, pie chart |
| Day Name | Text | Slicer, area chart |
| Customer Ratings | Number | Funnel chart |

**Measures:**

| Measure | Description |
|---------|-------------|
| Total Sales | Sum of sales revenue |
| Total Quantity | Sum of units sold |
| Transactions | Count of transactions |
| Average | Average sales value |

---

## 🛠️ Tools & Technologies

- **Tool**: Power BI Desktop
- **Data Source:** Sales_Data table (imported/embedded)
- **Theme:** Microsoft CY24SU10 base theme
- **Color Scheme:** Motorola brand blue (`#0060AA`) with white backgrounds

---

## 📁 File Structure

```
📦 Project_05_Mobile_Sales_Dashboard
 ┣ 📄 PowerBI_Project_-_Mobile_Sales_Dashboard.pbix   # Main Power BI file
 ┗ 📄 README.md
```

---

## 🚀 How to Open

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. Clone or download this repository.
3. Open `PowerBI_Project_-_Mobile_Sales_Dashboard.pbix` in Power BI Desktop.
4. Explore the dashboard using the slicers and interactive visuals.

---

## 💡 Key Insights the Dashboard Answers

- Which cities generate the highest mobile sales revenue?
- Which mobile models are the top sellers?
- What payment methods do customers prefer?
- How do sales vary across months and days of the week?
- What is the customer satisfaction distribution?

---

## 👤 Author

**Saad Khan**
CS Student — University of Peshawar
📧 saadpk848@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/saad-khan-a50953370/)

---

## 📌 Notes

- This project was built for learning and portfolio purposes.
- The dataset covers mobile phone sales across major Indian cities including Delhi, Mumbai, Bangalore, Chennai, Hyderabad, and more.
- The dashboard is single-page and designed at 1280×720 resolution.
- Part of the **Data Science & Analytics Learning Series** — Project 05 of ongoing portfolio.
