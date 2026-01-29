# My Data Science Portfolio

I am an experienced Information Technologist with a passion for data science. I love data science because it is a key driver of the AI revolution, transforming our world, identifying needs, opportunities, and areas for improvement. I am a Data Analyst, working my way up to becoming a Data Scientist.

## Education
- BSc (Honours) Information Systems in Computer Science and Information Systems, University of South Africa
- Certificate in Oracle E-Commerce Development, University of Toronto
- Certificate in Project Leadership (Postgraduate) in Project Management, University of Waterloo 

## Data Science credentials:
- Data Analyst (Python), DataCamp
- Data Analyst Associate (SQL), DataCamp
- Associate Data Scientist, DataCamp (to be completed soon)

## Data Science Courses completed:
### Python
- Introduction to Python
- Intermediate Python
- Data Manipulation with Pandas
- Joining Data With Pandas
- Introduction to Statistics in Python
- Introduction to Data Visualization With Matplotlib
- Introduction to Data Visualization With Seaborn
- Introduction to Functions in Python
- Python Toolbox 
- Exploratory Data Analysis in Python
- Working With Categorical Data in Python
- Data Communication Concepts
- Introduction to Importing Data in Python
- Cleaning Data in Python
- Working With Dates and Times in Python
- Writing Functions in Python
- Introduction to Regression With Statsmodels in Python
- Sampling in Python
- Hypothesis Testing in Python
- Experimental Design in Python
- Supervised Learning with Scikit-Learn
- Unsupervised Learning in Python
- Machine Learning With Tree-based Models in Python

### SQL
- Joining Data in SQL
- Data Manipulation in SQL
- Exploratory Data Analysis in SQL
- PostgreSQL Summary Stats and Window Function
- Data-Driven Decision Making in SQL
- Applying SQL to Real-World Problems

## My Latest Projects
## Executive Project Portfolio Performance & Risk (PPM Analytics)
This project demonstrates executive portfolio analytics for an integrated Project Portfolio Management (PPM) environment. The dashboard combines financial performance, delivery risk, and resource capacity to support prioritization and leadership decision-making.

### Executive Project Portfolio Performance & Risk Overview
An integrated dashboard combining financial performance, delivery health, and resource capacity to support executive portfolio decisions.
![Revenue Health/Risk](/images/ppm1_dashboard.png)

### Portfolio Financial Baseline
Executive KPIs establish approved budget, actual spend, remaining headroom, and budget consumption across the portfolio.
![Revenue Health/Risk](/images/ppm2_kpis.png)

### Portfolio Spend Is Concentrated Across a Small Number of Portfolios
A limited set of portfolios account for the majority of approved spend, increasing exposure if delivery performance declines.
![Revenue Health/Risk](/images/ppm3_budget.png)

### Delivery Risk Is Unevenly Distributed Across the Portfolio
Certain portfolios exhibit a disproportionate number of projects behind schedule, independent of total budget size.
![Revenue Health/Risk](/images/ppm4_delivery_risk.png)

### Systemic Resource Pressure Drives Delivery Risk
Multiple roles exceed utilization thresholds during peak execution periods, indicating structural capacity constraints rather than isolated issues.
![Revenue Health/Risk](/images/ppm5_resource_capacity.png)

### High-Value Projects Behind Schedule Require Immediate Attention
Mapping project value against schedule variance highlights where executive intervention can deliver the greatest impact.
![Revenue Health/Risk](/images/ppm6_matrix.png)



========
## Revenue Health & Churn Risk (Executive Decision Support)

![Revenue Health/Risk](/images/dashboard1.png)   

## Tools

Tableau Desktop · Parameters & Actions · Calculated Fields

## 1. Business Background

A telecommunications company uses a subscription model with multiple contract types and customer segments. While revenue appears steady, leadership faces an ongoing challenge:

** How much revenue is exposed to churn risk, and how sensitive is that risk to leadership’s tolerance level?

This project enables executives to simulate risk tolerance decisions and immediately see their impact on revenue exposure.

## 2. Business Objectives

This project supports executive decision-making by answering the following questions:

