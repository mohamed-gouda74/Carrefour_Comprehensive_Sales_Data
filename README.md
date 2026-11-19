# 🛒 Carrefour Comprehensive Sales Data Analysis

## 📌 Project Overview

This project focuses on performing comprehensive data cleaning, preparation, and exploratory data analysis (EDA) on Carrefour sales transaction data using Python.

The main objective is to transform raw sales data into a clean, structured dataset and extract meaningful business insights related to sales performance, customer behavior, product categories, store locations, and purchasing trends.

The project covers the complete data analysis workflow, starting with data inspection and cleaning, followed by feature engineering and exploratory data analysis, ending with business insights supported by visualizations.

---

## 🎯 Project Objectives

- Inspect and understand the structure and quality of the dataset.
- Identify and handle missing values and invalid data.
- Detect duplicate records and investigate potential outliers.
- Prepare and transform data for further analysis.
- Analyze sales and financial performance using KPIs.
- Explore customer purchasing behavior and demographics.
- Compare sales performance across store locations and product categories.
- Identify monthly, yearly, and weekly sales trends.

---

## 📂 Dataset Overview

The dataset contains **10,000 sales transactions** with 28 original columns.

It includes information about:

- Transaction details and timestamps.
- Store IDs, locations, regions, and store types.
- Customer demographics and loyalty information.
- Product names, categories, subcategories, and brands.
- Unit prices, quantities, discounts, taxes, and shipping costs.
- Payment methods and delivery types.
- Order statuses, promotions, and customer ratings.

After feature engineering, the dataset contains **35 columns**.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Main programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations and missing value handling |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Plotly Express | Interactive charts |
| Plotly Graph Objects | KPI indicators and dashboard components |
| Jupyter Notebook | Development environment |

---

## 🧹 Project Workflow

### 1. Data Inspection & Initial Preparation

- Loaded the dataset using Pandas.
- Inspected dataset dimensions and sample records.
- Cleaned column names by removing unnecessary spaces.
- Reviewed data types and converted relevant columns.
- Converted transaction dates into the appropriate datetime format.

### 2. Data Quality Assessment

- Checked for duplicate records.
- Identified missing values and calculated their percentages.
- Examined numerical and categorical columns using descriptive statistics.
- Investigated relationships between categorical features to identify possible ways to recover missing information.

**Initial findings:**
- 10,000 records.
- 28 original columns.
- 0 fully duplicated rows.
- Missing values were identified across multiple columns.

### 3. Data Cleaning & Missing Value Handling

Applied different cleaning techniques depending on the nature of each column.

**Categorical Data:**
- Used logical relationships between store IDs, locations, regions, and store types.
- Used product-related relationships to recover missing product information.
- Applied mode imputation where appropriate.
- Assigned descriptive placeholders to certain missing identifiers and categorical values.

**Numerical Data:**

Investigated invalid or unrealistic values in:

- Customer Age
- Customer Rating
- Unit Price
- Quantity Sold
- Total Transaction Amount
- Discount
- Tax Amount
- Shipping Cost

Invalid values were converted to missing values based on defined validation rules, then handled using median imputation.

### 4. Outlier Detection

Used the **Interquartile Range (IQR)** method to identify statistical outliers in numerical columns.

The investigation included:

- Calculating Q1, Q3, and IQR.
- Defining lower and upper statistical boundaries.
- Counting values outside the calculated boundaries.
- Investigating unusually high unit prices by product category.

The investigation showed that some high unit prices were associated with Electronics products, highlighting the importance of understanding business context before treating statistical outliers as errors.

### 5. Feature Engineering

Created additional features to support deeper analysis:

- `Year`: Extracted transaction year.
- `Month`: Extracted transaction month.
- `Day`: Extracted day of the month.
- `Day_Name`: Extracted weekday name.
- `Hour`: Extracted transaction hour.
- `Age_Group`: Segmented customers into age groups.
- `Customer_Rating_%`: Converted customer ratings from a 5-point scale into percentages.

