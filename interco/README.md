# Sales Performance & Profitability Analysis

## Project Overview
This project analyzes sales, profit, discounting, and product performance across regions, customer segments, and categories. The goal is to identify what drives revenue, where margins are leaking, and which business areas require action.

## Business Problem
A company can grow revenue while still underperforming on profit because of discounting, product mix, regional inefficiencies, or weak category performance. This analysis answers questions such as:
- Which regions generate the most sales and profit?
- Which categories and products are most profitable?
- Where are discounts hurting margin?
- Which products or sub-categories are loss-making?
- How do sales and profit trend over time?

## Dataset
The dataset in this project is a realistic synthetic business dataset with more than 12,000 cleaned rows and the following fields:
- `order_id`
- `order_date`
- `ship_date`
- `ship_mode`
- `customer_id`
- `segment`
- `region`
- `category`
- `sub_category`
- `product_name`
- `sales`
- `quantity`
- `discount`
- `profit`

A raw version is also included with a small number of duplicates and missing values for data-cleaning practice.

## Tools Used
- Python
- pandas
- numpy
- matplotlib
- Jupyter Notebook

## Project Structure
```text
sales-performance-analysis
│
├── data
│   ├── raw_sales_data.csv
│   └── cleaned_sales_data.csv
│
├── notebooks
│   └── sales_analysis.ipynb
│
├── visuals
│
├── README.md
└── requirements.txt
```

## Analysis Workflow
1. Load and inspect the raw dataset
2. Clean missing values and duplicates
3. Create core business KPIs:
   - Total Sales
   - Total Profit
   - Profit Margin
   - Average Order Value
4. Analyze performance by:
   - Region
   - Segment
   - Category
   - Sub-category
   - Product
   - Month
5. Evaluate discount impact on profitability
6. Identify top- and bottom-performing products
7. Summarize business insights and recommendations

## Recommended Charts
- Sales by Region
- Profit by Category
- Monthly Sales Trend
- Average Profit by Discount Level
- Top 10 Products by Profit
- Bottom 10 Products by Profit

## Example Business Insights
- Revenue may be concentrated in one or two regions, but those regions may not have the highest margins.
- Heavy discounting can significantly reduce profit.
- Some product lines may generate strong sales but low or negative profit.
- Seasonal spikes may indicate where the business should focus inventory and marketing.

## Business Recommendations
- Review pricing and discount strategy for low-margin products
- Reduce deep discounting on already high-demand items
- Reassess loss-making products or sub-categories
- Concentrate sales effort on high-margin categories and regions
- Use monthly trend analysis to support forecasting and campaign planning