* How concentrated is revenue across contract types?
* Which segments exceed acceptable churn risk?
* How does revenue exposure change as churn tolerance tightens or loosens?
* Where should retention efforts be given priority to protect revenue?

## 3. Data Overview

The dataset contains customer-level subscription data, including:

* Monthly charges (revenue proxy)
* Customer tenure (lifecycle indicator)
* Contract type
* Internet service type
* Customer churn status (Yes/No)

The dataset lacks calendar-based snapshots. All metrics were defined bearing this in mind, to ensure accuracy, transparency, and defensibility.

## 4. Key Metrics Defined

Active Monthly Revenue

Sum of monthly charges for non-churned customers - used as a proxy for Monthly Recurring Revenue (MRR)

Active Customers

Distinct count of customers who have not churned.

Customer Churn Rate

Proportion of customers who have discontinued within each segment.

Note: Monthly churn was intentionally avoided due to data limitations.

Revenue at High Churn Risk (Executive KPI)

Revenue associated with segments whose churn rate exceeds a user-defined risk threshold.

## 5. Analytical Approach

This project goes beyond descriptive analytics by introducing parameter-driven what-if analysis.

Key design principles:

* Metrics remain stable and validated.
* Parameters control analytical logic, not data filtering.
* Executives define what “high risk” means.
* The dashboard responds instantly without recalculating base metrics.

## 6. Dashboard Design

## Key Business KPIs with Risk Exposure
In addition to core revenue and churn metrics, this dashboard quantifies how much revenue is exposed to churn risk above a configurable tolerance level.

![KPIs](/images/KPI2.png)

A dedicated KPI row provides immediate business context:

* Active Monthly Revenue
* Active Customers
* Overall Customer Churn Rate
* Revenue at High Churn Risk (dynamic)

Together, these KPIs answer:

“How large is the business, and how much of it is at risk?”

Core Analytical Views

Revenue Contribution by Contract

Highlights revenue concentration across contract types, showing which segments are most critical to business stability.

Customer Churn Risk by Contract

Uses parameter-driven coloring to classify contract types as acceptable risk or high risk, based on executive-defined thresholds.

Monthly Charges vs Customer Tenure

Provides diagnostic insight into the relationship between customer tenure and revenue contribution.

## Key Insights

### 1. Medium tenure and long-tenure contracts generate the most revenue.

![Revenue Contribution](/images/revenue_trend3.png)


### 2. Revenue Is Concentrated in Long-Term Contracts, creating both strength and dependency.


![Contracts](/images/contracts4.png)

A small number of contract types generate the majority of revenue, creating both stability and concentration risk.
  
### 3. As churn risk thresholds tighten, a disproportionate share of revenue becomes classified as “at risk.”

![Contracts](/images/risks5.png)

Executives can adjust churn risk tolerance and instantly identify which contract types exceed acceptable risk levels.

### 4. Tenure Is Associated with Higher Monthly Charges

![Tenures](/images/tenures6.png)

Longer-tenured customers tend to generate higher monthly revenue, reinforcing the importance of retention-focused strategies.

## 7. Recommendations

Based on the analysis:

1. Protect high-value segments
2. Prioritize retention strategies for long-term contract customers who contribute the majority of revenue.
3. Reduce exposure in high-risk segments.
4. Introduce targeted incentives or contract migration strategies for month-to-month customers.
5. Use risk tolerance explicitly.
6. Leadership should align churn risk thresholds with the business strategy, while being aware of the trade-off between growth flexibility and revenue consistency.

## 8. Why This Project Matters

This project shows my ability to:

* Design executive-focused KPIs
* Use parameters for scenario simulation, not gimmicks.
* Translate analytical metrics into risk-based decision support.
* Balance technical correctness with business usability.

Instead of reporting churn and revenue independently, this dashboard connects them to inform leadership action.

## 9. What I would Explore Next

With additional data, I would extend this analysis by:

* Modeling churn risk by tenure cohorts
* Quantifying the cost of churn-mitigation strategies
* Simulating revenue impact of contract-mix changes
* Integrating time-based churn snapshots for trend analysis

## Final Note

This project demonstrates how I approach executive analytics problems:

-clear metric definitions
-validated logica
-interactive tools that support real decisions instead of static reporting.

​