The final dataset contains **35 columns**.

### 6. Final Data Validation

Performed a final missing-value check to ensure the cleaned dataset was ready for analysis.

**Final result: 0 remaining missing values.**

---

## 📊 Exploratory Data Analysis (EDA)

The analysis was divided into two main sections.

### 1. Sales & Financial Performance

Calculated six Key Performance Indicators (KPIs):

| KPI | Result |
|---|---:|
| Total Sales Revenue | EGP 44.74 Million |
| Total Transactions | 10,000 |
| Average Order Value (AOV) | EGP 4,473.92 |
| Total Quantity Sold | 40,134 Units |
| Average Customer Rating | 2.98 / 5 |
| Average Discount Rate | 7% |

### 2. Store & Customer Performance

Created 11 visualizations to explore different aspects of business performance:

1. Total Sales by Store Location.
2. Total Sales by Product Category.
3. Distribution of Transaction Amounts (Histogram).
4. Box Plot for Outlier Detection.
5. Total Sales by Customer Gender.
6. Total Sales by Customer Age Group.
7. Sales Distribution by Store Type.
8. Yearly Sales Trend (2025–2026).
9. Monthly Sales Performance and Seasonality.
10. Sales Distribution by Day of the Week.
11. Average Customer Rating by Product Subcategory.

---

## 💡 Key Business Insights

### 1. Product Category Performance

- Electronics generated the highest sales revenue, approximately EGP 42.12 million.
- Electronics represented the dominant share of total sales compared with other product categories.

### 2. Store Location Performance

- Maadi - Grand Mall recorded the highest sales, approximately EGP 6.84 million.
- Mansoura and Cairo - Mall of Arabia followed among the top-performing locations.

### 3. Customer Demographics

- Customers aged 31–45 generated the highest sales, approximately EGP 14.26 million.
- The 46–60 age group ranked second, generating approximately EGP 11.98 million.
- Female customers generated slightly higher sales than male customers.

### 4. Store Type Performance

- Hypermarkets generated approximately EGP 24.94 million.
- Supermarkets generated approximately EGP 19.80 million.

### 5. Sales Trends

- 2025 recorded approximately EGP 27.56 million in sales.
- 2026 recorded approximately EGP 17.18 million in the available dataset.
- January recorded the highest monthly sales, approximately EGP 4.95 million.
- September recorded the lowest monthly sales, approximately EGP 1.99 million.

### 6. Weekly Sales Performance

- Tuesday recorded the highest sales among the days of the week.
- Saturday ranked second in total sales.

### 7. Customer Satisfaction

- The overall average customer rating was 2.98 out of 5.
- Customer ratings were also compared across product subcategories to explore differences in customer satisfaction.

---

## 📈 Final Dashboard

The project concludes by combining the six KPIs and eleven visualizations into a comprehensive analytical dashboard using Plotly.

The dashboard provides an overview of:

- Overall sales performance.
- Financial indicators.
- Store and location performance.
- Customer demographics.
- Product category performance.
- Sales trends and seasonality.
- Customer satisfaction.

---

## 📝 Conclusion

This project demonstrates a complete practical data analysis workflow using Python, from raw data inspection and cleaning to feature engineering and exploratory data analysis.

By analyzing 10,000 sales transactions, the project highlights important patterns in customer behavior, product performance, store contributions, and sales trends.

The extracted insights can support better business understanding and help identify areas that may require further investigation and improvement.

---

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn plotly openpyxl jupyter
```

3. Place the Excel dataset file (`Carrefour_Comprehensive_Sales_Data.xlsx`) in the appropriate working directory.
4. Open the notebook:

```bash
jupyter notebook
```

5. Run `Carrefour 1.ipynb` to explore the complete analysis.

---

**Project Type:** Exploratory Data Analysis (EDA) & Data Cleaning  
**Domain:** Retail / Sales Analytics  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly
