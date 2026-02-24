# E-commerce Sales Analysis – SQL Portfolio Project


## 📌 Project Overview

In this project, I analysed an e-commerce sales dataset using **pure MySQL** to uncover actionable business insights. I performed data cleaning, exploratory data analysis (EDA), and answered real-world business questions that managers/stakeholders would ask.

**Goal** 
To demonstrate my SQL skills (aggregations, window functions, CTEs, subqueries, date manipulation) while thinking like a data analyst - focusing on **business value** rather than just technical queries.

**Dataset**
I used a data set that is available on Kaggle (E-commerce sales) containing order_date, product_name, category, region, quantity, sales and profit columns.

**Key Questions Answered**:
- What are the overall KPIs (total revenue, profit)?
- How have sales and orders trended over time?
- Which categories / products drive the most revenue and profit?
- Which regions perform best / worst?
- What is the profit by category and region?
- Which products are underperforming (low or negative profit)?

## 🛠️ Tools & Technologies

- **Database**: MySQL
- **SQL Features Used**: GROUP BY, ORDER BY, CTEs, Subqueries, Window functions (running totals), DATE_FORMAT, aggregations


## 📊 Key Insights & Business Recommendations

- Total revenue reached **10 667 881**, with an overall profit of **1 844 665** in 3 years (2022-2024). The profit margin remained relativeLY the same for the first two years at **~18%** and decresed slightly in 2024 to **~17%**. This indicates low profitability or slow growth
- **Electronics** category generates **5 326 074** of revenue, and **923 186** of profit, both of which are the highest, making it the most profitable category. Increasing marketing efforts to increase sales in this category could boost the company's profitability

## Regional Analysis ##
- Interestingly, sales volume, revenue, and profit are distributed quite evenly across all regions (differences < 12–15%). This suggests the business has achieved strong national    consistency in marketing, pricing, product offering, and delivery, a sign of a well-executed, scalable e-commerce model with limited geographic dependency.
However, small variations in profit margin and average order value still exist. Next steps could include:
- Testing targeted promotions in the slightly higher-margin regions
- Monitoring whether new infrastructure investments create divergence over time

## Product Analysis ##  
**Monitors** lead in volume, but **Cameras** have the highest profit margin. Therefore, the company must protect & promote Monitor + Camera (high volume + high profit margin)
- Smartwatches lag in price per unit,  possible entry-level positioning or heavy promotion.

## 🔍 Project Walkthrough: Step-by-Step Process

I followed a structured, analyst-first approach to extract meaningful insights from the raw e-commerce sales data. Below is the exact journey I took — from first opening the dataset to delivering business-ready recommendations.

### 1. Understanding the Data (Schema & Initial Exploration)
**Goal**: Know what I’m working with before touching anything.

- I created and worked with duplicate tables to preserve the original data
- Ran `DESCRIBE sales;` to inspect column names and data types  
- Checked date range, unique values, and basic statistics

### 2. Data Cleaning
**Goal**: Make the data trustworthy and analysis-ready.

Steps I performed:
- Removed duplicate rows
- Standardized text (category and region names)
- Handled NULLs and blanks
- Changed data types (`Sales` and `Profit` from INT/DOUBLE to `DECIMAL(12,2)`)
- Verified date column was properly stored as `DATE`

**Key query used**:
```sql
ALTER TABLE sales 
MODIFY COLUMN Sales DECIMAL(12,2),
MODIFY COLUMN Profit DECIMAL(12,2);

## 📁 Project Files

- `sales.sql`               → Main SQL script with all cleaning + analysis queries
- `schema.png` / `describe_output.txt` → Table structure & data types
- `insights.md` / screenshots → Visuals & key result tables (optional)
- `README.md`               → This file

## 🔍 How to Run / Explore This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ecommerce-sales-analysis.git
