# Sales-Analytics-Dashboard-Excel
This project is an end-to-end Sales Analytics Dashboard built in Microsoft Excel. It analyzes sales performance across customers, countries, product lines, and order behavior to generate actionable business insights.

## 📁 Dataset Overview
- Source: Sales transaction dataset
- Records: ~2800+ rows
- Features: Orders, customers, products, revenue, geography

## 🧹 Data Cleaning Process

The dataset was cleaned and prepared in Excel before analysis to ensure accuracy and consistency for dashboard creation.

### 1. Handling Missing Values
- Identified missing values in key columns:
  - ADDRESSLINE2: 2521 out of 2823 values were blank
  - POSTALCODE: 76 missing values
  - STATE: 1486 missing values (~52%)

- Removed **ADDRESSLINE2** column as it contained mostly null values and added little analytical value.

- Handled STATE column by replacing missing values with **"Not Applicable"**, as many countries do not use state-level addressing.

- Standardized POSTALCODE missing values by replacing blanks with **"Unknown"**.

---

### 2. Duplicate Data Check
- Performed duplicate check using Excel “Remove Duplicates” tool.
- No duplicate records were found in the dataset.

---

### 3. Date Standardization
- Cleaned and standardized the ORDERDATE column for consistency.
- Created a cleaned version using:
  `=IFERROR(LEFT(F2,FIND(" ",F2)-1),F2)`
- Converted the result into a proper date format (dd-mm-yyyy).
- Replaced the original column with the cleaned version.

---

### 4. Data Type Standardization
- Converted POSTALCODE and PHONE columns to **Text format** to preserve formatting and prevent data loss.

---

### 5. Additional Cleaning Steps
- Created CLEANED_POSTALCODE using:
  `=IF(LEN(TRIM(A2))=0,"Unknown",A2)`
- Standardized STATE values using:
  `=IF(TRIM(A2)="","Not Applicable",A2)`
- Ensured consistency across text fields by trimming extra spaces and formatting issues.

## 📊 Exploratory Data Analysis (EDA)

After cleaning the dataset, exploratory data analysis was performed to understand sales performance and business behavior across different dimensions.

### 1. Sales Performance Overview
- Calculated total sales, total orders, and average order value (AOV).
- Identified overall revenue generation patterns across the business.

### 2. Country-wise Sales Analysis
- Analyzed revenue distribution across different countries.
- Identified top-performing markets contributing the highest sales revenue.
- Observed strong revenue concentration in a few key regions.

### 3. Product Line Analysis
- Evaluated sales performance across different product lines.
- Identified top-performing product categories contributing maximum revenue.
- Highlighted underperforming product segments for potential improvement.

### 4. Customer Analysis
- Identified top customers based on total revenue contribution.
- Observed a long-tail distribution where a few customers contribute significantly higher revenue.
- Highlighted dependency on major accounts.

### 5. Deal Size Analysis
- Analyzed revenue contribution based on deal size (Small, Medium, Large).
- Found that medium-sized deals contribute the highest share of revenue.
- Identified opportunities to increase large deal conversions.

### 6. Order Status Analysis
- Evaluated order fulfillment status distribution.
- Observed that majority of orders are successfully shipped.
- Minor proportion of orders fall under cancelled or disputed categories.

## 📊 Dashboard Overview

An interactive Excel dashboard was created to visualize key business metrics and insights derived from the dataset.

### 📌 Key Dashboard Components:
- KPI Cards: Total Sales, Total Orders, Average Order Value (AOV)
- Country-wise Sales Analysis (Top 10 Markets)
- Product Line Performance Analysis
- Top Customers by Revenue Contribution
- Deal Size Distribution
- Order Status Breakdown

### 📈 Tools Used:
- Microsoft Excel
- Pivot Tables
- Charts (Bar, Line, Pie/Donut)
- Data Cleaning using Excel formulas

---

## 💡 Key Insights

- USA dominates sales revenue, indicating strong North American demand concentration. Diversification opportunities exist in underperforming European markets
- Classic Cars dominate revenue contribution, indicating strong demand for premium collectible segments. Opportunity exists to improve underperforming product lines.
- Medium-sized deals contribute the highest revenue share, indicating balanced customer purchasing behavior. Focus on increasing Large deal conversions for revenue expansion.
- Revenue is heavily concentrated in a few key customers, with Euro Shopping Channel alone contributing the highest share, indicating a strong dependency on top accounts. The rest of the customers follow a long-tail distribution with significantly lower individual contributions.
- Majority of orders are successfully shipped, indicating strong operational efficiency. Minor proportion of cancelled/disputed orders highlights limited business risk.
- A major portion of sales comes from countries where state-level segmentation does not exist or is not recorded, making country-level analysis more reliable than state-level insights for this dataset. However, state-level data is only relevant for certain countries like the USA and Australia. Within structured regions, states like NY, MA, and NSW emerge as the top revenue contributors.

---

## 📷 Dashboard Preview

<img width="1152" height="595" alt="image" src="https://github.com/user-attachments/assets/b0a96edc-1c6f-45c0-93b9-15acee922391" />
<img width="1151" height="682" alt="image" src="https://github.com/user-attachments/assets/83c11230-ae01-4d52-9076-cb1b622b23d0" />

---

## 🚀 Conclusion

This project demonstrates end-to-end data analysis skills including data cleaning, transformation, visualization, and business insight generation using Excel. It highlights the ability to convert raw transactional data into meaningful business intelligence for decision-making.
