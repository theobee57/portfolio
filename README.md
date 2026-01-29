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

## Business Background

CDK Global encountered ongoing challenges in managing financial controls, delivery performance, and resource capacity across multiple projects using the Oracle Cloud Project Portfolio Management (PPM) platform.

Senior leadership needed to address a recurring question.

Where is the portfolio exposed, what causes this exposure, and where should intervention be prioritized?

Without an integrated executive dashboard, CDK Global risks multi-million-dollar losses from unchecked budget overruns and potential schedule delays on key projects. Executives require a dashboard that consolidates budget performance, schedule risk, and resource pressure into a single executive view.

## Business Objectives

The objective was to design a portfolio dashboard that enables leadership to:

1. Understand the overall portfolio financial condition.
2. Identify delivery risk beyond acceptable tolerance.
3. Detect systemic resource capacity pressure.
4. Prioritize high-value projects requiring intervention.
5. Explore risk tolerance scenarios.

## Data Overview

### Core entities

* Projects (portfolio, type, region, planned budget, progress)
* Project budgets (labor and non-labor categories)
* Time-phased actual costs
* Time-phased revenue / value realization
* Resources and roles
* Monthly resource assignments (hours and labor cost)
* Calendar month dimension

Each table was modeled at the appropriate level of detail and linked by logical relationships to prevent duplication and ensure data accuracy.

## Metrics Defined

Total Planned Budget: Sum of approved project budgets across the portfolio.

Actual Cost to Date: Cumulative actual costs recorded for all projects.

Budget Variance: The difference between the approved budget and actual cost.

Budget Consumed: Ratio of actual cost to approved budget.

Schedule Variance: The difference between the actual and planned percent complete.

Delivery Risk Status: Parameter-driven classification of projects based on schedule variance tolerance.

Role Utilization: Ratio of assigned hours to available capacity per role per month.

Capacity Risk Status: Classification of roles as Overallocated, Balanced, or Underutilized based on utilization thresholds.

## Analytical Approach

I applied a layered, validation-first approach to the analysis. Parameters governed analytical logic instead of filtering data, allowing leadership to explore different risk tolerances without recalculating base metrics. My approach included the following steps:

Step 1 - Financial Baseline: Established CFO-approved totals before introducing trends and segmentation.

Step 2 - Delivery Health: Evaluated schedule performance independently from financial indicators.

Step 3 - Resource Utilization: Modeled capacity pressure using explicit, defensible assumptions.

Step 4 - Portfolio Segmentation: Integrated finance, delivery, and resources to expose priority areas.

Step 5 - Executive Assembly: Developed a single-page dashboard for the steering committee.

## Executive Dashboard Design

### KPIs Section

A KPI row provides immediate context, linking each metric directly to a decision. 

KPI 1: Total Portfolio Budget to understand the scope and scale of the financial commitment.

KPI 2: Actual Cost to Date, so we can assess spending efficiency against the planned numbers.

KPI 3: Budget Variance, to identify any immediate financial discrepancies that require attention.

KPI 4: Budget Consumed, so we can evaluate the rate of expenditure relative to budgeted resources and adjust as necessary.

These KPIs address portfolio size and budget utilization efficiency.

### Key Insights Section

Insight 1: Portfolio spend is concentrated in a few portfolios, increasing exposure if delivery issues occur.

Insight 2: Schedule risk is unevenly distributed and does not always correlate with budget size.

Insight 3: Several roles exceed utilization thresholds during peak periods, indicating ongoing capacity pressure.

Insight 4: Several high-budget projects are behind schedule, representing significant delivery risk.

## Recommendations

Based on the analysis, I recommend the following actions.

1. Prioritize high-value, high-risk projects by intervening in projects combining large budgets with negative schedule variance.
2. Manage systemic resource pressure by rebalancing capacity or sequencing work to reduce ongoing role overutilization.
3. Explicitly align risk tolerance by using parameter-driven thresholds to ensure delivery expectations match the organization's risk profile.
4. Maintain portfolio balance by ensuring interventions address both large portfolios and smaller, high-risk areas.

## Why This Project Matters

The dashboard goes beyond reporting isolated metrics and supports leadership decisions in the following ways. By equipping executives with insights that drive confident decision-making, we can envision a future in which leadership accurately steers the portfolio toward strategic objectives, ensuring optimal resource utilization and project success.

* Design trustworthy KPIs. 
* Integrate finance, delivery, and resource data seamlessly.
* Use parameters for scenario-based decision support.
* Communicate portfolio risk clearly and concisely.

## Follow Up

With additional data, I would expand this work by:

* Modeling forecasted Estimate-at-Completion (EAC)
* Analyzing delivery risk by project phase
* Simulating capacity adjustments and schedule impact
* Integrating benefits realization metrics

## Final Note

This project demonstrates my approach to enterprise analytics challenges.

Validate first, integrate carefully, and design dashboards that leaders can act on immediately.

## Design Tools

* Tableau 
*  Parameters 
* Calculated Fields


# Revenue Health & Churn Risk (Executive Decision Support)

![Revenue Health/Risk](/images/dashboard1.png)   

## Tools

* Tableau
* Parameters & Actions
* Calculated Fields

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

* clear metric definitions
* validated logic
* interactive tools that support real decisions instead of static reporting

​







